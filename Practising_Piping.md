# 1. Redirecting output
The challenge prompted me to stdout to files. 

## My Solve
**Flag:** `pwn.college{YBLlETKeUlPSs1u619KHv_sDURL.QX0YTN0wiN1kjNzEzW}`

```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{YBLlETKeUlPSs1u619KHv_sDURL.QX0YTN0wiN1kjNzEzW}
```

## What I learned
I learned how to use `>` to output to files.

## References
The problem statement was used as the reference
```
In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).
```

# 2. Redirecting more output
The challenge prompted me to redirect output. 

## My Solve
**Flag:** `pwn.college{YnfBumF93ay9l_6LWDgD3wkoYeU.QX1YTN0wiN1kjNzEzW}`

```bash
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{YnfBumF93ay9l_6LWDgD3wkoYeU.QX1YTN0wiN1kjNzEzW}
```

## What I learned
I learned how to use `>` to output to files.

## References
The problem statement was used as the reference
```
Aside from redirecting the output of echo, you can, of course, redirect the output of any command. In this level, /challenge/run will once more give you a flag, but only if you redirect its output to the file myflag. Your flag will, of course, end up in the myflag file!
```

# 3. Appending output
The challenge prompted me to append output to an existing file. 

## My Solve
**Flag:** `pwn.college{0EGpWjqmTSfmER5ispcIfEsLLlc.QX3ATO0wiN1kjNzEzW}`

```bash
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
 |
\|/ This is the first half:
 v
pwn.college{0EGpWjqmTSfmER5ispcIfEsLLlc.QX3ATO0wiN1kjNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
```

## What I learned
I learned how to use `>>` to append output to an already existing file.

## References
The problem statement was used as the reference
```
To practice, run /challenge/run with an append-mode redirect of the output to the file /home/hacker/the-flag. The practice will write the first half of the flag to the file, and the second half to stdout if stdout is redirected to the file. If you properly redirect in append-mode, the second half will be appended to the first, but if you redirect in truncation mode (>), the second half will overwrite the first and you won't get the flag!
```

# 4. Redirecting errors
The challenge prompted me to redirect errors to a file. 

## My Solve
**Flag:** `pwn.college{Aazz42jS3H0suf5JNkUILfGSdPk.QX3YTN0wiN1kjNzEzW}`

```bash
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{Aazz42jS3H0suf5JNkUILfGSdPk.QX3YTN0wiN1kjNzEzW}
```

## What I learned
I learned how to use `File Descriptor numbers` to redirect output and errors to multiple files.

## References
The problem statement was used as the reference
```
Let's put this into practice! In this challenge, you will need to redirect the output of /challenge/run, like before, to myflag, and the "errors" (in our case, the instructions) to instructions. You'll notice that nothing will be printed to the terminal, because you have redirected everything! You can find the instructions/feedback in instructions and the flag in myflag when you successfully pull this off!
```

# 5.  Redirecting input
The challenge prompted me to redirect input. 

## My Solve
**Flag:** `pwn.college{E7YBBON05T3g-TRaQSQNXosQGsq.QXwcTN0wiN1kjNzEzW}`

```bash
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{E7YBBON05T3g-TRaQSQNXosQGsq.QXwcTN0wiN1kjNzEzW}
```

## What I learned
I learned how to use `<` to redirect input from a file to command.

## References
The problem statement was used as the reference
```
You can do interesting things with a lot of different programs using input redirection! In this level, we will practice using /challenge/run, which will require you to redirect the PWN file to it and have the PWN file contain the value COLLEGE! To write that value to the PWN file, recall the prior challenge on output redirection from echo!
```

# 6. Grepping stored results
The challenge prompted me to redirect output and use the grep command in combination. 

## My Solve
**Flag:** `pwn.college{EPT_4wGhm7CWQKqyK_vcaJbJkx8.QX4EDO0wiN1kjNzEzW}`

```bash
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{EPT_4wGhm7CWQKqyK_vcaJbJkx8.QX4EDO0wiN1kjNzEzW}
```

## What I learned
I learned how to do a more complex task by redirecting output and using grep to search for data.

## References
The problem statement was used as the reference
```
In preparation for more complex levels, we want you to:

Redirect the output of /challenge/run to /tmp/data.txt.
This will result in a hundred thousand lines of text, with one of them being the flag, in /tmp/data.txt.
grep that for the flag!
```

# 7. Grepping live output
The challenge prompted me to use the `|` operator. 

## My Solve
**Flag:** `pwn.college{oIz-UQO-t_Il9D7xDBw1iX0KMIw.QX5EDO0wiN1kjNzEzW}`

