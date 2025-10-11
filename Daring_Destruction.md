# 1. The Fork Bomb
The challenge prompted me to edit the PATH variable. 

## My Solve
**Flag:** `pwn.college{YWfMLaE1IqUYi9Cv_eUShFwxGsn.0VMzEzNxwiN1kjNzEzW}`

```bash
hacker@shenanigans~bashrc-backdoor:~$ /challenge/victim
Username: zardus
Password: ***********
pwn.college{YWfMLaE1IqUYi9Cv_eUShFwxGsn.0VMzEzNxwiN1kjNzEzW}
zardus@shenanigans~bashrc-backdoor:~$ exit
logout
hacker@shenanigans~bashrc-backdoor:~$
```

## What I learned
I learned about the .bashrc script

## References
The problem statement was used as the reference
```
In this challenge, we'll pretend that you've broken into a victim user's machine! That user is named zardus, with a home directory of /home/zardus. You, as the hacker user, have write access to his .bashrc, and zardus has read-access to /flag. The victim is simulated by the script /challenge/victim, and you can launch this script at any time to observe the victim logging into the computer. Can you get the flag?
```

# 2. Setting PATH
The challenge prompted me to set a PATH variable.

## My Solve
**Flag:** `pwn.college{EBilB-_6KX5xICnwnmfwPcF2dxf.QX1cjM1wiN1kjNzEzW}`

```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{EBilB-_6KX5xICnwnmfwPcF2dxf.QX1cjM1wiN1kjNzEzW}
```

## What I learned
I learned how to set a directory in PATH variable.

## References
The problem statement was used as the reference
```
Let's practice. This level's /challenge/run will run the win command via its bare name, but this command exists in the /challenge/more_commands/ directory, which is not initially in the PATH. The win command is the only thing that /challenge/run needs, so you can just overwrite PATH with that one directory. Good luck!
```

# 3. Finding Commands
The challenge prompted me to use `which`.

## My Solve
**Flag:** `pwn.college{kH18tqSomQL8Gv-j1K4BDjpmivz.01NzEzNxwiN1kjNzEzW}`

```bash
hacker@path~finding-commands:~$ cat /challenge/paths/31424/flag
pwn.college{kH18tqSomQL8Gv-j1K4BDjpmivz.01NzEzNxwiN1kjNzEzW}
```

## What I learned
I learned how to use `win` command to list the commands directory.

## References
The problem statement was used as the reference
```
In this challenge, we added a win command somewhere in your $PATH, but it won't give you the flag. Instead, it's in the same directory as a flag file that we made readable by you! You must find win (with the which command), and cat the flag out of that directory!
```

# 4. Adding Commands
The challenge prompted me add commands to PATH

## My Solve
**Flag:** `pwn.college{g7bxUNjz-ojv91kRKgVvwlJn-a4.QX2cjM1wiN1kjNzEzW}`

```bash
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{g7bxUNjz-ojv91kRKgVvwlJn-a4.QX2cjM1wiN1kjNzEzW}
```

## What I learned
I learned how to set commands to PATH

## References
The problem statement was used as the reference
```
You have three options to avoid that:

Figure out where the cat program is on the filesystem. It must be in a directory that lives in the PATH variable, so you can print the variable out (refer to Shell Variables to remember how!), and go through the directories in it (recall that the different entries are separated by :), find which one has cat in it, and invoke cat by its absolute path.
Set a PATH that has the old directories plus a new entry for wherever you create win.
Use read (again, refer to Shell Variables) to read /flag. Since read is a builtin functionality of bash, it is unaffected by PATH shenanigans.
```

# 5.  Hijacking Commands
The challenge prompted me to put what ive learnt to use.

## My Solve
**Flag:** `pwn.college{shSeK5Ylp9uCT_DyuKc3GcIujRp.QX3cjM1wiN1kjNzEzW}`

```bash
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
Found 'rm' command at /home/hacker/rm. Executing!
pwn.college{shSeK5Ylp9uCT_DyuKc3GcIujRp.QX3cjM1wiN1kjNzEzW}
```

## What I learned
I learned how to replace rm with a fake rm command.

## References
The problem statement was used as the reference
```
Armed with your knowledge, you can now carry out some shenanigans. This challenge is almost the same as the first challenge in this module. Again, this challenge will delete the flag using the rm command. But unlike before, it will not print anything out for you.

How can you solve this? You know that rm is searched for in the directories listed in the PATH variable. You have experience creating the win command when the previous challenge needed it. What else can you create?
```
