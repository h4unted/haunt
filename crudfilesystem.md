[return](filesystem)

:crudfilesystem:

```sh

# creates a directory in the current location
mkdir directoryname

# creates multiple directories in the current location. Do not use spaces inside {}
mkdir {dir1,dir2,dir3,dir4}

# creates a directory structure with the missing parent directories (if any)
mkdir –p directory/path/newdir

# creates a directory and sets full read, write, execute permissions for all users
mkdir –m777 directory_name

# creates a directory in the current location
mkdir –v directory_name(s)

# delete a non-empty directory without any prompts
sudo rm -rf directory

# delete an empty directory
sudo rm -d directory

# cut or move a file from one directory to the other
mv source_directory/file dest_directory/file

# rename a file (source and destination directory
# must only be on the same directory)
mv previous_filename new_filename

```




