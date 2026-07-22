piping/redirection

Every linux standard prgm has three standard streams→standard input (0,stdin), standard output(1,stdout) , standard error(2,stderr)

inorder to redirect an out to a file
    > , it overwrites
    >> ,to append instead of overwriting

to take an input like this we use→<
to redirect the error msgs only→2>
for both error and output redirection→command > output.txt 2>&1

linux provides a special file , anything sent there disappears→/dev/null 

We use pipes(|) to→send output of one command as the input of another , we can combine as many commands we want using this

if want to run two commands one after another we can use→&& , if its not taking any input from the prev command

exit status→every linux command returns an exit status (aka exit code) when it finishes ; inorder to check it echo $? , after running the command whose exit code is needed

why 0 considered success→in unix and linux it means no error
