Permissions

- rwx r-x r--
│ │   │   │
│ │   │   └── Others
│ │   └────── Group
│ └────────── Owner (User)
└──────────── File Type

File types can be 
regular (-) , directory(d) , symbolic (l) , character device (c), block device (b), named pipe (p), socket (s)

permission bits 
read→4 ,means can view the file
write→2 , able modify or delete the file(subject to directory permissions)
execute→1 ,able to run the file
No permission→0

we can add permission in couple of ways
Symbolic→by using letters with chmod
Numberic(octal) mode→using numbers with chmod
to add every permission to everyone
    chmod a+x file.sh  (a⇒all ; g⇒group; u⇒user , o⇒other)
    chmod 777 file.sh

Change file owner by using
    sudo chown user file
    sudo chown user:group file
    recursivly
        sudo chown -R user file/ 
        sudo chown -R alice:developers project/
    

to only change the group→sudo chgrp gpname file

inorder to set default permissions for newly created files and directories
    umask
    umask 755

only the file owner or root can delete their files
    using sticky bit
    chmod +t file

to check ownership details→ls -l


to show the current user→whoami
execute a command as root→sudo
to get the detailed information about a file→stat  {stat file.txt}
to show permissions of every dir in a path→namei {namei -l path}
inorder to display ACLs→getfacl
to show user id , group id , group→id
show group of the current user→groups
