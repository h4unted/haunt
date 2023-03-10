[return](bootableusb)

:home:

select free space and select continue
select new partition and select continue
type 'max' for home partition
after typing max, the “beginning” selection will not appear. 


(a bios boot mode system will promt primary 
or logical selection, in bios boot mode 
select primary only for root partition
and make the root partion bootable
while keeping the rest non bootable)

(in eufi boot mode system, only the
esp partition should be bootable)

\

for home partition;

name: Beta
use as: ext4 journalizing file system
mount point: /home

( mount options: defaults
label: none
reserved blocks: 5%
typical usage: standard )

bootable flag: off

\


done setting up partition
select continue

then select finish partitioning 
and write partitions in to disk. 
