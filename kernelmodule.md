[return](debianinstall)

:kernelmodule:

```sh

sudo modprobe ath10k_pci

# When the proper firmware .bin file or binary files have been found, downloaded and extracted, for a particular pci device, simply copy them in to the usr/lib/firmware folder. then update the kernel modules for those firmwares using this command.
sudo /usr/sbin/modprobe ath10k_pci

```
