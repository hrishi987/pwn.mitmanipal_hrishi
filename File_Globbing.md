# 1. Matching with *
The challenge prompted me to use `*` glob. 

## My Solve
**Flag:** `pwn.college{odirKXV5ubnF9yYPFCRbQ1VucAn.QXxIDO0wiN1kjNzEzW}`

```bash
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{odirKXV5ubnF9yYPFCRbQ1VucAn.QXxIDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `*` glob which replaces itself with any matching file name.

## References
The problem statement was used as the reference
```
Now, practice this yourself! Starting from your home directory, change your directory to /challenge, but use globbing to keep the argument you pass to cd to at most four characters! Once you're there, run /challenge/run for the flag!
```

# 2. Matching with ?
The challenge prompted me to use `?` glob. 

## My Solve
**Flag:** `pwn.college{A5aNF02fFE--idfyiUXe4-zl4_T.QXyIDO0wiN1kjNzEzW}`

```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{A5aNF02fFE--idfyiUXe4-zl4_T.QXyIDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `?` glob which replaces itself with any matching character.

## References
The problem statement was used as the reference
```
Now, practice this yourself! Starting from your home directory, change your directory to /challenge, but use the ? character instead of c and l in the argument to cd! Once you're there, run /challenge/run for the flag!
```

# 3. Matching with []   
The challenge prompted me to use `[]` glob. 

## My Solve
**Flag:** `pwn.college{8fQuaOwVz6NVdg08Jkea-n0jg4-.QXzIDO0wiN1kjNzEzW}`

```bash
hacker@globbing~matching-with-:/challenge$ cd files/
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{8fQuaOwVz6NVdg08Jkea-n0jg4-.QXzIDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `[]` glob which replaces itself with limited specified characters.

## References
The problem statement was used as the reference
```
Try it here! We've placed a bunch of files in /challenge/files. Change your working directory to /challenge/files and run /challenge/run with a single argument that bracket-globs into file_b, file_a, file_s, and file_h!
```

# 4. Matching paths with []
The challenge prompted me to use `[]` glob for path matching.

## My Solve
**Flag:** `pwn.college{QlHDomKTPwCzJUjDs6tg7aX57Qo.QX0IDO0wiN1kjNzEzW}`

```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{QlHDomKTPwCzJUjDs6tg7aX57Qo.QX0IDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use `[]` glob which replaces itself with limited specified characters for path matching    .

## References
The problem statement was used as the reference
```
Now it's your turn. Once more, we've placed a bunch of files in /challenge/files. Starting from your home directory, run /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files!
```

# 5. Multiple globs
The challenge prompted me to use multiple globs. 

## My Solve
**Flag:** `pwn.college{cjXGO5l1YIyX35xpTxGr89yPDsO.0lM3kjNxwiN1kjNzEzW}`

```bash
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{cjXGO5l1YIyX35xpTxGr89yPDsO.0lM3kjNxwiN1kjNzEzW}
```

## What I learned
I learned to use multiple globs in a single command.

## References
The problem statement was used as the reference
```
Now you try it. We put a few happy, but diversely-named files in /challenge/files. Go cd there and run /challenge/run, providing a single argument: a short (3 characters or less) globbed word with two * globs in it that covers every word that contains the letter p.
```

# 6. Mixing Globs
The challenge prompted me to use the `globs`. 

## My Solve
**Flag:** `pwn.college{oq_21RnEOL99evVVMMPlecTmp7O.QX1IDO0wiN1kjNzEzW}`

```bash
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{oq_21RnEOL99evVVMMPlecTmp7O.QX1IDO0wiN1kjNzEzW}
```

## What I learned
I learned how to use multiple globs in a single command.

## References
The problem statement was used as the reference
```
Now, let's put the previous levels together! We put a few happy, but diversely-named files in /challenge/files. Go cd there and, using the globbing you've learned, write a single, short (6 characters or less) glob that (when passed as an argument to /challenge/run) will match the files "challenging", "educational", and "pwning"!
```

# 7. Exclusionary globbing
The challenge prompted me to use the `[!]`  command. 

## My Solve
**Flag:** `pwn.college{kka7xainZy9_1WKIAGp7VI8h809.QX2IDO0wiN1kjNzEzW}`

```bash
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{kka7xainZy9_1WKIAGp7VI8h809.QX2IDO0wiN1kjNzEzW}
```

## What I learned
I learned to use [!] to get the files which don't start with specific characters.

## References
The problem statement was used as the reference
```
NOTE: The ! character has a different special meaning in bash when it's not the first character of a [] glob, so keep that in mind if things stop making sense! ^ does not have this problem, but is also not compatible with older shells.
```

# 8. Tab completion
The challenge prompted me to use tab completion. 

## My Solve
**Flag:** `pwn.college{01c-IynMEs-g-_8_qcn5uzgJAXH.0FN0EzNxwiN1kjNzEzW}`

```bash
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege
pwn.college{01c-IynMEs-g-_8_qcn5uzgJAXH.0FN0EzNxwiN1kjNzEzW}
```

## What I learned
I learned to use tab to autocomplete my file names.

## References
The problem statement was used as the reference
```
When you hit that tab key, the name will expand and you'll be able to read the file. Good luck!
```
# 9. Multiple options for tab completion
The challenge prompted me to use tab completion. 

## My Solve
**Flag:** `pwn.college{4FqGXY8F8znANY3PgZSYF29Yxaf.0lN0EzNxwiN1kjNzEzW}`

```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{4FqGXY8F8znANY3PgZSYF29Yxaf.0lN0EzNxwiN1kjNzEzW}
```

## What I learned
I learned to use tab to autocomplete my file names.

## References
The problem statement was used as the reference
```
This challenge has a /challenge/files directory with a bunch of files starting with pwncollege. Tab-complete from /challenge/files/p or so, and make your way to the flag!
```

# 10. Tab completion on commands
The challenge prompted me to use tab completion on commands. 

## My Solve
**Flag:** `pwn.college{Eo8mQ-tgcJVrf-aUo395WUISlXW.0VN0EzNxwiN1kjNzEzW}`

```bash
hacker@globbing~tab-completion-on-commands:~$ pwncollege-31941
Correct! Here is your flag:
pwn.college{Eo8mQ-tgcJVrf-aUo395WUISlXW.0VN0EzNxwiN1kjNzEzW}
```

## What I learned
I learned to use tab to autocomplete my commands.

## References
The problem statement was used as the reference
```
Tab completion is for more than files! You can also tab-complete commands. This level has a command that starts with pwncollege, and it'll give you the flag. Type pwncollege and hit the tab key to auto-complete it!
```



