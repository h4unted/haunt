[return](bootableusb)

:esp:

If you are using a uefi boot mode, set a bootable esp partition for uefi at 536.9mb

Delete auto created esp partition
(efi system partition) (efi=extensible firmware interface)
Select free space and select continue
Select new partition and select continue
Type '536.9 mb' for esp partition
Select beginning. 

(A bios boot mode system will promt primary 
or logical selection, in bios boot mode 
select primary only for root partition
and make the root partion bootable
while keeping the rest non bootable)

(In eufi boot mode system, only the
esp partition should be bootable)

\

For esp partition,

name: esp
use as: esp (efi system partition)

bootable flag: on

\


Note: If you are using a bios boot mode, you will need to install a grub-pc boot loader for bios, to the master boot record, at the optional installation later 
(and choose the hardrive from which you want to install that grub-pc boot loader)

Note: setting up uefi on the other hand, automatically installs a grub-efi-amd64

Delete the created root partition
swap partion and home partition

A unified free disk partition will then appear
then manually create the following 3 partitions from it.
(method under tree)
