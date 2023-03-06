[return](commands)

:diagnostic:

# dxdiag
is technically a tool for troubleshooting DirectX, which has no direct Linux equivalent. However, there are a number of diagnostic tools in Linux to use when finding things out about the system.

# lshw  
is a tool that will scan the system and list out all hardware devices based on the diagnostic responses the equipment is designed to output.

# lspci 'and' lsusb  
are specific to the PCI and USB buses, respectively, and list out the hardware attached to those buses.

# ps 
is a program that will show a list of all running processes. With commandline switches, you can determine if it’s limited to that terminal, limited to those launched by your user, or everything on the system.

# top 
is similar to ps, as it lists processes, but it shows a regularly-updating list of processes sorted by their CPU usage.

[lm_sensors](lm_sensor) 
is a program that will show the state of the system’s temperature monitors, power levels, and fan speeds.

# df 
is a tool that tells, at a glance, how much free space your hard drive(s) have, as well as their total amounts, where they’re mounted, and how full they are (including a percentage).

Most of the OS-specific properties are not readily accessible by a program (or, at least, not by any standard all-in-one tool), but can be accessed by reading files in the /proc and /sys directory structures. For example, by reading /proc/cpu, you get a pretty exhaustive list of the CPU features on your system, while /proc/version gives you the detailed version of the Linux kernel, usually including the time it was compiled, the user who compiled it, and what compiler was used to compile it.

```
