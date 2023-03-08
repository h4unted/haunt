[return](linuxguide)

:package:

```sh

# Intalling using apt or the advanced package tool will install
# the software on all users and often times it is needed to 
# run shell with root user privileges to by typing sudo to be able 
# to run the following command
apt-get install 

# or 
apt install

#to install a .deb file first you have to download it's tar.gz compressed
#installer. then you must extract it with this command
tar -xvzf compinstaller.tar.gz
#x – instructs tar to extract the files from the zipped file
#v – means verbose, or to list out the files it’s extracting
#z – instructs tar to decompress the files – without this, you’d have a folder full of compressed files
#f – tells tar the filename you want it to work on

# installing by download link only using wget and extraction using tar will only install on current user only 
# To install and remove a .deb package type the following
sudo dpkg -i package_file.deb
sudo apt-get remove package_name

```

Package installation [confirmation](confirmation)

