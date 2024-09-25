# File structure hierachy
The Linux file system hierarchy is organized in a tree-like structure where everything is stored under a single root directory, /.


/
├── bin
├── boot
├── dev
├── etc
├── home
├── lib
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── srv
├── sys
├── tmp
├── usr
└── var

1.  ## / (Root Directory)
  The root directory is the top of the file system hierarchy.
  Only the root user (superuser) has full control over the root directory.

   ## 2. /bin (User Binaries)
  . Contains essential binary executables (programs) needed to boot and run the system.
  .   Commands like ls, cp, mv, cat, echo, etc., are stored here.

  3. ## /boot (Boot Loader Files)
 Stores files needed to boot the system, such as the Linux kernel, bootloader (like GRUB), and other necessary files.

 4. ## /dev (Device Files)
Contains special files representing device nodes. Every hardware device (disk, USB, etc.) is represented here, for example, /dev/sda for hard drives.

5. ## /etc (Configuration Files)
.Contains system-wide configuration files for applications and services.
.Example: /etc/passwd for user account information, /etc/fstab for file system mount information.

6.  ## /home (Home Directories)
.Contains the home directories of all users except the superuser (root). For example, the home directory of user alice would be /home/alice.
.Users store personal files and configurations here.

7. ## /lib (Shared Libraries)
Contains essential shared libraries (similar to DLLs in Windows) needed by binaries in /bin and /sbin.

8. ## /media (Removable Media)
. Mount point for removable media such as USB drives, CDs, DVDs, and external hard drives. When you insert a USB stick, it may be mounted automatically under /media/username/.

9. ## /mnt (Mount Directory)
. Temporary mount point for manually mounted file systems, often used for network shares, or extra disks mounted by the system administrator.

10. ## /opt (Optional Software)
. Used to install optional software packages that are not part of the default installation.
. Third-party software often resides here, such as /opt/application/.

11. ## /proc (Process Information)
. A virtual file system containing information about system processes and kernel parameters.
. For example, /proc/cpuinfo contains details about the CPU, and /proc/meminfo provides memory information.

12. ## /root (Root User’s Home Directory)
. The home directory for the root user. It's separate from /home and is stored directly under / to give the superuser direct access to the system.

13. ## /run (Runtime Variable Data)
. Stores information about the system runtime, such as process IDs (PIDs) and system state information.

14. ## /sbin (System Binaries)
. Contains essential binaries that are used for system administration tasks (commands typically used by the root user).
. Examples include ifconfig, reboot, fdisk, and iptables.

15. ## /srv (Service Data)
. Contains data for services provided by the system, such as web servers or FTP servers.
. Example: A web server might serve files from /srv/www.

16. ## /sys (System Information)
. A virtual file system that provides information about the kernel and hardware devices attached to the system, similar to /proc.

17. ## /tmp (Temporary Files)
. Temporary files are stored here by applications and users.
. Files in /tmp are often deleted on system reboot to free up space.

18. ## /usr (User Programs)
. Contains user-installed software and utilities. This is often the largest directory in the system.

. /usr/bin: Non-essential user commands and binaries.

. /usr/sbin: Non-essential system binaries.

. /usr/lib: Libraries for programs in /usr/bin and /usr/sbin.

. /usr/local: Locally installed software (user-specific installations).

19. ## /var (Variable Data Files)
. Contains files that are expected to grow in size over time, such as logs, caches, and temporary files.

. /var/log: System and application log files.

. /var/tmp: Temporary files that should persist across reboots.

. /var/lib: State information, like package databases and service data.



## Cat command
. The cat (short for concatenate) command is used to display the contents of a file or combine multiple files. It does not number the lines by default.

Example:

    cat filename.txt
    This is line 

    This is line 

    This is line 

## nl Command

. The nl (number lines) command is similar to cat but adds line numbers to the output by default.

Example:
     ### nl filename.txt
         
     1 This is line
     
     2 This is line 
     
     3 This is line 

## Key difference

. cat: Displays the file content as is, without line numbers.

. nl: Adds line numbers to each line in the output.

### cat with -n Option

. If you want to number lines using cat, you can use the -n option, which functions similarly to nl.

### cat -n filename.txt
     1  This is line 
     2  This is line 
     3  This is line 
## Summary:
. cat filename.txt: Displays file contents without line numbers.

. cat -n filename.txt: Displays file contents with line numbers.

. nl filename.txt: Displays file contents with line numbers by default.












