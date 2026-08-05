[2:22 pm, 13/07/2026] ...: # Lab 12: Basic Shell Scripting

## Objectives
- Understand the basics of shell scripting
- Learn how to write, make executable, and run a simple shell script
- Gain experience with Linux command-line operations

## Commands Practiced

| Command | Purpose |
|---|---|
| nano script.sh | Create/edit a shell script file |
| chmod +x script.sh | Make a script executable |
| ./script.sh | Run a script from the current directory |
| read variable | Take user input into a variable inside a script |
| #!/bin/bash | Shebang line, tells the system which shell to run the script with |

## Key Concepts
- A shell script is a text file containing a sequence of commands that 
  run automatically, instead of typing each one manually
- The shebang line (#!/bin/bash) at the top of a script specifies 
  which shell interpreter should execute it
- A script must have execute permission (chmod +x) before it can be 
  run directly
- ./script.sh is required (not just script.sh) to explicitly tell 
  the shell to run the file from the current directory
- Scripts can use variables and take user input via read, combining 
  concepts from earlier labs (Lab 5: permissions, Lab 7: wildcards, 
  Lab 11: environment variables)
- Real-world use cases: automating repetitive tasks, backups, system 
  administration, and — relevant to cybersecurity — reconnaissance and 
  scanning scripts that chain multiple commands together

## Practice Log
- Wrote myscript.sh: printed a greeting and the current date using 
  echo and date
- Made it executable with chmod +x and ran it with ./myscript.sh — 
  confirmed correct output including live system date
- Wrote myscript2.sh: added read to accept user input (name) and 
  used it inside a variable — confirmed working interactive script
- Wrote backup.sh: automated a basic backup task —
  - mkdir -p backup creates a backup folder
  - cp *.txt backup/ copies all matching files into it using a wildcard
  - echo + date confirm completion
- First run failed with `cp: cannot stat '*.md': No such file or 
  directory` — no .md files existed in that directory. Edited the 
  script with nano to match *.txt instead, created test files 
  (test1.txt, test2.txt, test3.txt), reran successfully
- Verified the backup with ls backup/ — confirmed copies existed both 
  in the original location and inside backup/, demonstrating the core 
  purpose of a backup: a duplicate safety copy in case the original is 
  lost or deleted

## Status
✅ Lab completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/1763830c-5719-4eef-91c4-29759752816d" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/562a19e1-2556-40c4-85c3-52668e7680cd" />

