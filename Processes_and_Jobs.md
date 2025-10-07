# 1. Listing processes
The challenge prompted me to use `ps`. 

## My Solve
**Flag:** `pwn.college{gBcz2JpjoDHnxnhkCepGGxQHm5u.QX4MDO0wiN1kjNzEzW}`

```bash
hacker@processes~listing-processes:~$ /challenge/12431-run-12435
Yahaha, you found me! Here is your flag:
pwn.college{gBcz2JpjoDHnxnhkCepGGxQHm5u.QX4MDO0wiN1kjNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```

## What I learned
I learned how to use `ps aux` to list running processes.

## References
The problem statement was used as the reference
```
Anyways! Let's practice. In this level, I have once again renamed /challenge/run to a random filename, and this time made it so that you cannot ls the /challenge directory! But I also launched it, so you can find it in the running process list, figure out the filename, and relaunch it directly for the flag! Good luck!
```

# 2. Kill processes
The challenge prompted me to use `kill` command. 

## My Solve
**Flag:** `pwn.college{4hPSWd7_vJd8vR2Q7DjWS_wQKjt.QXyQDO0wiN1kjNzEzW}`

```bash
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{4hPSWd7_vJd8vR2Q7DjWS_wQKjt.QXyQDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `kill` command to kill processes by PID.

## References
The problem statement was used as the reference
```
Now, it's time to terminate your first process! In this challenge, /challenge/run will refuse to run while /challenge/dont_run is running! You must find the dont_run process and kill it. If you fail, pwn.college will disavow all knowledge of your mission. Good luck.
```

# 3. Interrupting processes
The challenge prompted me to interrupt a process. 

## My Solve
**Flag:** `pwn.college{8MjyykNELb5IazRuR4KXGizPE_E.QXzQDO0wiN1kjNzEzW}`

```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{8MjyykNELb5IazRuR4KXGizPE_E.QXzQDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `Ctrl+c` to interrupt a process.

## References
The problem statement was used as the reference
```
Try it here! /challenge/run will refuse to give you the flag until you interrupt it. Good luck!
```

# 4. Kill misbehaving processes
The challenge prompted me to kill a misbehaving process. 

## My Solve
**Flag:** `pwn.college{4GtQMt3ujAQUs2TOcTISniRelYK.0FNzMDOxwiN1kjNzEzW}`

```bash
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{4GtQMt3ujAQUs2TOcTISniRelYK.0FNzMDOxwiN1kjNzEzW}
```

## What I learned
I learned the workflow to kill a misbehaving process.

## References
The problem statement was used as the reference
```
In this challenge, there's a decoy process that's hogging a critical resource - a named pipe (FIFO) at /tmp/flag_fifo into which (like in the Practicing Piping FIFO challenge) /challenge/run wants to write your flag. You need to kill this process.
```

# 5.  Suspending processes
The challenge prompted me to suspend a process. 

## My Solve
**Flag:** `pwn.college{MpylVIHKJz1raqNvAOTAL55ZLeF.QX1QDO0wiN1kjNzEzW}`

```bash
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         139     130  0 12:38 pts/0    00:00:00 bash /challenge/run
root         147     130  0 12:38 pts/0    00:00:00 bash /challenge/run
root         149     147  0 12:38 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{MpylVIHKJz1raqNvAOTAL55ZLeF.QX1QDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `ctrl+z` to suspend a process in the background.

## References
The problem statement was used as the reference
```
This level's run wants to see another copy of itself running and using the same terminal. How? Use the terminal to launch it, then suspend it, then launch another copy while the first is suspended!
```

# 6. Resuming processes
The challenge prompted me to resume a process. 

## My Solve
**Flag:** `pwn.college{crbI_8kEJQ-8tqQeljOevTMCJni.QX2QDO0wiN1kjNzEzW}`

```bash
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{crbI_8kEJQ-8tqQeljOevTMCJni.QX2QDO0wiN1kjNzEzW}
Don't forget to press Enter to quit me!
```

## What I learned
I learned how to use `fg` command to resume a suspended process.

## References
The problem statement was used as the reference
```
Go try it out! This challenge's run needs you to suspend it, then resume it. Good luck!
```

# 7. Backgrounding processes
The challenge prompted me to use the `bg` command. 

## My Solve
**Flag:** `pwn.college{U1veRKI24gUAgitFvDhUUb0Q2ED.QX3QDO0wiN1kjNzEzW}`

```bash
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         138 S    bash /challenge/run
root         148 S    sleep 6h
root         149 S+   bash /challenge/run
root         151 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{U1veRKI24gUAgitFvDhUUb0Q2ED.QX3QDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `bg` command to background a suspended process.

## References
The problem statement was used as the reference
```
This level's run wants to see another copy of itself running, not suspended, and using the same terminal. How? Use the terminal to launch it, then suspend it, then background it with bg and launch another copy while the first is running in the background!
```

# 8. Foregrounding processes
The challenge prompted me to use the `fg` command. 

## My Solve
**Flag:** `pwn.college{YeUl73lL1cJhPgZfIp3om6sb1bT.QX4QDO0wiN1kjNzEzW}`

```bash
hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{YeUl73lL1cJhPgZfIp3om6sb1bT.QX4QDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `fg` command to foreground a background process.

## References
The problem statement was used as the reference
```
Imagine that you have a backgrounded process, and you want to mess with it some more. What do you do? Well, you can foreground a backgrounded process with fg just like you foreground a suspended process! This level will walk you through that!
```

# 9. Starting backgrounded processes
The challenge prompted me to use the `&` command. 

## My Solve
**Flag:** `pwn.college{8CpiaVKpTMw04nXi9VDqHKS2Y00.QX5QDO0wiN1kjNzEzW}`

```bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 138
hacker@processes~starting-backgrounded-processes:~$


Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{8CpiaVKpTMw04nXi9VDqHKS2Y00.QX5QDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `&` along with the command to start it backgrounded.

## References
The problem statement was used as the reference
```
Here, sleep is actively running in the background, not suspended. Now it's your turn to practice! Launch /challenge/run backgrounded for the flag!
```

# 10. Process exit codes
The challenge prompted me to use the `$&` command. 

## My Solve
**Flag:** `pwn.college{EyEzYfkc6aXqe2dENhrizmMtKbt.QX5YDO1wiN1kjNzEzW}`

```bash
hacker@processes~process-exit-codes:~$ /challenge/submit-code 239
CORRECT! Here is your flag:
pwn.college{EyEzYfkc6aXqe2dENhrizmMtKbt.QX5YDO1wiN1kjNzEzW}
```

## What I learned
I learned how to use `$&` command to view exit code of the previously terminated process.

## References
The problem statement was used as the reference
```
In this challenge, you must retrieve the exit code returned by /challenge/get-code and then run /challenge/submit-code with that error code as an argument. Good luck!
```
