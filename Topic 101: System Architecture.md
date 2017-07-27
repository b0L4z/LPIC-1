# LPIC-1
## Linux+ and LPIC-1: System Administrator
### Topic 101: System Architecture

#### 101.1 Determine and configure hardware settings

##### Weight: 2

Description: Candidates should be able to determine and configure fundamental system hardware.

Key Knowledge Areas:

Tools and utilities to list various hardware information (e.g. lsusb, lspci, etc.)
Tools and utilities to manipulate USB devices
Conceptual understanding of sysfs, udev, dbus
The following is a partial list of the used files, terms and utilities:

/sys/
/proc/
/dev/
modprobe
lsmod
lspci
lsusb
 

#### 101.2 Boot the system

##### Weight: 3

Description: Candidates should be able to guide the system through the booting process.

Key Knowledge Areas:

Provide common commands to the boot loader and options to the kernel at boot time
Demonstrate knowledge of the boot sequence from BIOS to boot completion
Understanding of SysVinit and systemd
Awareness of Upstart
Check boot events in the log files
Terms and Utilities:

dmesg
BIOS
bootloader
kernel
initramfs
init
SysVinit
systemd
 

#### 101.3 Change runlevels / boot targets and shutdown or reboot system

##### Weight: 3

Description: Candidates should be able to manage the SysVinit runlevel or systemd boot target of the system. This objective includes changing to single user mode, shutdown or rebooting the system. Candidates should be able to alert users before switching runlevels / boot targets and properly terminate processes. This objective also includes setting the default SysVinit runlevel or systemd boot target. It also includes awareness of Upstart as an alternative to SysVinit or systemd.

Key Knowledge Areas:

Set the default runlevel or boot target
Change between runlevels / boot targets including single user mode
Shutdown and reboot from the command line
Alert users before switching runlevels / boot targets or other major system events
Properly terminate processes
Terms and Utilities:

/etc/inittab
shutdown
init
/etc/init.d/
telinit
systemd
systemctl
/etc/systemd/
/usr/lib/systemd/
wall
