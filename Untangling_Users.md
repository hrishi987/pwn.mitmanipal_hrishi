# 1. Becoming root with su
The challenge prompted me to use `su`. 

## My Solve
**Flag:** `pwn.college{c9GqEV2Nx-JoMxNdA0yqVMkqy5a.QX1UDN1wiN1kjNzEzW}`

```bash
root@users~becoming-root-with-su:/home/hacker# cat not-the-flag
pwn.college{c9GqEV2Nx-JoMxNdA0yqVMkqy5a.QX1UDN1wiN1kjNzEzW}
```

## What I learned
I learned how to use `su` command to elevate to root user.

## References
The problem statement was used as the reference
```
But THIS challenge (and only this challenge) does have a root password. That password is hack-the-planet, and you must provide it to su to become root! Go do that, and read the flag!
```

# 2. Other users with su
The challenge prompted me to use `su user` command. 

## My Solve
**Flag:** `pwn.college{Ew7pNUyAXbiycPwAOyjE4e7FLU4.QX2UDN1wiN1kjNzEzW}`

```bash
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{Ew7pNUyAXbiycPwAOyjE4e7FLU4.QX2UDN1wiN1kjNzEzW}
```

## What I learned
I learned how to use `su` command to switch to another user.

## References
The problem statement was used as the reference
```
Awesome! In this level, you must switch to the zardus user and then run /challenge/run. Zardus' password is dont-hack-me. Good luck!
```

# 3. Cracking passwords
The challenge prompted me to crack other user password. 

## My Solve
**Flag:** `pwn.college{kUfkiEvFz9yCjFOxtrqwU06IKOh.QX3UDN1wiN1kjNzEzW}`

```bash
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{kUfkiEvFz9yCjFOxtrqwU06IKOh.QX3UDN1wiN1kjNzEzW}
```

## What I learned
I learned how to use `john` and to read etc/shadow file to crack zardus user password.

## References
The problem statement was used as the reference
```
This level simulates this story, giving you a leak of /etc/shadow (in /challenge/shadow-leak). Crack it (this could take a few minutes), su to zardus, and run /challenge/run to get the flag!
```

# 4. Using sudo
The challenge prompted me to use sudo. 

## My Solve
**Flag:** `pwn.college{kRpIZcOm2qeBA-SF_FiMXCzR2MF.QX4UDN1wiN1kjNzEzW}`

```bash
hacker@users~using-sudo:~$ sudo cat not-the-flag
pwn.college{kRpIZcOm2qeBA-SF_FiMXCzR2MF.QX4UDN1wiN1kjNzEzW}
```

## What I learned
I learned how to use `sudo` command.

## References
The problem statement was used as the reference
```
In this level, we will give you sudo access, and you will use it to read the flag. Nice and easy!
```
