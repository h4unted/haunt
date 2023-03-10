[return](debianinstall)

:completefirmware:

```sh

# copy the firmware list file into the home directory
# make sure each ‘main contrib non-free’ is at the end of each line
# mume
sudo nano /etc/apt/sources.list

# mume
sudo dpkg --add-architecture i386
sudo apt-get update
sudo apt-get install dselect
sudo apt-get install $(cat ~/Firmware.list | awk '{print $1}')

```








