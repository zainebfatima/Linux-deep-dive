Lab 46: Using the "history" Command

Objectives

- Understand the purpose and utility of the "history" command.
- Learn to view previously executed commands.
- Execute previous commands using their history numbers.
- Learn how to clear the command history.

What I Learned

The "history" command displays commands that were previously entered in the Bash shell.

Each command is assigned a history number, which can be used to execute that command again.

Commands Practiced

View Command History

history

This displays previously executed commands with their history numbers.

Execute a Previous Command

!12

This executes the command stored at history number "12".

For example, if history number 12 contains:

source ~/.bashrc

then:

!12

runs that command again.

Clear Command History

history -c

This clears the current shell's command history list.

Practical Practice

I used:

history

to view my commands, then used history numbers such as:

!13
!12

to execute previous commands.

Finally, I cleared the history using:

history -c

and verified it with:

history

Key Takeaway

The "history" command is useful for viewing and reusing previously executed commands without having to type them again.

Lab Status: Completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/3a8463d2-b078-424e-99ba-d2f228fc2c9b" />
