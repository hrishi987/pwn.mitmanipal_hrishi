# 1. Chaining with Semicolons
The challenge prompted me to use `;`.

## My Solve
**Flag:** `pwn.college{4bMPhgua86N3EBLU5ONYRryEoP4.QX1UDO0wiN1kjNzEzW}`

```bash
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{4bMPhgua86N3EBLU5ONYRryEoP4.QX1UDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `;` to run multiple commands in the same line.

## References
The problem statement was used as the reference
```
Give it a try now! In this level, you must run /challenge/pwn and then /challenge/college, chaining them with a semicolon.
```

# 2. Building on Success
The challenge prompted me to use `&&` 

## My Solve
**Flag:** `pwn.college{gYfgEJv9VeI5-6J1ltZtdm0jkVT.0lM0MDOxwiN1kjNzEzW}`

```bash
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second
Nice chaining! Flag: pwn.college{gYfgEJv9VeI5-6J1ltZtdm0jkVT.0lM0MDOxwiN1kjNzEzW}
```

## What I learned
I learned how to use `&&` to run second command if first succeeds.

## References
The problem statement was used as the reference
```
In this challenge, you need to chain the programs /challenge/first-success and /challenge/second using the && operator. Try running each command separately first to see what happens (which is that you will not get the flag). But if you chain them with &&, the flag will appear!
```

# 3. Handling Failure
The challenge prompted me to use `||`.

## My Solve
**Flag:** `pwn.college{0bF_DcausWQPKkh_1qZcosWKitX.01M0MDOxwiN1kjNzEzW}`

```bash
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{0bF_DcausWQPKkh_1qZcosWKitX.01M0MDOxwiN1kjNzEzW}
```

## What I learned
I learned how to use `||` to run second command if first fails.

## References
The problem statement was used as the reference
```
In this challenge, you need to chain /challenge/first-failure and /challenge/second using the || operator. Go for it!
```

# 4. Your First Shell Script
The challenge prompted me to make .sh file.

## My Solve
**Flag:** `pwn.college{8hccteWaDAes1MGeWX6yZ_3g-J2.QXxcDO0wiN1kjNzEzW}`

```bash
hacker@chaining~your-first-shell-script:~$ nano x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{8hccteWaDAes1MGeWX6yZ_3g-J2.QXxcDO0wiN1kjNzEzW}
```

## What I learned
I learned how to make and execute a shell script.

## References
The problem statement was used as the reference
```
Now, it's your turn! Same as last level, run /challenge/pwn and then /challenge/college, but this time in a shell script called x.sh, then run it with bash!
```

# 5.  Redirecting Script Output
The challenge prompted me to redirect script output. 

## My Solve
**Flag:** `pwn.college{kT8TDZnFNZaRwcdCfNMwoxbsLnw.QX4ETO0wiN1kjNzEzW}`

```bash
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{kT8TDZnFNZaRwcdCfNMwoxbsLnw.QX4ETO0wiN1kjNzEzW}
```

## What I learned
I learned how to pipe output of a bash scipt to a command.

## References
The problem statement was used as the reference
```
In this level, we will practice piping (|) from your script to another program. Like before, you need to create a script that calls the /challenge/pwn command followed by the /challenge/college command, and pipe the output of the script into a single invocation of the /challenge/solve command!
```

# 6. Executable Shell Scripts
The challenge prompted me to make an executable shell script.

## My Solve
**Flag:** `pwn.college{YlKqFAf1TDEVqNFIfTDu_N2dnkf.QX0cjM1wiN1kjNzEzW}`

```bash
hacker@chaining~executable-shell-scripts:~$ chmod u+x x.sh
hacker@chaining~executable-shell-scripts:~$ ./x.sh
Congratulations on your shell script execution! Your flag:
pwn.college{YlKqFAf1TDEVqNFIfTDu_N2dnkf.QX0cjM1wiN1kjNzEzW}
```

## What I learned
I learned how to make a shell script which is executable without using `bash` command.

## References
The problem statement was used as the reference
```
Try that here! Make a shellscript that will invoke /challenge/solve, make it executable, and run it without explicitly invoking bash!
```

# 7. Understanding Shebangs
The challenge prompted me to use shebangs.

## My Solve
**Flag:** `pwn.college{0v-JXwwVVQfjigoSEV_SXgjOO8_.0VOzMDOxwiN1kjNzEzW}`

```bash
hacker@chaining~understanding-shebangs:~$ chmod a+x ~/solve.sh
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{0v-JXwwVVQfjigoSEV_SXgjOO8_.0VOzMDOxwiN1kjNzEzW}
```

## What I learned
I learned how to use use `shebangs` at the top of bash scripts.

## References
The problem statement was used as the reference
```
For this challenge, create a script at /home/hacker/solve.sh that has a proper shebang and outputs "hack the planet". Remember to make it executable, then run /challenge/run to verify your script works correctly!
```

# 8. Scripting with Arguments
The challenge prompted me to use arguments in the script. 

## My Solve
**Flag:** `pwn.college{cXyw1YvbXYgkB2yKKlL_J0Pdlt8.0VNzMDOxwiN1kjNzEzW}`

```bash
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{cXyw1YvbXYgkB2yKKlL_J0Pdlt8.0VNzMDOxwiN1kjNzEzW}
```

## What I learned
I learned how to use arguments in my bash script.

## References
The problem statement was used as the reference
```
For this challenge, you need to write a script at /home/hacker/solve.sh that:

