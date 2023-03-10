[return](bootableusb)

:swap:

select free space and select continue
select new partition and select continue
type (1.5 x 8gb to 64gb ram size) for swap partition
select beginning. 

(a bios boot mode system will promt primary 
or logical selection, in bios boot mode 
select primary only for root partition
and make the root partion bootable
while keeping the rest non bootable)

(in eufi boot mode system, only the
esp partition should be bootable)

\

For swap partition;

name: swap
use as: swap area

bootable flag: off

\


done setting up partition
select continue








