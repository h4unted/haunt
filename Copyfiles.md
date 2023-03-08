[return](filesystem)

:copyfiles:

```sh

# copy files in the current directory to some directory
cp a.txt b.txt c.txt /home/atlas/backup/
sudo cp /a/b/file /a/b/file.bak

# Will copy the file from USER1 to USER2, and then change the owner of the copy in /home/USER2 to USER2
sudo cp /home/USER1/FNAME /home/USER2/FNAME && sudo chown USER2:USER2 /home/USER2/FNAME

# –v  verbose: shows the progress of multiple copied files
# –p  preserve: keeps the same attributes, like creation date and file permissions
# –f  force: force the copy by deleting an existing file first
# –i  interactive: prompts for confirmation, highly advised
# –R recursive: copies all files and subfolders in a directory
# –u update: copy only if source is newer than destination

```



