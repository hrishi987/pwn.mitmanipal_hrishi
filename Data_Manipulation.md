# 1. Translating characters
The challenge prompted me to use `tr` command.

## My Solve
**Flag:** `pwn.college{YOXbv6DoQbMhPuSVaj_z6EefNlm.01MxEzNxwiN1kjNzEzW}`

```bash
hacker@data~translating-characters:~$ /challenge/run | tr PWNCOLEGBVHUJAZFMXIKyoxdqmpsvenw pwncolegbvhujazfmxikYOXDQMPSVENW
YOur caSE-SWaPPED flag:
pwn.college{YOXbv6DoQbMhPuSVaj_z6EefNlm.01MxEzNxwiN1kjNzEzW}
```

## What I learned
I learned how to use `tr` along with piping to translate characters in stdout stream.

## References
The problem statement was used as the reference
```
Now, you try it! In this level, /challenge/run will print the flag but will swap the casing of all characters (e.g., A will become a and vice-versa). Can you undo it with tr and get the flag?
```

# 2. Deleting characters
The challenge prompted me to use `tr` command along with `-d` argument. 

## My Solve
**Flag:** `pwn.college{Y7AK1EpmbchO7Zl5_eCeMhPZOCZ.0FNxEzNxwiN1kjNzEzW}`

```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{Y7AK1EpmbchO7Zl5_eCeMhPZOCZ.0FNxEzNxwiN1kjNzEzW}
```

## What I learned
I learned how to delete characters from output using `tr -d`.

## References
The problem statement was used as the reference
```
Pretty simple! Now you give it a try. I'll intersperse some decoy characters (specifically: ^ and %) among the flag characters. Use tr -d to remove them!
```

# 3. Deleting newlines
The challenge prompted me to delete new lines from the flag. 

## My Solve
**Flag:** `pwn.college{AkqGVNO7Z-3WzKTGYVZH8eXY49R.0VNxEzNxwiN1kjNzEzW}`

```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{AkqGVNO7Z-3WzKTGYVZH8eXY49R.0VNxEzNxwiN1kjNzEzW}hacker@data~deleting-newlines:~$
```

## What I learned
I learned how to use `tr` command to spot and delete new lines from string.

## References
The problem statement was used as the reference
```
Now, let's combine this with deletion. In this challenge, we'll inject a bunch of newlines into the flag. Delete them with tr's -d flag and the escaped newline specification!
```

# 4. Extracting the first lines with head
The challenge prompted me to use `head` command. 

## My Solve
**Flag:** `pwn.college{4DPemJqJ9qBa9TCIerCXsetRRu-.0lNxEzNxwiN1kjNzEzW}`

```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{4DPemJqJ9qBa9TCIerCXsetRRu-.0lNxEzNxwiN1kjNzEzW}
```

## What I learned
I learned how to use `head` command to fetch first n lines of the output.

## References
The problem statement was used as the reference
```
This challenge's /challenge/pwn outputs a bunch of data, and you'll need to pipe it through head to grab just the first 7 lines and then pipe them onwards to /challenge/college, which will give you the flag if you do this right! Your solution will be a long composite command with two pipes connecting three commands. Good luck!
```

# 5.  Extracting specific sections of text
The challenge prompted me to use `cut` command. 

## My Solve
**Flag:** `pwn.college{c3BW3hpXC3gLICkg5k_SI-nE8mM.01NxEzNxwiN1kjNzEzW}`

```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{c3BW3hpXC3gLICkg5k_SI-nE8mM.01NxEzNxwiN1kjNzEzW}hacker@data~extracting-specific-sections-of-text:~$
```

## What I learned
I learned how to use `cut` command to separate text with columns.

## References
The problem statement was used as the reference
```
In this challenge, the /challenge/run program will give you a bunch of lines with random numbers and single characters (characters of the flag) as columns. Use cut to extract the flag characters, then pipe them to tr -d "\n" (like the previous level!) to join them together into a single line. Your solution will look something like /challenge/run | cut ??? | tr ???, with the ??? filled out.
```

# 6. Sorting data
The challenge prompted me to use `sort` command. 

## My Solve
**Flag:** `pwn.college{ULTyoG-Tzdvr7LJ1CDGweOzjnAZ.0FM0MDOxwiN1kjNzEzW}`

```bash
hacker@data~sorting-data:~$ sort /challenge/flags.txt
....
pwn.college{ULTyoG-Tzdvr7LJ1CDGweOzjnAZ.0FM0MDOxwiN1kjNzEzW}
```

## What I learned
I learned how to use `sort` command to sort words in a file/input in alphabetical and various other orders.

## References
The problem statement was used as the reference
```
In this challenge, there's a file at /challenge/flags.txt containing 100 fake flags, with the real flag mixed among them. When sorted alphabetically, the real flag will be at the end (we made sure of this when generating fake flags). Go get it!
```
