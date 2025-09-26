# 1. cat: not the pet, but the command!
The challenge prompted me to use the cat command to read a file. 

## My Solve
**Flag:** `pwn.college{8euax5I11w_No4ZWRqV55jH4aAz.QXxcTN0wiN1kjNzEzW}`

```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{8euax5I11w_No4ZWRqV55jH4aAz.QXxcTN0wiN1kjNzEzW}
```

## What I learned
I learned how to use cat command, to read a file.

## References
The problem statement was used as the reference
```
In this challenge, I will copy the flag to the flag file in your home directory (where your shell starts). Go read it with cat!
```

# 2. catting absolute paths
The challenge prompted me to use the cat command with absolute path to read a file. 

## My Solve
**Flag:** `pwn.college{EdXRLOpzAKC-Eulm4z8ToIabs5-.QX5ETO0wiN1kjNzEzW}`

```bash
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{EdXRLOpzAKC-Eulm4z8ToIabs5-.QX5ETO0wiN1kjNzEzW}
```

## What I learned
I learned how to use cat command by referring to absolute path, to read a file.

## References
The problem statement was used as the reference
```
In this directory, I will not copy it to your home directory, but I will make it readable. You can read it with cat at its absolute path: /flag.
```

# 3. more catting practise
The challenge prompted me to use the cat command again with absolute path to read a file. 

## My Solve
**Flag:** `pwn.college{A9r4MGtN5tZWyi46PVodjGanC3M.QXwITO0wiN1kjNzEzW}`

