[return](debianinstall)

:wifi:

```sh

#First make sure you have backed up and added <main contrib non free> on each debian repository within the /etc/apt/sources.list file

# Then check what your chipset is
lspci -nn
lspci -nn | grep Network

# add the non-free contrib lines on your apk sources.list file
# update the apk then install  the firmeware-realtek
sudo apt-get update
sudo apt-get install firmware-atheros

# then for the wifi chipset, Qualcomm Atheros QCA6174 802.11ac Wireless Network Adapter
# this is the following kernel module or driver for debian it's called:  rtl8821ae
sudo lsmod 
sudo lsmod ath10k_pci
sudo modprobe ath10k_pci

# in the end it is better to replace the wifi chipset, with an intel
# chipset, if there are no kernel modules and non-free firmware
# from debian to support it.

```
