[return](debianinstall)

:bootableusb:

In the bios, set the sata operation of the drive you want to install
the debian operating system into, into an 'ahci' if it's set from ‘raid on’

In debian installer's auto partitioning, select 

"guided - use entire disk"

“select all files in one partition (recommended for new users)”

An overview of the auto partioning done will then be displayed

Create a manual [esp](esp) partition
Create a manual [root](root) partition
Create a manual [swap](swap) partition
Create a [home](home) partition
[Reinstalling](Reinstalling) debian while keeping the home partition






