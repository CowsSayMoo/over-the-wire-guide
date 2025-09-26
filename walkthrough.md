# Bandit Wargame Walkthrough

## Level 0

Connected to the server via `ssh -p 2220 bandit0@bandit.labs.overthewire.org`. The password for the next level was found in the `readme` file.

Password for Level 1: `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`

## Level 1

The password for Level 2 was found in a file named `-`.
Attempting to `cat -` or open with `vim -` did not work as expected. This is because many command-line utilities, including `cat`, interpret a single hyphen (`-`) as a special argument to read from standard input (stdin) rather than treating it as a filename.

To read the file literally named `-` in the current directory, the command `cat ./-` was used. The `./` explicitly tells the shell that `-` is a file in the current directory.

Password for Level 2: `263JGJPfgU6LtdEvgfWU1XP5yac29mFx`

## Level 2

The password for Level 3 was found in a file with spaces in its name.
To read this file, the spaces in the filename were escaped using a backslash (`\`).

Command used: `cat ./--spaces\ in\ this\ filename--`

Password for Level 3: `MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx`

## Level 3

The password for Level 4 was found in a hidden file. Hidden files in Unix-like systems typically start with a dot (`.`). In this case, the file was named `...Hiding-From-You`.

Command used: `cat ./...Hiding-From-You`

Password for Level 4: `2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ`

## Level 4 

I used the file command to check the type each file in the directory. If it returned output `./-file07: ASCII text`, you know that it contains regular text. In this case the password.

Password for level 5: `4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw`

## level 5 

I used the `du --all --bytes` command, this show the file size of all the files in each directory. Then i used grep to search for the number 1033.

Password for level 6: `HWasnPhtq9AVKe0dmk45nxy20cvUa6EG`

## level 6 

I used the `find / -type f -user bandit7 -group bandit6 2>/dev/null` to search the entire server for a file that matches the given parameters. And redirected the error messages, so they wouldn't clutter the output.

Password for level 7: `morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj`

## level 7