```bash
hacker@commands~more-catting-practice:~$ cat /lib/x86_64-linux-gnu/xtables/flag
pwn.college{A9r4MGtN5tZWyi46PVodjGanC3M.QXwITO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `cat` command by referring to absolute path, to read a file.

## References
The problem statement was used as the reference
```
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /lib/x86_64-linux-gnu/xtables/flag. Go cat it out **without** cding
into that directory!
```

# 4. grepping for a needle in a haystack
The challenge prompted me to use the grep command. 

## My Solve
**Flag:** `pwn.college{MFedCetLHEQ_UQiUXnzCBNzHnLz.QX3EDO0wiN1kjNzEzW}`

```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{MFedCetLHEQ_UQiUXnzCBNzHnLz.QX3EDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `grep` command to search for a specific string in a large file.

## References
The problem statement was used as the reference
```
Invoked like this, grep will search the file for lines of text containing SEARCH_STRING and print them to the console.
In this challenge, I've put a hundred thousand lines of text into the /challenge/data.txt file. grep it for the flag!
HINT: The flag always starts with the text pwn.college.
```

# 5. comparing files
The challenge prompted me to use the diff command. 

## My Solve
**Flag:** `pwn.college{cu9LopUw8-CG6NHuWwAHUZWdRWX.01MwMDOxwiN1kjNzEzW}`

```bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
97a98
> pwn.college{cu9LopUw8-CG6NHuWwAHUZWdRWX.01MwMDOxwiN1kjNzEzW}
```

## What I learned
I learned how to use `diff` command to compare two files for changes.

## References
The problem statement was used as the reference
```
Now for your challenge! There are two files in /challenge:

/challenge/decoys_only.txt contains 100 fake flags
/challenge/decoys_and_real.txt contains all 100 fake flags plus the one real flag
Use diff to find what's different between these files and get your flag!
```

# 6. listing files
The challenge prompted me to use the `ls` command. 

## My Solve
**Flag:** `pwn.college{wMoaYIm7pAMZsDoOzbiE08EsnEZ.QX4IDO0wiN1kjNzEzW}`

```bash
hacker@commands~listing-files:~$ /challenge/17233-renamed-run-5918
Yahaha, you found me! Here is your flag:
pwn.college{wMoaYIm7pAMZsDoOzbiE08EsnEZ.QX4IDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `ls` command to compare two files for changes.

## References
The problem statement was used as the reference
```
In this challenge, we've named /challenge/run with some random name! List the files in /challenge to find it.
```

# 7. touching files
The challenge prompted me to use the `touch` command. 

## My Solve
**Flag:** `pwn.college{YXm32fN-uvmL_OdjET34ZL3rqVy.QXwMDO0wiN1kjNzEzW}`

```bash
hacker@commands~touching-files:~$ touch /tmp/pwn
hacker@commands~touching-files:~$ touch /tmp/college
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{YXm32fN-uvmL_OdjET34ZL3rqVy.QXwMDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `touch` command to create a file.

## References
The problem statement was used as the reference
```
It's that simple! In this level, please create two files: /tmp/pwn and /tmp/college, and run /challenge/run to get your flag!
```

# 8. removing files
The challenge prompted me to use the `rm` command. 

## My Solve
**Flag:** `pwn.college{4RT7tz5qVLbFTuN9Q9K2InIDmow.QX2kDM1wiN1kjNzEzW}`

```bash
hacker@commands~removing-files:~$ touch delete_me
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{4RT7tz5qVLbFTuN9Q9K2InIDmow.QX2kDM1wiN1kjNzEzW}
```

## What I learned
I learned how to use `rm` command to remove/delete a file.

## References
The problem statement was used as the reference
```
Let's practice. This challenge will create a delete_me file in your home directory! Delete it, then run /challenge/check, which will make sure you've deleted it and then give you the flag!
```

# 9. moving files
The challenge prompted me to use the `mv` command. 

## My Solve
**Flag:** `pwn.college{AAavdmtgBMsxMkmeB9hXNTZ5eK3.0VOxEzNxwiN1kjNzEzW}`

```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{AAavdmtgBMsxMkmeB9hXNTZ5eK3.0VOxEzNxwiN1kjNzEzW}
```

## What I learned
I learned how to use `mv` command to move a file to another directory.

## References
The problem statement was used as the reference
```
This challenge wants you to move the /flag file into /tmp/hack-the-planet (do it)! When you're done, run /challenge/check, which will check things out and give the flag to you.
```

# 10. hidden files
The challenge prompted me to use the `ls -a` command. 

## My Solve
**Flag:** `pwn.college{AAavdmtgBMsxMkmeB9hXNTZ5eK3.0VOxEzNxwiN1kjNzEzW}`

```bash
hacker@commands~hidden-files:~$ ls -a
.  ..  .bash_history  .config  a
hacker@commands~hidden-files:~$ cat a
pwn.college{A64h6Oan_jePOBxD2g19KfVc6G4.QXzMDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `ls` command with argument`-a` to view hidden files.

## References
The problem statement was used as the reference
```
Now, it's your turn! Go find the flag, hidden as a dot-prepended file in /.
```

# 11. An Epic Filesystem Quest
The challenge prompted me to use the `ls` and `cd` commands. 

## My Solve
**Flag:** `pwn.college{w3WUeULfCFEtZ1vzWdV_8hXsHHr.QX5IDO0wiN1kjNzEzW}`

```bash
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sympy/polys/agca$ cat /usr/lib/python3/dist-pack
ages/twisted/internet/test/.SECRET
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{w3WUeULfCFEtZ1vzWdV_8hXsHHr.QX5IDO0wiN1kjNzEzW}
```

## What I learned
I learnt and understood how to work with  `ls` and `cd` commands better with this challenge.

## References
The problem statement was used as the reference
```
In this challenge, I have hidden the flag! Here, you will use ls and cat to follow my breadcrumbs and find it! Here's how it'll work:

Your first clue is in /. Head on over there.
Look around with ls. There'll be a file named HINT or CLUE or something along those lines!
cat that file to read the clue!
Depending on what the clue says, head on over to the next directory (or don't!).
Follow the clues to the flag!
Good luck!
```

# 12. making directories
The challenge prompted me to use the `mkdir` command.

## My Solve
**Flag:** `pwn.college{w9HfgLVyrgSdzRB2GXQ7HRvvFKm.QXxMDO0wiN1kjNzEzW}`

```bash
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ touch /tmp/pwn/college
hacker@commands~making-directories:~$ /challenge/run
Success! Here is your flag:
pwn.college{w9HfgLVyrgSdzRB2GXQ7HRvvFKm.QXxMDO0wiN1kjNzEzW}
```

## What I learned
I learnt and understood how to use the `mkdir` command to create directories.

## References
The problem statement was used as the reference
```
Now, go forth and create a /tmp/pwn directory and make a college file in it! Then run /challenge/run, which will check your solution and give you the flag!
```

# 13. finding files
The challenge prompted me to use the `find` command.

## My Solve
**Flag:** `pwn.college{IIU-Q6B1T2Ti18oyFE_eH5UEeas.QXyMDO0wiN1kjNzEzW}`

```bash
hacker@commands~finding-files:~$ cat /opt/linux/linux-5.4/tools/arch/ia64/include/uapi/flag
pwn.college{IIU-Q6B1T2Ti18oyFE_eH5UEeas.QXyMDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use the `find` command to search for a file/directory in the filesystem.

## References
The problem statement was used as the reference
```
Now it's your turn. I've hidden the flag in a random directory on the filesystem. It's still called flag. Go find it!

Several notes. First, there are other files named flag on the filesystem. Don't panic if the first one you try doesn't have the actual flag in it. Second, there're plenty of places in the filesystem that are not accessible to a normal user. These will cause find to generate errors, but you can ignore those; we won't hide the flag there! Finally, find can take a while; be patient!
```

# 14. linking files
The challenge prompted me to use the `ln` command.

## My Solve
**Flag:** `pwn.college{Ym_S2b1PhJCV39-NHHdEPaLS7to.QX5ETN1wiN1kjNzEzW}`

```bash
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{Ym_S2b1PhJCV39-NHHdEPaLS7to.QX5ETN1wiN1kjNzEzW}
```

## What I learned
I learned how to use the `ls` command to create and use symbolic link files

## References
The problem statement was used as the reference
```
Okay, now you try it! In this level the flag is, as always, in /flag, but /challenge/catflag will instead read out /home/hacker/not-the-flag. Use the symlink, and fool it into giving you the flag!
```