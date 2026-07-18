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
