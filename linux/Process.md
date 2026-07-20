#Process

process→running instance of a program
program→a file stored on disk like /usr/bin/python3

Process Lifecycle→program ⇒ executed ⇒ running pcs ⇒finished / killed 

Process States→Running(R) , sleeping/waiting(S) , uniterruptible sleep (usually for Input out) , Stopped (T) , Zombie (Z) , idle (I)

inorder to show the currently running pcs→ps
to show all the running pcs→ps aux or ps -ef (used often in scripts and server admn)

PID→Every pcs has unique id , used to stop or insepect the pcs
you can find a pcs with the help of grep→ps aux | grep app
to get pid directly→pgrep app

for real time mointering of cpu , memory running pcs and load average we use→top (imp version is htop)

to terminate or kill a pcs→kill PID

to force kill→kill -9 PID

to kill by pcs name
    pkill app
    killall app

Signals
SIGTERM→gracefully terminate ,send by kill pid
SIGKILL→force kill , send by kill -9 pid
SIGINT→interrupt (ctrl+c)
SIGSTOP→pause pcs
SIGCONT→resume paused pcs
SIGHUP→reload configuration

inorder to suspend a running pcs→crtl+z to resume it back 'bg'
for process tree→pstree

to display parent PID→ps -ef from that youll get the ppid
to find which pcs uses a port→lsof -i 8080

to monitor cpu→uptime
to monitor memory→free -h
A zombie is a process→that has finished executing but still has an entry in the process table because its parent has not yet collected its exit status

top vs ps
    top is interactive and also useful for monitoring cpu, memory in real life ;and its live
    ps is a snapshot of a point which is non interactive and useful for scripting
