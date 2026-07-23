Level 0
--------------
ssh - network protocol which connects another computer over network, its encrypted , standard tool for remote linux administration , which runs in port 22
ssh [options] user@host

connected to bandit0@bandit.labs.overthewire.org on port 2220
ssh -p 2220 bandit0@bandit.labs.overthewire.org

got password from the readme file ⇒ 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR

Level 1
---------------
using this password got from the bandit0 we have to login into bandit1
With no FILE, or when FILE is -, read standard input
in this case we got the file name as -
cat ./-
and got the key for bandit2 ⇒ PK8fYLZg2hnHSz83plBL1iEPKdD3QToB

Level 2
---------------
there a text file in which lots of space inbetween the letter
--spaces in this filename--

to read this 
cat ./'--spaces in this filename--'
got key for bandit3 ⇒ 7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME

Level 3
---------------
in this key for next level is stored inside a hidden text file inside inhere directory

inorder to access the key
cat ./'...Hiding-From-You'

got key for bandit4 ⇒ xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq

Level 4
---------------
After logging inside inhere directory there were several files from it by trail and error method went through files and got the key from -file07
cat ./'-file07'
Key ⇒ 6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG

Level 5
----------------
got logged in 
there where many files in it inside it too
so i had to find using filters like size and type since there is no file extension
find ./ -size 1k -type f 
but the size was 1033bytes 
so i had to use 
find ./ -size 1033c -type f
here c denotes bytes (k - kb , m-mb , g-gb,
then using cat displayed contents from it if the permission does not contain execution
got key from maybehere07/'.file2'
key ⇒ pXa26xhMWaC2SvDotA4r9EgZkulOeSBW

Level 6
-----------------
inorder to search the entire system we have to start from the root folder
find / -size 33c -user bandit7 -group bandit6
cat /var/lib/dpkg/info/bandit7.password
and got key ⇒ Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3 

Level 7
-----------------
using cat and grep got the key 
cat data.txt | grep millionth
Key  ⇒ VR1ljMayciFxbnUokuQmJFw6QC9VKtub

Level 8
-----------------
by using sort and uniq by piping got the uniq text from the text file
sort data.txt | uniq -u
key ⇒ EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl
