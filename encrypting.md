[return](diskmgmt)

:encrypting:

```sh

#(Optional) Fill the partition with random data before encryption
#Overwrite the partition 3 times with random data, that's enough to protect you against forensic investigation. It took me nearly 30 minutes for 20 GB partition to be overwritten 3 times.
shred --verbose --random-source=/dev/urandom --iterations=3 /dev/sda3

#Several minutes per gigabytes
dd if=/dev/urandom of=<device>

#Fastest way, which provides lower quality random data:
badblocks -c 10240 -s -w -t random -v <device>

#Create cryptographic device mapper device in LUKS encryption mode
#https://howtoforge.com/tutorial/how-to-encrypt-a-linux-partition-with-dm-crypt-luks/?fbclid=IwAR0F15NR984djKwM6ZI5SLKGltogTUFwSQP6moKXlrJwvHLTsaBecG2XLoQ
cryptsetup --verbose --cipher aes-xts-plain64 --key-size 512 --hash sha512 --iter-time 5000 --use-random luksFormat /dev/sda3

#Or you can also create a cryptographic device mapper this way
sudo cryptsetup luksFormat /dev/sda2

#After supplying the passphrase twice the device will be formatted for use. To verify, use the following command:
sudo cryptsetup isLuks /dev/sda2 && echo affirmative

#To see a summary of the encryption information for the device, use the following command:
sudo cryptsetup luksDump /dev/sda2

#To find a LUKS device's UUID, run the following command:
sudo cryptsetup luksUUID /dev/sda2

#An example of a reliable, informative and unique mapping name would be luks-<uuid>, where <uuid> is replaced with the device's LUKS UUID (eg: luks-50ec957a-5b5a-47ee-85e6-f8085bbc97a8). This naming convention might seem unwieldy but is it not necessary to type it often.
sudo cryptsetup luksOpen /dev/sda2 luks-50ec957a-5b5a-47ee-85e6-f8085bbc97a8

#There should now be a device node, /dev/mapper/<name>, which represents the decrypted device. This block device can be read from and written to like any other unencrypted block device.
#To see some information about the mapped device, use the following command:
sudo dmsetup info luks-50ec957a-5b5a-47ee-85e6-f8085bbc97a8

#Create a file system on the mapped device
sudo mkfs.ext4 /dev/mapper/luks-50ec957a-5b5a-47ee-85e6-f8085bbc97a8

#To mount this mapped filesystem on /mnt/test, use the following command:
mount /dev/mapper/luks-50ec957a-5b5a-47ee-85e6-f8085bbc97a8 /mnt/test

#For the system to setup a mapping and a permanent mount point for the device there must be an entry present in /etc/crypttab and /etc/fstab which is written on the next node

#In order to remove the dm-crypt mapping, unmount mapped device and close the mapping of the device
sudo umount /dev/mapper/luks-luks_uuid
sudo cryptsetup close luks-luks_uuid

#Set a randomly generated key as an additional way to access an encrypted block device
#This will generate a 256-bit key in the file $HOME/keyfile
dd if=/dev/urandom of=$HOME/keyfile bs=32 count=1
chmod 600 $HOME/keyfile

#Add the key to an available keyslot on the encrypted device
sudo cryptsetup luksAddKey /dev/sda2 ~/keyfile

#Aside from keyfiles you can also just add a passphrase key on the device
sudo cryptsetup luksAddKey /dev/sda2

#A device can have many passphrases. To remove a passphrase or key from a device type this command
sudo cryptsetup luksRemoveKey /dev/sda2

```


