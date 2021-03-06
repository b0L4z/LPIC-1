# LPIC-1
## Linux+ and LPIC-1: System Administrator - Exam 101
### Topic 101: System Architecture

#### 101.1 Determine and configure hardware settings

#### Weight: 2

**Description:** Candidates should be able to determine and configure fundamental system hardware.

#### Key Knowledge Areas:

Tools and utilities to list various hardware information (e.g. lsusb, lspci, etc.)
Tools and utilities to manipulate USB devices
Conceptual understanding of sysfs, udev, dbus
#### The following is a partial list of the used files, terms and utilities:

* /sys/ - system harware and kernel module without process IDs
* /proc/ - files sytem that shows processes, mounts, process IDs, and hardware ids
     - /proc/interrupts - interrupts cpu to ask for permission to use system resources
     - /proc/dma - allows direct access to system resources
     - /proc/PID/environ - displays environment variables for specified PID number.
* /dev/ - lists device items
* `modprobe` add or remove modules from the Linux Kernel dpeending on the switch
     - `modprobe -r` removes a module
     - ``sudo insmod /usr/lib/modules/`uname -r`/kernel/fs/isofs/isofs.ko`` insert a module without modprobe
* `lsmod` nicely formats and lists contents of /proc/modules
* `lspci` lists device ID on PCI
     - `lspci -v` v = verbose
* `lsscsi` lists SCSI drives
     - `lsscsi -s` s = size
* `lscpu` displays cpu information
     - `lscpu -a -e=CPU` a = all e = extended
     - `lscpu -aep` p = parse
* `lsusb` shows list of devices on USB buses
* `lsblk` lists information about available or specified block devices
* `lsraid` displays any RAID disks
* `lsdev` lists all devices connected to kernel
 

#### 101.2 Boot the system

#### Weight: 3

**Description:** Candidates should be able to guide the system through the booting process.

#### Key Knowledge Areas:

Provide common commands to the boot loader and options to the kernel at boot time
Demonstrate knowledge of the boot sequence from BIOS to boot completion
Understanding of SysVinit and systemd
Awareness of Upstart
Check boot events in the log files
#### Terms and Utilities:

* Sysvinit Boot Process - **BIOS** (Basic Input/Output System executes MBR) > **MBR** (Master Boot Record executes GRUB) > **GRUB** (Grand Unified Bootloader executes Kernel) > **Kernel** (Kernel /sbin/init) > **Init** (Init executes runlevel programs) > **Runlevel** (Runlevelprograms are executed from /etc/rc.d/rc*.d/)
* Systemd Boot Process - **BIOS** (Basic Input/Output System executes MBR/GPT includes EFI) > **MBR** (Master Boot Record executes LILO/GRUB/GRUB2) > **GRUB** (Grand Unified Bootloader executes Kernel) > **Kernel** (Kernel ) > **Init** (Init executes runlevel programs) > **Runlevel** (Runlevelprograms are executed from /usr/lib/systemd/system)
* `dmesg` is used to write the kernel messages in Linux. Output location is /var/log/dmesg or /var/log/syslog
* BIOS -- 1st thing to load when powering on a machine. This then hands off to the bootsector. Boot sector provides MBR.
* bootloader -- LILO/GRUB/GRUB2 decides what you can boot. May be able to use user input to select an OS.
* kernel -- after bootloader the kernel is read and executed. Device initialization, module loading, and initial RAM (initrd) is loaded
* initramfs
* init -- program loads after kernel and becomes the first process ID.
* SysVinit -- package conatining a group of processes that control basic functions of system and runlevels seen below. Scripts are located in /etc/rc.d/
     - 0 - HALT (shutdown)
     - 1 - Single User
     - 2 - Multi-User (No Network or Remote Filesystems)
     - 3 - Full Multi-User (Including Networking and Remote Filesystems)
     - 4 - Unused
     - 5 - X11 (Full Multi-User with Graphical Desktop Environment)
     - 6 - Reboot
* systemd -- initialization system for bootstrapping the user space and managing all processes subsequent to system start. It was developed to replace sysvinit. Has fewer dependencies, allows for prioritization and precedence, and reduces start up time. Scripts for targets are located /usr/lib/systemd/system
     - 0 - poweroff.target (shutdown)
     - 1 - rescue.target (Single User/Rescue Shell)
     - 2 - multi-user.target (Non-Graphical, Full Network, Multi-User)
     - 3 - multi-user.target (Non-Graphical, Full Network, Multi-User)
     - 4 - multi-user.target (Non-Graphical, Full Network, Multi-User)
     - 5 - graphical.target (Full Multi-User with Graphical Desktop Environment)
     - 6 - reboot.target (Reboot)
* `runlevel` shows current run level

#### 101.3 Change runlevels / boot targets and shutdown or reboot system

#### Weight: 3

**Description:** Candidates should be able to manage the SysVinit runlevel or systemd boot target of the system. This objective includes changing to single user mode, shutdown or rebooting the system. Candidates should be able to alert users before switching runlevels / boot targets and properly terminate processes. This objective also includes setting the default SysVinit runlevel or systemd boot target. It also includes awareness of Upstart as an alternative to SysVinit or systemd.

#### Key Knowledge Areas:

Set the default runlevel or boot target
Change between runlevels / boot targets including single user mode
Shutdown and reboot from the command line
Alert users before switching runlevels / boot targets or other major system events
Properly terminate processes
#### Terms and Utilities:

* /etc/inittab - after init program loads inittab is read and appropriate runlevel scripts are run. Used in Sysvinit not systemd. In order to change the default runlevel for Sysvinit you must change the default runlevel by changing the number here: "id:3:initdefault"
* `shutdown` comannd to run different shutdown commands
     - `shutdown -r 30` r 30 = reboot 30 mins
     - `shutdown -h` h = halt it stops machine and advises to shutdown 
     - `shutdown -p` p=power down it turns off machine
     - `shutdown -k` k = broadcast a message similar to `wall`
     - `shutdown -c` c = cancel
* `init`similar to `telinit`
* /etc/init.d/
* `telinit` changes runlevel to specified
* systemd - a type of system with targets instead of rc.d
* `systemctl`
     - `systemctl get-default` shows default target for a systemd machine
     - `systemctl set-default graphical.target` sets default target for a systemd machine
     - `systemctl list-units --type=target` lists all targets available on system
* /etc/systemd/
* /usr/lib/systemd/ - location of systemd target in /system/
* `wall` broadcasts messages to anyone on the terminal
