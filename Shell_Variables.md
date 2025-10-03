# 1. Printing variables
The challenge prompted me to print variables in terminal.

## My Solve
**Flag:** `pwn.college{EW9_FleQsALu2oAywgrKjZNo2zW.QX3UTN0wiN1kjNzEzW}`

```bash
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{EW9_FleQsALu2oAywgrKjZNo2zW.QX3UTN0wiN1kjNzEzW}
```

## What I learned
I learned how to use print variables using `echo` command.

## References
The problem statement was used as the reference
```
Now it's your turn. Have your shell print out the FLAG variable and solve this challenge!
```

# 2. Setting Variables
The challenge prompted me to store values in variables. 

## My Solve
**Flag:** `pwn.college{AVz3WJEWlWGUS_XkPiS_mre3zuM.QX5UTN0wiN1kjNzEzW}`

```bash
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{AVz3WJEWlWGUS_XkPiS_mre3zuM.QX5UTN0wiN1kjNzEzW}
```

## What I learned
I learned how to set values to variables in shell.

## References
The problem statement was used as the reference
```
To solve this level, you must set the PWN variable to the value COLLEGE. Be careful: both the names and values of variables are case-sensitive! PWN is not the same as pwn and COLLEGE is not the same as College.
```

# 3. Multi-word Variables
The challenge prompted me to store multi-word values in a variable. 

## My Solve
**Flag:** `pwn.college{0eUe6HJghsgy6NgxyxdjKk8KQKJ.QXwYTN0wiN1kjNzEzW}`

```bash
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{0eUe6HJghsgy6NgxyxdjKk8KQKJ.QXwYTN0wiN1kjNzEzW}
```

## What I learned
I learned how to use stores values containing multiple words in a variable.

## References
The problem statement was used as the reference
```
Here, the shell reads 1337 SAUCE as a single token, and happily sets that value to VAR. In this level, you'll need to set the variable PWN to COLLEGE YEAH. Good luck!
```

# 4. Exporting Variables
The challenge prompted me to export and use variables. 

## My Solve
**Flag:** `pwn.college{QYCABZHxoaHulSjwtkoj62DtvoB.QXyYTN0wiN1kjNzEzW}`

```bash
hacker@variables~exporting-variables:~$ sh
sh-5.2$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{QYCABZHxoaHulSjwtkoj62DtvoB.QXyYTN0wiN1kjNzEzW}
```

## What I learned
I learned how to export variables and use them in child shell processes.

## References
The problem statement was used as the reference
```
In this challenge, you must invoke /challenge/run with the PWN variable exported and set to the value COLLEGE, and the COLLEGE variable set to the value PWN but not exported (e.g., not inherited by /challenge/run). Good luck!
```

# 5.  Printing Exported Variables
The challenge prompted me to use `env` command. 

## My Solve
**Flag:** `pwn.college{oDTWxraukxJXRhPgpIWCi4fVcP2.QX4UTN0wiN1kjNzEzW}`

```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=b5034dc96ede2b29d47b0d3b98be601d5eb3b95cc69f124205895e21a44b4809
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{oDTWxraukxJXRhPgpIWCi4fVcP2.QX4UTN0wiN1kjNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

## What I learned
I learned how to use `env` to see list of exported variables.

## References
The problem statement was used as the reference
```
Try the env command: it'll print out every exported variable set in your shell, and you can look through that output to find the FLAG variable!
```

# 6. Storing command output
The challenge prompted me to store command output in a variable. 

## My Solve
**Flag:** `pwn.college{gkeUjWY68ATpc5Makbx_TGoxGYE.QX1cDN1wiN1kjNzEzW}`

```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{gkeUjWY68ATpc5Makbx_TGoxGYE.QX1cDN1wiN1kjNzEzW}
```

## What I learned
I learned how to store a command's output in a variable and print it.

## References
The problem statement was used as the reference
```
In preparation for more complex levels, we want you to:

Neat! Now, you practice. Read the output of the /challenge/run command directly into a variable called PWN, and it will contain the flag!
```

# 7. Reading Input
The challenge prompted me to read input. 

## My Solve
**Flag:** `pwn.college{Qx1CUtyWcTGXgU5qI9BY4dEa6DB.QX4cTN0wiN1kjNzEzW}`

```bash
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Qx1CUtyWcTGXgU5qI9BY4dEa6DB.QX4cTN0wiN1kjNzEzW}
```

## What I learned
I learned how to read input using shell and store it in a variable.

## References
The problem statement was used as the reference
```
In this challenge, your job is to use read to set the PWN variable to the value COLLEGE. Good luck!
```

# 8. Reading Files
The challenge prompted me to read from file. 

## My Solve
**Flag:** `pwn.college{4iy7-4JKSfJL5FTo8Oj77aE5pdE.QXwIDO0wiN1kjNzEzW}`

```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{4iy7-4JKSfJL5FTo8Oj77aE5pdE.QXwIDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use use `<` to read from a file directly and store in a variable.

## References
The problem statement was used as the reference
```
What happened there? The example redirects some_file into the standard input of read, and so when read reads into VAR, it reads from the file! Now, use that to read /challenge/read_me into the PWN environment variable, and we'll give you the flag! The /challenge/read_me will keep changing, so you'll need to read it right into the PWN variable with one command!
```
