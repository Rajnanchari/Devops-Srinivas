### What happens when we turn on computer?

    The power supply sends electricity to the components of the computer, such as the motherboard, hard drive, and fans.
    The BIOS (basic input/output system) or UEFI initializes and performs a power-on self-test (POST), which checks the basic hardware components to ensure they are working properly. If any issues are detected, error messages may be displayed.
    The operating system (OS), such as Windows or macOS, is loaded from the hard drive or another storage device into the computer’s RAM (random access memory).
    The OS then initializes its own components and drivers and presents the login screen or desktop environment to the user.

    An overview of the boot process  


### What is Linux 
   Linux is an open source operating system modelled on Unix, and deveoped in c language.

### Feature og linux:

  .Linux is open-source
  .Significantly reduces the monitoy cost
  .Hugh base of developers that freely provide support 
  .It is Reliable as it runs smonthly and no need to reboot it repeatly.
  .licensing freedom to re-use and re-publish the code 
  .can be customized if you wanted to change your systems look

### Run level in Linux
  Level 0: System Halt.
  Level 1: Single user mode.
  Level 2: Full multiuser mode without network.
  Level 3: Full multiuser mode with network.
  Level 4: user definable.
  Level 5: Full multiuser mode with network and X display manager.
  Level 6: Reboot.

### GNU
    GNU stands for GNU's Not UNIX. It is a Unix-like operating system, but unlike Unix, it is free software and contains no Unix code

    The name GNU is a recursive acronym, chosen because GNU's design is Unix-like, but it differs from Unix by being free software and containing no Unix code


### Linux File Systems: 

1) ext (Extended File System): 
Implemented in 1992, it is the first file system specifically designed for Linux. It is the first member of the ext family of file systems.

2) ext2: 
The second ext was developed in 1993. It is a non-journaling file system that is preferred to be used with flash drives and SSDs. It solved the problems of separate timestamp for access, inode modification and data modification. Due to not being journaled, it is slow to load at boot time.

3) Xiafs: 
Also developed in 1993, this file system was less powerful and functional than ext2 and is no longer in use anywhere.

4) ext3: 
The third ext developed in 1999 is a journaling file system. It is reliable and unlike ext2, it prevents long delays at system boot if the file system is in an inconsistent state after an unclean shutdown. Other factors that make it better and different than ext2 are online file system growth and HTree indexing for large directories.

5) JFS (Journaled File System):
First created by IBM in 1990, the original JFS was taken to open source to be implemented for Linux in 1999. JFS performs well under different kinds of load but is not commonly used anymore due to the release of ext4 in 2006 which gives better performance.

6) ReiserFS: 
It is a journal file system developed in 2001. Despite its earlier issues, it has tail packing as a scheme to reduce internal fragmentation. It uses a B+ Tree that gives less than linear time in directory lookups and updates. It was the default file system in SUSE Linux till version 6.4, until switching to ext3 in 2006 for version 10.2.

7) XFS: 
XFS is a 64-bit journaling file system and was ported to Linux in 2001. It now acts as the default file system for many Linux distributions. It provides features like snapshots, online defragmentation, sparse files, variable block sizes, and excellent capacity. It also excels at parallel I/O operations.

8) SquashFS: 
Developed in 2002, this file system is read-only and is used only with embedded systems where low overhead is needed.

9) Reiser4: 
It is an incremental model to ReiserFS. It was developed in 2004. However, it is not widely adapted or supported on many Linux distributions.

10) ext4: 
The fourth ext developed in 2006, is a journaling file system. It has backward compatibility with ext3 and ext2 and it provides several other features, some of which are persistent pre-allocation, unlimited number of subdirectories, metadata checksumming and large file size. ext4 is the default file system for many Linux distributions and also has compatibility with Windows and Macintosh.

11) btrfs (Better/Butter/B-tree FS): 
It was developed in 2007. It provides many features such as snapshotting, drive pooling, data scrubbing, self-healing and online defragmentation. It is the default file system for Fedora Workstation.

12) bcachefs: 
This is a copy-on-write file system that was first announced in 2015 with the goal of performing better than btrfs and ext4. Its features include full filesystem encryption, native compression, snapshots, and 64-bit check summing.

13) Others:
 Linux also has support for file systems of operating systems such as NTFS and exFAT, but these do not support standard Unix permission settings. They are mostly used for interoperability with other operating systems.

### Understanding the Linux Folder Structure

The Linux directory structure is organized in a hierarchical manner, starting from the root directory /. This structure is defined by the Filesystem Hierarchy Standard (FHS), which ensures consistency across different Linux distributions

### Root Directory (/)

The root directory is the top-level directory in the Linux filesystem. All other directories and files are located under this directory. It is similar to the C:\ drive in Windows, but without drive letters

/bin - Essential User Binaries

This directory contains essential command binaries that are required for the system to function, such as ls, cp, and mv. These binaries are accessible by all users

/boot - Boot Files

The /boot directory contains the files needed to boot the system, including the Linux kernel and boot loader configuration files

/dev - Device Files

This directory contains special files that represent devices. For example, /dev/sda represents the first SATA drive. These are not actual files but virtual files that provide an interface to hardware devices

/etc - Configuration Files

The /etc directory contains system-wide configuration files. These files can be edited to configure the system and its services

/home - User Home Directories

The /home directory contains personal directories for each user. For example, the user alice would have a home directory at /home/alice. This directory stores user-specific files and settings


/lib - Essential Shared Libraries

This directory contains shared libraries needed by the binaries in /bin and /sbin. These libraries are similar to DLL files in Windows

/mnt and /media - Mount Points

The /mnt directory is used for temporarily mounting filesystems, while /media is used for automatically mounting removable media such as USB drives and CDs


/opt - Optional Software

The /opt directory is used for installing third-party software that is not included in the distribution's package manager

/proc - Process and Kernel Files

This directory contains virtual files that provide information about the system and running processes. For example, /proc/cpuinfo contains information about the CPU

/root - Root User's Home Directory

This is the home directory for the root user. It is separate from the root directory /

/sbin - System Binaries

This directory contains essential system binaries that are generally intended to be run by the root user for system administration

/tmp - Temporary Files

The /tmp directory is used for storing temporary files. These files are usually deleted when the system is restarted

/usr - User Binaries and Read-Only Data

The /usr directory contains user binaries, libraries, documentation, and source code. It is further divided into subdirectories such as /usr/bin for user commands and /usr/lib for libraries

/var - Variable Data Files

This directory contains files that are expected to grow in size, such as log files, mail spools, and caches

Understanding the Linux directory structure is crucial for effectively navigating and managing the filesystem, locating important configuration files, and accessing system information


### Architure of Linux 

