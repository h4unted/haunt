[return](diskmgmt)

:partition:

```sh

# You can also partition drives by doing the following, again first, all partitions by using fdisk
sudo fdisk -l

# Always remember to select the whole drive to be partitioned and not just an existing partition of the drive. In other words the whole drive should be empty or empty and already backed up. Then type,
sudo fdisk /dev/sdb

# To create an empty gpt partition
g
# To create a new partition
n
# When prompted for partition number 1-128 select default 1
# When prompted for the first sector select 2048
# When promted for the last sector write +<and the number of gigabytes you wish as a partiton>G
# Print the partition table for you to review it 
p
# Write and finalize that partition table for the whole drive
w


```