Takes two arguments
Outputs them in REVERSE order (second argument first, then the first argument)
```

# 9. Scripting with Conditionals
The challenge prompted me if conditionals.

## My Solve
**Flag:** `pwn.college{ADlV3isJCM05Al1msjoJfl1iVpl.0lNzMDOxwiN1kjNzEzW}`

```bash
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{ADlV3isJCM05Al1msjoJfl1iVpl.0lNzMDOxwiN1kjNzEzW}
```

## What I learned
I learned how to use `if conditionals` in bash script.

## References
The problem statement was used as the reference
```
For this challenge, write a script at /home/hacker/solve.sh that:

Takes one argument
If the argument is "pwn", output "college"
For any other input, output nothing
```

# 10. Scripting with Default Cases
The challenge prompted me to if-else conditional.

## My Solve
**Flag:** `pwn.college{wsSmYKth9P2fP_Lr2F3_tDs4dZG.01NzMDOxwiN1kjNzEzW}`

```bash
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{wsSmYKth9P2fP_Lr2F3_tDs4dZG.01NzMDOxwiN1kjNzEzW}
```

## What I learned
I learned how to use `if-else` conditionals in bash script.

## References
The problem statement was used as the reference
```
For this challenge, write a script at /home/hacker/solve.sh that:

Takes one argument
If the argument is "pwn", output "college"
For any other input, output "nope"
```

# 11. Scripting with Multiple Conditions
The challenge prompted me to use the if-elif conditionals.

## My Solve
**Flag:** `pwn.college{I-4wMlgOT3ticnQf_APmQMyObzU.0FOzMDOxwiN1kjNzEzW}`

```bash
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{I-4wMlgOT3ticnQf_APmQMyObzU.0FOzMDOxwiN1kjNzEzW}
```

## What I learned
I learnt how to use `if-elif` conditionals in bash script.

## References
The problem statement was used as the reference
```
For this challenge, write a script at /home/hacker/solve.sh that:

Takes one argument
If the argument is "hack", output "the planet"
If the argument is "pwn", output "college"
If the argument is "learn", output "linux"
For any other input, output "unknown"
```

# 12. Reading Shell Scripts
The challenge prompted me to read code of a shell script

## My Solve
**Flag:** `pwn.college{k7xWAUsw66zkBdR07gimcSQjDrx.0lMwgDOxwiN1kjNzEzW}`

```bash
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{k7xWAUsw66zkBdR07gimcSQjDrx.0lMwgDOxwiN1kjNzEzW}
```

## What I learned
I learnt how to read the code of a shell script.

## References
The problem statement was used as the reference
```
In this level, we will learn to read shell scripts. /challenge/run is a shell script that requires you to put in a secret password, but that password is hardcoded into the script iself! Read the script (using, say, cat), figure out the password, and get the flag!
```