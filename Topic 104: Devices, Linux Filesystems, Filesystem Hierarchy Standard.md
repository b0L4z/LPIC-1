# LPIC-1
## Linux+ and LPIC-1: System Administrator - Exam 101
Topic 104: Devices, Linux Filesystems, Filesystem Hierarchy Standard

104.1 Create partitions and filesystems

Weight: 2

Description: Candidates should be able to configure disk partitions and then create filesystems on media such as hard disks. This includes the handling of swap partitions.

Key Knowledge Areas:

Manage MBR partition tables
Use various mkfs commands to create various filesystems such as:
ext2/ext3/ext4
XFS
VFAT
Awareness of ReiserFS and Btrfs
Basic knowledge of gdisk and parted with GPT
Terms and Utilities:

fdisk
gdisk
parted
mkfs
mkswap
 

104.2 Maintain the integrity of filesystems

Weight: 2

Description: Candidates should be able to maintain a standard filesystem, as well as the extra data associated with a journaling filesystem.

Key Knowledge Areas:

Verify the integrity of filesystems
Monitor free space and inodes
Repair simple filesystem problems
Terms and Utilities:

du
df
fsck
e2fsck
mke2fs
debugfs
dumpe2fs
tune2fs
XFS tools (such as xfs_metadump and xfs_info)
 

104.3 Control mounting and unmounting of filesystems

Weight: 3

Description: Candidates should be able to configure the mounting of a filesystem.

Key Knowledge Areas:

Manually mount and unmount filesystems
Configure filesystem mounting on bootup
Configure user mountable removable filesystems
Terms and Utilities:

/etc/fstab
/media/
mount
umount
 

104.4 Manage disk quotas

Weight: 1

Description: Candidates should be able to manage disk quotas for users.

Key Knowledge Areas:

Set up a disk quota for a filesystem
Edit, check and generate user quota reports
Terms and Utilities:

quota
edquota
repquota
quotaon
 

104.5 Manage file permissions and ownership

Weight: 3

Description: Candidates should be able to control file access through the proper use of permissions and ownerships.

Key Knowledge Areas:

Manage access permissions on regular and special files as well as directories
Use access modes such as suid, sgid and the sticky bit to maintain security
Know how to change the file creation mask
Use the group field to grant file access to group members
Terms and Utilities:

chmod
umask
chown
chgrp
 

104.6 Create and change hard and symbolic links

Weight: 2

Description: Candidates should be able to create and manage hard and symbolic links to a file.

Key Knowledge Areas:

Create links
Identify hard and/or soft links
Copying versus linking files
Use links to support system administration tasks
Terms and Utilities:

ln
ls
 

104.7 Find system files and place files in the correct location

Weight: 2

Description: Candidates should be thoroughly familiar with the Filesystem Hierarchy Standard (FHS), including typical file locations and directory classifications.

Key Knowledge Areas:

Understand the correct locations of files under the FHS
Find files and commands on a Linux system
Know the location and purpose of important file and directories as defined in the FHS
Terms and Utilities:

find
locate
updatedb
whereis
which
type
/etc/updatedb.conf
