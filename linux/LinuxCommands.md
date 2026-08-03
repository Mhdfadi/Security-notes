
ssh
    securely connect to a remote machine 
    ssh user@host

ls
    to list files and directories
    ls -l ⇒ for detailed list
    ls -a ⇒ for hidden files
    ls -R ⇒ for recurssive
    ls -lh ⇒ detailed in human readable size

cd
    inorder to change directory
    cd ..  (backward only as per str)or cd - (both sides)⇒ prev directory
    cd ~ ⇒ goes to home directory of the user
    cd / ⇒ goes to root directory

cat
    inorder to view the file
    cat file.txt

file
    gives which type of file it is (jpeg image, ascii text ...)
    file filname

du
    to show disk usage
    du -sh folder ⇒ disk usage of a folder {s=summary,h=human readable}
    du -ah ⇒ disk usage of all files and folders {a=all,h=human readable}

find
    to find files ; can also use filters like type , size ,permission
    find . -name "secret.txt"
    find . -type f -size +1M  {f⇒file}
    find . -perm 644
    find . -type d -name "backup" {d⇒dir}
