[return](grub)

:grubconfiguration:

```sh

# first backup grub

sudo cp /etc/default/grub /etc/default/grub.bak


# Have a visual on and edit grub
# mume


cat /etc/default/grub

vim /etc/default/grub



# update the grub.cfg in debian
# mume

sudo update-grub



# to update the grub.cfg when creating a boot menu with a different name or path
# mume 

sudo grub-mkconfig –o /boot/grub/grub.cfg


# GRUB_TIMEOUT: The time in seconds after the menu is displayed to boot the default entry, unless a key is pressed. The default is 5. Set to 0 to boot immediately without displaying the menu, or to -1 to wait indefinitely.

# GRUB_DISTRIBUTOR: Set by distributors of GRUB and is used to generate more informative menu entry titles. The example evaluates to CentOS Linux Server.

# GRUB_DEFAULT The default menu entry to boot. A value of 0 boots the first menuentry. A value of 1 boots the second menuentry. A value of saved instructs GRUB 2 to load the last successfully loaded operating system.

# (Even though GRUB 2 is installed on your computer, the grub2-mkconfig command may not be available in your favorite Linux distribution. But the grub-mkconfig command may be available in your Linux distribution. There is no difference between grub-mkconfig and grub2-mkconfig if GRUB 2 is installed.

# Note that, if you have GRUB legacy installed, then grub-mkconfig and grub2-mkconfig commands will not be the same)

```



