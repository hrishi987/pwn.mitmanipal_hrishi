# 1. Changing File Ownership
The challenge prompted me to change ownership of a file

## My Solve
**Flag:** `pwn.college{Y4Zl1DJZgn2TPemMBBLehAQmQu_.QXxEjN0wiN1kjNzEzW}`

```bash
hacker@permissions~changing-file-ownership:~$ chown hacker not-the-flag
hacker@permissions~changing-file-ownership:~$ cat not-the-flag
pwn.college{Y4Zl1DJZgn2TPemMBBLehAQmQu_.QXxEjN0wiN1kjNzEzW}
```

## What I learned
I learned how to use `chown` tcommand to change access control of a file.

## References
The problem statement was used as the reference
```
In this level, we will practice changing the owner of the /flag file to the hacker user, and then read the flag. For this challenge only, I made it so that you can use chown to your heart's content as the hacker user (again, typically, this requires you to be root). Use this power wisely and chown away!
```

# 2. Groups and Files
The challenge prompted me to make user part of a group. 

## My Solve
**Flag:** `pwn.college{MryOBx2B8unC7ZBGJqrvfFuWWNL.QXxcjM1wiN1kjNzEzW}`

```bash
hacker@permissions~groups-and-files:~$ chgrp hacker not-the-flag
hacker@permissions~groups-and-files:~$ cat not-the-flag
pwn.college{MryOBx2B8unC7ZBGJqrvfFuWWNL.QXxcjM1wiN1kjNzEzW}
```

## What I learned
I learned how to use `chgrp` to change user's group.

## References
The problem statement was used as the reference
```
In this level, I have made the flag readable by whatever group owns it, but this group is currently root. Luckily, I have also made it possible for you to invoke chgrp as the hacker user! Change the group ownership of the flag file, and read the flag!
```

# 3. Fun With Groups Names
The challenge prompted me to use `id` to list the groups.

## My Solve
**Flag:** `pwn.college{w2V424PWxHW3M08zgDlqn-ogeNq.QXycjM1wiN1kjNzEzW}`

```bash
hacker@permissions~fun-with-groups-names:~$ chgrp grp4153 not-the-flag
hacker@permissions~fun-with-groups-names:~$ cat not-the-flag
pwn.college{w2V424PWxHW3M08zgDlqn-ogeNq.QXycjM1wiN1kjNzEzW}
```

## What I learned
I learned how to use `id` to list all the groups user's part of.

## References
The problem statement was used as the reference
```
The point is, you've used hacker for the group before, but in this level, that is not going to work. I'll still allow you to use chgrp, but I have randomized the name of the group that your user is in. You will need to use the id command to figure that name out, then chgrp to victory!
```

# 4. Changing Permissions
The challenge prompted me to change permissions of a file.

## My Solve
**Flag:** `pwn.college{IYVG38RMI2GkCSlZHVnvonSxaYk.QXzcjM1wiN1kjNzEzW}`

```bash
hacker@permissions~changing-permissions:/$ chmod o+r flag
hacker@permissions~changing-permissions:/$ cat flag
pwn.college{IYVG38RMI2GkCSlZHVnvonSxaYk.QXzcjM1wiN1kjNzEzW}
```

## What I learned
I learned how to use `chmod` to change permissions of a file for a user/group/other users.

## References
The problem statement was used as the reference
```
In this challenge, you must change the permissions of the /flag file to read it! Typically, you need to have write access to the file in order to change its permissions, but I have made the chmod command all-powerful for this level, and you can chmod anything you want even though you are the hacker user. This is an ultimate power. The /flag file is owned by root, and you can't change that, but you can make it readable. Go and solve this!
```

# 5.  Executable Files
The challenge prompted me to change permissions of an executable.

## My Solve
**Flag:** `pwn.college{4YSveWeiCv1EP6s28EhUYBoRdXr.QXyEjN0wiN1kjNzEzW}`

```bash
hacker@permissions~executable-files:~$ chmod u+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{4YSveWeiCv1EP6s28EhUYBoRdXr.QXyEjN0wiN1kjNzEzW}
```

## What I learned
I learned how to use `chmod` to change permissions of an executable.

## References
The problem statement was used as the reference
```
In this challenge, the /challenge/run program will give you the flag, but you must first make it executable! Remember your chmod, and get /challenge/run to tell you the flag!
```

# 6. Permission Tweaking Practise
The challenge prompted me to do a bunch of permission changes.

## My Solve
**Flag:** `pwn.college{0gW_nNZr6gCxDoR-pyw9CXE9ONu.QXwEjN0wiN1kjNzEzW}`

```bash
hacker@permissions~permission-tweaking-practice:~$ chmod u+r /flag
hacker@permissions~permission-tweaking-practice:~$ cat /flag
pwn.college{0gW_nNZr6gCxDoR-pyw9CXE9ONu.QXwEjN0wiN1kjNzEzW}
```

## What I learned
I got a bit of practise on changing different file permissions.

## References
The problem statement was used as the reference
```
This challenge will ask you to change the permissions of the /challenge/pwn file in specific ways a few times in a row. If you get the permissions wrong, the game will reset and you can try again. If you get the permissions right eight times in a row, the challenge will let you chmod /flag to make it readable for yourself :-) Launch /challenge/run to get started!
```

# 7. Permissions Setting Practise
The challenge prompted me to practise a bunch of permission changes.

## My Solve
**Flag:** `pwn.college{MBbLs4S4YX8YJG1lBGMaQ7506Ko.QXzETO0wiN1kjNzEzW}`

```bash
hacker@permissions~permissions-setting-practice:~$ chmod u+r /flag
hacker@permissions~permissions-setting-practice:~$ cat /flag
pwn.college{MBbLs4S4YX8YJG1lBGMaQ7506Ko.QXzETO0wiN1kjNzEzW}
```

## What I learned
I practised a bunch of file permission changing commands.

## References
The problem statement was used as the reference
```
This level extends the previous level by requesting more radical permission changes, which you will need = and ,-chaining to achieve. Good luck!
```

# 8. The SUID Bit
The challenge prompted me to set `SUID` bit permissions.

## My Solve
**Flag:** `pwn.college{ghO2eLsZghPfvOA5j6j3XoDDl6s.QXzEjN0wiN1kjNzEzW}`

```bash
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root!
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{ghO2eLsZghPfvOA5j6j3XoDDl6s.QXzEjN0wiN1kjNzEzW}
```

## What I learned
I learned how to add `SUID` bit to a program's permissions.

## References
The problem statement was used as the reference
```
Now, we are going to let you add the SUID bit to the /challenge/getroot program in order to spawn a root shell for you to cat the flag yourself!
```
