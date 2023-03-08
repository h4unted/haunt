[return](grub)

:grubbootorder:


```sh

#mume

efibootmgr

sudo efibootmgr --bootorder 0003,0000,0004,0005

sudo efibootmgr --bootnum 0000 --inactive

```
