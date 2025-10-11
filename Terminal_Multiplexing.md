# 1. Launching Screen
The challenge prompted me to launch a screen. 

## My Solve
**Flag:** `pwn.college{cJcAqjznMcq4c6rtBF-cYoY2i-f.0VN4IDOxwiN1kjNzEzW}`

```bash
Congratulations! You're inside a screen session!
Here's your flag:
pwn.college{cJcAqjznMcq4c6rtBF-cYoY2i-f.0VN4IDOxwiN1kjNzEzW}
hacker@terminal-multiplexing~launching-screen:~$
```

## What I learned
I learned how to use `screen` to launch a screen session.

## References
The problem statement was used as the reference
```
For this challenge, we've hooked things up so that just launching screen will get you the flag. Easy!
```

# 2. Detaching and Attaching
The challenge prompted me to detach and attach to a screen.

## My Solve
**Flag:** `pwn.college{Ev9D48xo0WfqpRL2RgkQSdXkdPK.0lN4IDOxwiN1kjNzEzW}`

```bash
Yes! Flag is: pwn.college{Ev9D48xo0WfqpRL2RgkQSdXkdPK.0lN4IDOxwiN1kjNzEzW}
hacker@terminal-multiplexing~detaching-and-attaching:~$
```

## What I learned
I learned how to use `screen` and to detach and attach to it using `ctrl+A d` and `screen -r`.

## References
The problem statement was used as the reference
```
For this challenge, you'll need to:

Launch screen
Detach from it.
Run /challenge/run (this will secretly send the flag to your detached session!)
Reattach to see your prize
```

# 3. Finding Sessions
The challenge prompted me to list and look for a session.

## My Solve
**Flag:** `pwn.college{sK7sA71KW-q6POE1OM6eyE3Ag76.01N4IDOxwiN1kjNzEzW}`

```bash
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{sK7sA71KW-q6POE1OM6eyE3Ag76.01N4IDOxwiN1kjNzEzW}
pwn.college{sK7sA71KW-q6POE1OM6eyE3Ag76.01N4IDOxwiN1kjNzEzW}
```

## What I learned
I learned how to use `screen -ls` to list different sessions and reattach to it.

## References
The problem statement was used as the reference
```
In this challenge, we've created three screen sessions for you. One of them contains the flag. The other two are decoys!

You'll need to check each one until you find it. Don't forget to detach (Ctrl-A d) before trying the next session!
```

# 4. Switching Windows
The challenge prompted me to switch windows. 

## My Solve
**Flag:** `pwn.college{kR0NXBpN4fpyIF6f9um70e_Dw8P.0FO4IDOxwiN1kjNzEzW}`

```bash
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{kR0NXBpN4fpyIF6f9um70e_Dw8P.0FO4IDOxwiN1kjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{kR0NXBpN4fpyIF6f9um70e_Dw8P.0FO4IDOxwiN1kjNzEzW}
```

## What I learned
I learned how to switch windows in screen using `ctrl+A 0-9`

## References
The problem statement was used as the reference
```
For this challenge, we've set up a screen session with two windows:

Window 0 has... well, you'll have to switch there to find out!
Window 1 has a welcome message
Attach to the session with screen -r, then use one of the key combinations above to switch to Window 1. Go get that flag!
```

# 5.  Detaching and Attaching(tmux)
The challenge prompted me to use `tmux`. 

## My Solve
**Flag:** `pwn.college{kU-AeMVWPBlDzwhlQIi7Ebp9KF9.0VO4IDOxwiN1kjNzEzW}`

```bash
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{kU-AeMVWPBlDzwhlQIi7Ebp9KF9.0VO4IDOxwiN1kjNzEzW}
Congratulations, here is your flag: pwn.college{kU-AeMVWPBlDzwhlQIi7Ebp9KF9.0VO4IDOxwiN1kjNzEzW}
```

## What I learned
I learned how to use `tmux` to attach and detach from a session.

## References
The problem statement was used as the reference
```
For this challenge:

Launch tmux
Detach from it.
Run /challenge/run (this will send the flag to your detached session!)
Reattach to see your prize
```

# 6. Switching Windows
The challenge prompted me to switch windows using tmux.

## My Solve
**Flag:** `pwn.college{8nd3GL6b1G3q2dOt2DOnNSSgxYW.0FM5IDOxwiN1kjNzEzW}`

```bash
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{8nd3GL6b1G3q2dOt2DOnNSSgxYW.0FM5IDOxwiN1kjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{8nd3GL6b1G3q2dOt2DOnNSSgxYW.0FM5IDOxwiN1kjNzEzW}
```

## What I learned
I learned how to switch windows by using commands in tmux.

## References
The problem statement was used as the reference
```
We've created a tmux session with two windows:

Window 0 has the flag!
Window 1 has your warm welcome.
Go get that flag!
```
