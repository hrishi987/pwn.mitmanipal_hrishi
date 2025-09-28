# 1. Learning From Documentation
The challenge prompted me to get accustomed to reading the documentation. 

## My Solve
**Flag:** `pwn.college{EYh2HjZrxyw2Vvo1oKCPImg3MIt.QX0ITO0wiN1kjNzEzW}`

```bash
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{EYh2HjZrxyw2Vvo1oKCPImg3MIt.QX0ITO0wiN1kjNzEzW}
```

## What I learned
I learned how to read and use a sample documentation for a command.

## References
The problem statement was used as the reference
```
The program for this challenge is /challenge/challenge, and you'll need to invoke it properly in order for it to give you the flag. Let's pretend that this is its documentation:

Welcome to the documentation for /challenge/challenge! To properly run this program, you will need to pass it the argument of --giveflag. Good luck!

Given that knowledge, go get the flag!
```

# 2. Learning Complex Usage
The challenge prompted me to get familiar with reading documentation. 

## My Solve
**Flag:** `pwn.college{w-C-Igiu1DatGz_RpsTqTedIVkf.QX1ITO0wiN1kjNzEzW}`

```bash
hacker@man~learning-complex-usage:/$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{w-C-Igiu1DatGz_RpsTqTedIVkf.QX1ITO0wiN1kjNzEzW}
```

## What I learned
I learned how to read and understand documentation of a command.

## References
The problem statement was used as the reference
```
Welcome to the documentation for /challenge/challenge! This program allows you to print arbitrary files to the terminal, when given the --printfile argument. The argument to the --printfile argument is the path of the flag to read. For example, /challenge/challenge --printfile /challenge/DESCRIPTION.md will print out the description of the level!
```

# 3. Reading Manuals    
The challenge prompted me to use the `man` command. 

## My Solve
**Flag:** `pwn.college{MnrlPE8DTCIqzPHX0kICR215Mie.QX0EDO0wiN1kjNzEzW}`

```bash
hacker@man~reading-manuals:~$ /challenge/challenge --nrlqzk 802
Correct usage! Your flag: pwn.college{MnrlPE8DTCIqzPHX0kICR215Mie.QX0EDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `man` command to read details of a command, and its arguments.

## References
The problem statement was used as the reference
```
The challenge in this level has a secret option that, when you use it, will cause the challenge to print the flag. You must learn this option through the man page for challenge!
```

# 4. Searching Manuals
The challenge prompted me to search and use `man`. 

## My Solve
**Flag:** `pwn.college{o_qWY-_Llcak9oDSEcW8sVMUCdV.QX1EDO0wiN1kjNzEzW}`

```bash
hacker@man~searching-manuals:~$ /challenge/challenge --tgyb
Initializing...
Correct usage! Your flag: pwn.college{o_qWY-_Llcak9oDSEcW8sVMUCdV.QX1EDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `man` command and search for a string in the manual page.

## References
The problem statement was used as the reference
```
Find the option that will give you the flag by reading the challenge man page.
```

# 5. Searching For Manuals
The challenge prompted me to use the `man` command. 

## My Solve
**Flag:** `pwn.college{wE7teRRTRqX8sKK_fc7KsZK4EFb.QX2EDO0wiN1kjNzEzW}`

```bash
hacker@man~searching-for-manuals:~$ man -K challenge/challenge
^C
hacker@man~searching-for-manuals:~$ /challenge/challenge --wteqsf 787
Correct usage! Your flag: pwn.college{wE7teRRTRqX8sKK_fc7KsZK4EFb.QX2EDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `man man` command to read description of manual pages and search for specific command.

## References
The problem statement was used as the reference
```
This level is tricky: it hides the manpage for the challenge by randomizing its name. Luckily, all of the manpages are gathered in a searchable database, so you'll be able to search the man page database to find the hidden challenge man page! To figure out how to search for the right manpage, read the man page manpage by doing: man man!
```

# 6. Helpful Programs
The challenge prompted me to use the `--help` argument. 

## My Solve
**Flag:** `pwn.college{MnkYw1R8wGtozplg6Vxh-qwZ2Qj.QX3IDO0wiN1kjNzEzW}`

```bash
hacker@man~helpful-programs:~$ /challenge/challenge -g 186
Correct usage! Your flag: pwn.college{MnkYw1R8wGtozplg6Vxh-qwZ2Qj.QX3IDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `--help` argument to read a commands details.

## References
The problem statement was used as the reference
```
In this level, you will practice reading a program's documentation with --help. Try it out!
```

# 7. Help For Builtins
The challenge prompted me to use the `help` builtin command. 

## My Solve
**Flag:** `pwn.college{ou_lyzl4ca2gAp-cdFidk33KnAi.QX0ETO0wiN1kjNzEzW}`

```bash
hacker@man~help-for-builtins:~$ challenge --secret ou_lyzl4
Correct! Here is your flag!
pwn.college{ou_lyzl4ca2gAp-cdFidk33KnAi.QX0ETO0wiN1kjNzEzW}
```

## What I learned
I learned about builtin commands and using `help` to view their details

## References
The problem statement was used as the reference
```
Some good information! In this challenge, we'll practice using help to look up help for builtins. This challenge's challenge command is a shell builtin, rather than a program. Like before, you need to lookup its help to figure out the secret value to pass to it!
```

