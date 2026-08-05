[2:59 pm, 10/07/2026] ...: # Lab 10: Understanding Shells

## Objectives
- Understand the concept and purpose of a shell in Unix-like operating systems
- Learn how to check the default shell for a user
- List and identify available shells on a system
- Practice switching between different shells

## Commands Practiced

| Command | Purpose |
|---|---|
| echo $SHELL | Show the user's default configured shell |
| echo $0 | Show which shell is actively running the current session |
| cat /etc/shells | List all shells installed and available on the system |
| grep $USER /etc/passwd | Look up the user's account record, including assigned shell |
| sh | Switch into the sh shell |
| bash / exit | Return to the bash shell |

## Key Concepts
- A *shell* is the program that reads and executes the commands typed 
  into the terminal — it's the interpreter between the user and Linux
- $SHELL shows the default shell assigned to the user account, while 
  $0 shows what shell is actually running the current session — these 
  can differ if a user manually switches shells
- /etc/shells lists every valid, installed shell on the system, not 
  just the one currently in use
- /etc/passwd stores each user's account details, including their 
  assigned login shell as the last field on their line
- Multiple shells can exist on one system (bash, sh, rbash, dash, etc.) 
  and a user can switch between them temporarily using the shell's name 
  as a command, then return with exit or by launching the previous 
  shell directly

## Practice Log
- Confirmed default shell: echo $SHELL returned /bin/bash
- Confirmed active shell: echo $0 returned bash
- Listed available shells via cat /etc/shells: found /bin/sh, 
  /bin/bash, /bin/rbash, /usr/bin/dash, among others
- Verified account-level shell assignment via grep $USER /etc/passwd: 
  confirmed /bin/bash as the assigned shell
- Switched into sh using the sh command, confirmed the switch with 
  echo $0 returning sh
- Returned to bash using exit, reconfirmed with echo $0

## Status
✅ Lab completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/72aa7d83-b353-4f80-aa4f-8ab297ab2944" />
