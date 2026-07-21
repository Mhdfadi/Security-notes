piping/redirection

Every linux standard prgm has three standard streams→standard input (0,stdin), standard output(1,stdout) , standard error(2,stderr)

inorder to redirect an out to a file
    > , it overwrites
    >> ,to append instead of overwriting

to take an input like this we use→<
to redirect the error msgs only→2>
for both error and output redirection→command > output.txt 2>&1

linux provides a special file , anything sent there disappears→/dev/null 
