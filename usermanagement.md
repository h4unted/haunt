[return](users)

:usermanagement:

```sh

# useradd userdel usermod are commands that should be done with flag options

# adduser deluser are not commands but are pearl scripts that already have interactive flag options

# fio
# mume
su - root


# type root password
# rure
usermod -aG sudo username
exit


# mume
sudo useradd -m username
sudo passwd username
sudo groupadd group
sudo usermod -a -G username group
sudo chown username -R /home/username/folder/
sudo setfacl -m g:username:rwx -R


# change username
sudo usermod -l newname oldname

#changing the home directory of the new username
#-d represents the path to the new home directory and -m copies the contents of the old home directory in to the new home directory_at the end of the command you must simply specify the user
sudo usermod -d /home/meltdown -m meltdown

# To delete a user, first kill all its processes.
sudo killall -9 -u user 
exit

# The killall command kills a process name and all pid(s) associated with that process name
# and the -u flag limits it. The -u sets it to delete only all processes which that user owns.
# The kill command only kills a scpecific process id.
# https://linuxhint.com/kill-all-user-processes-linux/

# Both killall and kill have numerated optional flags on how they kill the process whether
# abruptly or orderly. You can list them all by typing kill -l.

# And they are such as  (-9 sigkill) or (-15 sigterm)  
 

# The -r flag for the userdel command only removes the home directory contents of the user
# and not all files of the use on the system. That is the limit of the userdel command.
sudo userdel -r username

# This command removes the user and all files of the user throughout the system.
sudo deluser --remove-all-files --remove-home user

# to remove a user and all its files that already have been removed.
# if you have not inserted the --remove-all-files flag when deleting a user
# add a new user with that deleted users uid for example 1001
# and then you can delete that user with such a flag.
# You can then delete the home directory for that user.
sudo adduser --uid 1001 user
sudo deluser --remove-all-files user
sudo rm -r /home/username

# to find a user and delete all its files
# to query for the uid of the user
# to insert that uid within the first command
find / -user xxx -delete
stat -c %u /home/user/
find / -user $(stat -c %u /home/user/) -delete

```



