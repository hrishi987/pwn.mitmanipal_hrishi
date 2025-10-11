# 1. Disk-Space Doomsday
A challenge 

## My Solve
**Flag:** `pwn.college{skSJ8Zes_v--jRx6avlcvhhYPf5.0lMyEzNxwiN1kjNzEzW}`

```bash
hacker@destruction~disk-space-doomsday:~$ /challenge/check
Disk space restored. Here is your flag:
pwn.college{skSJ8Zes_v--jRx6avlcvhhYPf5.0lMyEzNxwiN1kjNzEzW}
```

## What I learned
I learned about exhausting disk space using `yes`

## References
The problem statement was used as the reference
```
This challenge forces you to fill the disk and then clean up. The process:

Fill your disk.
Run /challenge/check. It will attempt to create a 1 megabyte temporary file. If that fails, you pass the first stage and the checker will ask you to free the space.
Delete the file you made (with rm) to clear up the space.
Run /challenge/check a second time. If it can now create the temporary file (i.e., you successfully cleaned up your home directory), you’ll receive the flag.
```

# 2.rm -rf /
Challenge to clera disk

## My Solve
**Flag:** `pwn.college{AjXACDwjBVIZFJPpuE4F_855BnS.0lMzEzNxwiN1kjNzEzW}`

```bash
hacker@destruction~rm-rf-:~$ YES! You wiped it, you wild hacker! The flag is yours:
pwn.college{AjXACDwjBVIZFJPpuE4F_855BnS.0lMzEzNxwiN1kjNzEzW}
```

## What I learned
I learned how to launch an attack to delete sys directory

## References
The problem statement was used as the reference
```
In this challenge, you will do something that you might never do again: wipe the whole system. We've actually modified things a bit to keep your home directory safe (normally, it would get wiped as well!), but otherwise, all that stands before you and the flag is your willingness to wipe the drive. But before you wipe it all, make sure to start /challenge/check so that it can watch the fireworks (and give you the flag)!
```

# 3. Life after rm -rf /
Challenge

## My Solve
**Flag:** `pwn.college{8WO5sSZNrRjE0jQek0xitImHu0P.01MzEzNxwiN1kjNzEzW}`

```bash
hacker@destruction~life-after-rm-rf-:~$ YES! You did it again! Go read the flag!
read s < /flag
[1]+  Done                    /challenge/check
hacker@destruction~life-after-rm-rf-:~$ echo $s
pwn.college{8WO5sSZNrRjE0jQek0xitImHu0P.01MzEzNxwiN1kjNzEzW}
```

## What I learned
Extension to previous challenge, refreshed use of read to read files

## References
The problem statement was used as the reference
```
This challenge will force you to try it. It's almost the same as the previous one, but you must read the flag yourself after you destroy the system. After you rm everything, your previously-launched /challenge/check will restore the /flag file and make it readable. Then you can read it!
```

# 4. Find meaning after rm -rf /
Challenge
## My Solve
**Flag:** `pwn.college{8iXtfrI3ZtYQm0K1EiHdNcva8yb.0FNzEzNxwiN1kjNzEzW}`

```bash
hacker@destruction~finding-meaning-after-rm-rf-:~$ read var < /d0b3accc
hacker@destruction~finding-meaning-after-rm-rf-:~$ echo $var
pwn.college{8iXtfrI3ZtYQm0K1EiHdNcva8yb.0FNzEzNxwiN1kjNzEzW}
```

## What I learned
More to deleting system direc

## References
The problem statement was used as the reference
```
There are a lot of ways to solve this challenge. echo is a builtin, and you can File Glob an argument to it to expand to all files! For example, echo * will print out the names of all of the files in the current directory. Similarly, you can use tab-completion (hit tab a few times) of an argument to have the shell list possible files for you.

Whatever route you use, find the randomly-named file that /challenge/check makes in / after you rm, read it, and get the flag!
```