```bash
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{oIz-UQO-t_Il9D7xDBw1iX0KMIw.QX5EDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `|` to read input to a command from the output of previous command without storing it.

## References
The problem statement was used as the reference
```
Now try it for yourself! /challenge/run will output a hundred thousand lines of text, including the flag. grep for the flag!
```

# 8. Grepping errors
The challenge prompted me to use the `>&` operator. 

## My Solve
**Flag:** `pwn.college{cmKzloq8bSZgXp2AsvdtmT-snDA.QX1ATO0wiN1kjNzEzW}`

```bash
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{cmKzloq8bSZgXp2AsvdtmT-snDA.QX1ATO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `>&` to redirect stderr to stdout and grep through it for the flag.

## References
The problem statement was used as the reference
```
Try it now! Like the last level, this level will overwhelm you with output, but this time on standard error. grep through it to find the flag!
```

# 9. Filtering with grep -v
The challenge prompted me to use the `grep -v` command. 

## My Solve
**Flag:** `pwn.college{AAavdmtgBMsxMkmeB9hXNTZ5eK3.0VOxEzNxwiN1kjNzEzW}`

```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{Mp7G2F2VqIVa7WdNnI1TOClcsgI.0FOxEzNxwiN1kjNzEzW}
```

## What I learned
I learned how to use `grep -v` command to filter out text with the argument provided.

## References
The problem statement was used as the reference
```
Use grep -v to filter out all the lines containing "DECOY" and reveal the real flag!
```

# 10. Duplicating piped data with tee
The challenge prompted me to use the `tee` command. 

## My Solve
**Flag:** `pwn.college{QCO1h9OT6pDb7fV4nK8HUlGzzqQ.QXxITO0wiN1kjNzEzW}`

```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret "QCO1h9OT" | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{QCO1h9OT6pDb7fV4nK8HUlGzzqQ.QXxITO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `tee` command to intercept a pipe and store output to a file.

## References
The problem statement was used as the reference
```
Now, you try it! This process' /challenge/pwn must be piped into /challenge/college, but you'll need to intercept the data to see what pwn needs from you!
```

# 11. Process substitution for input
The challenge prompted me to use the `diff` command with `Process Substitution`. 

## My Solve
**Flag:** `pwn.college{I4xMBmzVE_nWsK-8PhKcQTmE2iH.0lNwMDOxwiN1kjNzEzW}`

```bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
8a9
> pwn.college{I4xMBmzVE_nWsK-8PhKcQTmE2iH.0lNwMDOxwiN1kjNzEzW}
```

## What I learned
I learnt how to use Process Substitution to give command outputs as file arguments to other commands using `<(command)`.

## References
The problem statement was used as the reference
```
Now for your challenge! Recall what you learned in the diff challenge from Comprehending Commands. In that challenge, you diffed two files. Now, you'll diff two sets of command outputs: /challenge/print_decoys, which will print a bunch of decoy flags, and /challenge/print_decoys_and_flag which will print those same decoys plus the real flag.

Use process substitution with diff to compare the outputs of these two programs and find your flag!
```

# 12. Writing to multiple programs
The challenge prompted me to use the duplicate commands and use process substitution.

## My Solve
**Flag:** `pwn.college{sojjsvaB7AUffVvbsLgrEZlGxOJ.QXwgDN1wiN1kjNzEzW}`

```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) | /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{sojjsvaB7AUffVvbsLgrEZlGxOJ.QXwgDN1wiN1kjNzEzW}
```

## What I learned
I learnt how to duplicate output for a command using tee and process substitution.

## References
The problem statement was used as the reference
```
Now it's your turn! In this challenge, we have /challenge/hack, /challenge/the, and /challenge/planet. Run the /challenge/hack command, and duplicate its output as input to both the /challenge/the and the /challenge/planet commands! Scroll back through the previous challenges "Duplicating piped data with tee" and "Process substitution for input" if you need a refresher on this method.
```

# 13. Split-piping stderr and stdout
The challenge prompted me to do a more complex task.

## My Solve
**Flag:** `pwn.college{sGEo0-4b6gsqrIL97u9kOiN6czd.QXxQDM2wiN1kjNzEzW}`

```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{sGEo0-4b6gsqrIL97u9kOiN6czd.QXxQDM2wiN1kjNzEzW}
```

## What I learned
I learned how to redirect stderr and stdout of a program to different programs independently.

## References
The problem statement was used as the reference
```
In this challenge, you have:

/challenge/hack: this produces data on stdout and stderr
/challenge/the: you must redirect hack's stderr to this program
/challenge/planet: you must redirect hack's stdout to this program
Go get the flag!
```

# 14. Named pipes
The challenge prompted me to use `mkfifo` command to create named FIFOs.

## My Solve
**Flag:** `pwn.college{4zpwAv2EKKC3mOe5OjTbaRXlIB-.01MzMDOxwiN1kjNzEzW}`

```bash
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo 
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{4zpwAv2EKKC3mOe5OjTbaRXlIB-.01MzMDOxwiN1kjNzEzW}

```

## What I learned
I learned how to use the `mkfifo` command to create FIFO pipe and use it to solve the problem.

## References
The problem statement was used as the reference
```
This challenge will be a simple introduction to FIFOs. You'll need to create a /tmp/flag_fifo file and redirect the stdout of /challenge/run to it. If you're successful, /challenge/run will write the flag into the FIFO! Go do it!

```