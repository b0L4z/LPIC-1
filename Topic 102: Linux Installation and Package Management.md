# LPIC-1
## Linux+ and LPIC-1: System Administrator - Exam 101
### Topic 102: Linux Installation and Package Management

#### 102.1 Design hard disk layout

#### Weight: 2

**Description:** Candidates should be able to design a disk partitioning scheme for a Linux system.

#### Key Knowledge Areas:

Allocate filesystems and swap space to separate partitions or disks
Tailor the design to the intended use of the system
Ensure the /boot partition conforms to the hardware architecture requirements for booting
Knowledge of basic features of LVM
#### Terms and Utilities:

* / (root) filesystem - the root of where everything is installed. not good to have near full disk space used.
* /var filesystem - a standard subdirectory of the root directory in Linux and other Unix-like operating systems that contains files to which the system writes data during the course of its operation.
* /home filesystem - a user's home directory
* /boot filesystem - stores files necessary to boot the system.
* /opt filesystem - third party utilities
* swap space - dedicated partition for memory swap. should be at least 10% larger than the memory.
* mount points - the location where you will install different file systems. The /etc folder needs to be mounted in root.
* partitions - a seperation in a disk or set of disks to reserve space for a mount point.
* LVM (Logical Volume Manager) - Allows the creation of 'groups' of disks or partitions that can be assembled into a single (or
multiple) filesystems.
 

#### 102.2 Install a boot manager

#### Weight: 2

**Description:** Candidates should be able to select, install and configure a boot manager.

#### Key Knowledge Areas:

Providing alternative boot locations and backup boot options
Install and configure a boot loader such as GRUB Legacy
Perform basic configuration changes for GRUB 2
Interact with the boot loader
#### The following is a partial list of the used files, terms and utilities:

* GRUB (legacy) - CentOS 5 and older
     - /boot - GRUB boot volume
* GRUB2 - 
* menu.lst, grub.cfg and grub.conf
* grub-install
* grub-mkconfig
* MBR
 

#### 102.3 Manage shared libraries

#### Weight: 1

**Description:** Candidates should be able to determine the shared libraries that executable programs depend on and install them when necessary.

#### Key Knowledge Areas:

Identify shared libraries
Identify the typical locations of system libraries
Load shared libraries
#### Terms and Utilities:

* ldd
* ldconfig
* /etc/ld.so.conf
* LD_LIBRARY_PATH
 

#### 102.4 Use Debian package management

#### Weight: 3

**Description:** Candidates should be able to perform package management using the Debian package tools.

#### Key Knowledge Areas:

Install, upgrade and uninstall Debian binary packages
Find packages containing specific files or libraries which may or may not be installed
Obtain package information like version, content, dependencies, package integrity and installation status (whether or not the package is installed)
#### Terms and Utilities:

* /etc/apt/sources.list
* dpkg
* dpkg-reconfigure
* apt-get

* apt-cache

* aptitude

 

#### 102.5 Use RPM and YUM package management

#### Weight: 3

**Description:** Candidates should be able to perform package management using RPM and YUM tools.

#### Key Knowledge Areas:

Install, re-install, upgrade and remove packages using RPM and YUM
Obtain information on RPM packages such as version, status, dependencies, integrity and signatures
Determine what files a package provides, as well as find which package a specific file comes from
#### Terms and Utilities:

* rpm
* rpm2cpio
* /etc/yum.conf
* /etc/yum.repos.d/
* yum
* yumdownloader
