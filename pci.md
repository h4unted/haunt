[return](debianinstall)

:pci:

```sh

#to look for detected pci devices, sound cards, video cards or network cards installed type this command.
sudo lspci

#or
# -i = ignore case
sudo lspci | grep -i network

#after finding the slot number, you can also look for the device information attached to that slot number. including the device number of that pci device
#this command also prints out the kernel module and kernel driver and slot number of that pci device.
#-v = verbose, -n = device number, -s slot number
sudo lspci -vns 03:00

#it is also possible to look for the pci device through its device number, for example 03:00.0 0280: 168c:003e (rev 32) 3:00 is the slot number and 168c:003e is the device number
sudo lspci -vnd 168c:003e

#to look for firmare and kernel module errors related to such pci device type this command 
#it prints out  kernel buffer related messages
sudo dmesg | grep ath10k

```
