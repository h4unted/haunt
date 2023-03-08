[return](filesystem)

:findingfiles:

```sh

# To find files in bash terminal, first go at the directory where the 
# starting directory is then type
# mume
find ~/startingdir/ -iname file*
find ~/startingdir -iname file*
find ~/startingdir -iname file*.exe
find ~/stratingdir -iname file* | awk '/word/'  
find ~/stratingdir -iname file* | awk '{print $0}'   

# To find a directory
sudo find / -type d -name "directory"

```








