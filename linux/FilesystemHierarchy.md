Filesystem Hierarchy

- in linux everthing is treated as a file whether its driver , software , external drives , hardware devices
  
  
Core directories
- /→reps the root of the file system ; everything is inside of it
- /home , /root→home directory of user , root user
- /bin→all the commands like ls, cp , mv, mkdir are inside of this 
- /sbin→Sys admn commands like mount , reebot , fdisk are inside of this
- /etc→this is where they store the system configuration like passwd, hosts, user
- /var→inside this there will be variable data like logs , caches, database
- /usr→applications , manuals and libraries are present here
- /opt→all the 3rd softwares which are installed in the system will be present here
- /boot→bootloader files are located here such as grub, kernal
- /dev→device file like sda 
- /proc→process and kernal info
- /sys→kernal / device info
- /media→removable drives are shown here
- /mnt→manual mount point (temporary mounts)
- /run→contains the details of runtime pcs data like pid files , sockets
- /srv→server datas like web or ftp server data
- /lib→stores essential shared libraries which are needed by bin and sbin
  
Important Files
- /etc/passwd→user accounts
- /etc/shadow→passwords in encrypted form
- /etc/group→groups
- /etc/hosts→System hostname
- /etc/fstab→filesystem mount configuration
- /var/log/syslog→System logs (ubuntu)
- /proc/cpuinfo→CPU Info
- /proc/meminfo→memory info
  
Path Types
- Absolute path→which starts from /  
- Relative path→which starts from the current directory
  
Navigation Commands
- ls→to list directories
- ls -l→detailed listing
- ls -la→shows hidden file
- cd→to change directory
- cd /→go to root
- cd ..→go back one directory
- cd - / cd ~→goes back to home directory of the user
- tree→display directory tree
  
File Operation Commands
- touch→to create files
- mkdir→to create directories
- cp→to copy file {cp a.txt b/a.txt}
    - cp -r  dir1 dir2→to copy directory
- mv→to rename or move a file
- rm→to remove file {rm file.txt}
    - rm -r→to remove directories {rm -r file}
  
Viewing Files
- cat→to show whats inside the file
- head / tail→for lines from top or bottom
    - head file.txt 
    - tail file.txt 
    - tail -5 logfile.log ⇒ shows last 5 lines
- nano→text editor
  
Searching
- locate→prebuilt database instead of scanning the disk
    locate notes.txt
    runs with the help of prebuilt databse 
    sometimes databse may be outdated ; inorder to keep it updated→sudo updatedb
    fast
- which→shows which executable will run 
    finds where a command is installed
- whereis→used to find binaries,source,man page 
    unlike which gives multiple locations
- find→search files and directories filters can be add like size type and all
    - to search by name→find /dir -name "file name" 
    - to find by type→find /dir -name "*.zip"
    - to find larger files→find / -size +100M  {for over 100mb files}
    - for directories onlu→find /dir -type d
      
    - Extremely powerful
    - Always up to date
    - Can search by name, size, owner, permissions, date, etc.
    - Can be slow on large disks.
  
Disk Usage
- display disk usage for mounted filesystem→df -h
- inorder to show total size of a specific folder→du -sh folder
    - s⇒summary only
    - h⇒human readable form
- to show size of every file and directory→du -ah
    - a⇒includes files as well as directory
    - h⇒human readable form
