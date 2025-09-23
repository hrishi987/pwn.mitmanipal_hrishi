#The Root
Working with rooth path.

## My solve
**Flag:** `pwn.college{0SKCYdWda0Pijolavv_aXUZUCHC.QX4cTO0wiN1kjNzEzW}`

Pretty direct path command execution.

```bash
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{0SKCYdWda0Pijolavv_aXUZUCHC.QX4cTO0wiN1kjNzEzW}
```

#Program and absolute paths
Running program using absolute path.

## My solve
**Flag:** `pwn.college{ki9HjB_nPm5BdqMXaZndNJPnZdy.QX1QTN0wiN1kjNzEzW}`

Pretty direct absolute path command execution.

```bash
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{ki9HjB_nPm5BdqMXaZndNJPnZdy.QX1QTN0wiN1kjNzEzW}
```

#Position thy self
Navigating directories.

## My solve
**Flag:** `pwn.college{4zk8NUucpSB3FI5F9gvMfseDQ6u.QX2QTN0wiN1kjNzEzW}`

Had a bit of trouble initially trying to find out which directory to be in. Got an error message when i tried to run the program directly, which showed the path to cd to.

```bash
hacker@paths~position-thy-self:/usr/bin$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{4zk8NUucpSB3FI5F9gvMfseDQ6u.QX2QTN0wiN1kjNzEzW}
```

#Position elsewhere
Navigating directories.

## My solve
**Flag:** `pwn.college{gFpCzUihG_DvU0ZmSZMAR2HQ935.QX3QTN0wiN1kjNzEzW}`

Similar challenge as the previous one.

```bash
hacker@paths~position-elsewhere:/var/lib/apt/lists$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{gFpCzUihG_DvU0ZmSZMAR2HQ935.QX3QTN0wiN1kjNzEzW}
```

#Position yet elsewhere
Navigating directories.

## My solve
**Flag:** `pwn.college{0Rdwp8MYTB1vGDUTjoF3FY0UjUg.QX4QTN0wiN1kjNzEzW}`

Similar challenge as the previous one.

```bash
hacker@paths~position-yet-elsewhere:/var/log$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{0Rdwp8MYTB1vGDUTjoF3FY0UjUg.QX4QTN0wiN1kjNzEzW}
```

#Implicit relative paths, from /
Navigating directories using relative paths.

## My solve
**Flag:** `pwn.college{o3iQCMMc-tge6NoDyczD7N7Ntcj.QX5QTN0wiN1kjNzEzW}`

Learnt the difference between absolute and relative paths

```bash
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{o3iQCMMc-tge6NoDyczD7N7Ntcj.QX5QTN0wiN1kjNzEzW}
```

#explicit relative paths, from /
Navigating directories using relative paths.

## My solve
**Flag:** `pwn.college{wfK24j75smLrpHPPq49L8ABXmu0.QXwUTN0wiN1kjNzEzW}`

Learnt the use of ./ relative path

```bash
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{wfK24j75smLrpHPPq49L8ABXmu0.QXwUTN0wiN1kjNzEzW}
```

#implicit relative path
Navigating directories using relative paths.

## My solve
**Flag:** `pwn.college{0UtVaqeCQlk_06T_J-m-Ex6ZM3U.QXxUTN0wiN1kjNzEzW}`

Learnt to use ./ to run the program in the same directory explicitly

```bash
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{0UtVaqeCQlk_06T_J-m-Ex6ZM3U.QXxUTN0wiN1kjNzEzW}
```

#home sweet home
Navigating directories using relative paths.

## My solve
**Flag:** `pwn.college{A64h6Oan_jePOBxD2g19KfVc6G4.QXzMDO0wiN1kjNzEzW}`

Learnt to navigate to home directory ~/

```bash
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{A64h6Oan_jePOBxD2g19KfVc6G4.QXzMDO0wiN1kjNzEzW}
```