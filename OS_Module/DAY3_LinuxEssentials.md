# Linux Essentials 

## Linux Filesystem
```
The root directory of the file system /
Everything starts from this directory. Think of it as the doorway to the Linux Filesystem


Essential user commands in /bin
Contains commands like ls and echo which every user can use.


User Directories in /home
Contains directories for every non-root user on the system (with a home directory and login shell)


Host specific system configurations in /etc
Stands for everything configurable
Contains network configurations, system services(daemons), firewall configurations, etc.


Variable data files in /var
Contains all of the system logs by default
```
### **IMPORTANT
```
YOU CAN READ FILES WITHIN A DIRECTORY EVEN IF YOU DON'T HAVE PERMISSIONS TO ACESS THE DIRECTORTY
It’s also important to understand that file permissions do not overrule directory permissions. If a user does not have read rights to a directory, it also cannot read any of its files even if the file’s permissions allow it
```
## Special Permissions: SUID and SGID
```
When an executable is ran in Linux, it runs with the permissions of the user who started it. However, SUID and SGID change that to force the executable to run as the owning user or group. These permissions are represented as s in the User or Group field of ls- l
```
## What argument/switch option, when used with man, will search the short descriptions and man-page-names for a keyword that you provide?
```
man -k
```
## Hash with largest hash possible
```
echo -n "OneWayBestWay" | sha512sum
```
## Search the user home directories to find the file with the second-most lines in it. The flag is the number of lines in the file
```
find /home/* -type f -exec wc -l {} + 2>/dev/null | sort -rn
```
## Pull the comment from etc/passwd file
```
cat /etc/passwd | cut -d: -f5
```