Lab 46: Bash Profile vs. Bashrc

Objectives

- Understand the difference between ".bash_profile" and ".bashrc".
- Learn how to customize the Bash shell environment.
- Practice creating aliases and environment variables.

What I Learned

Bash

Bash (Bourne Again Shell) is a command-line shell and interpreter that allows users to interact with the Linux operating system using commands.

".bashrc"

".bashrc" is a configuration file used by Bash for interactive shells. It can be used to save:

- Aliases (command shortcuts)
- Environment variables
- Other Bash customizations

".bash_profile"

".bash_profile" is mainly used for login-shell configuration. It can contain environment variables and other settings that should be applied when logging in.

".bash_logout"

".bash_logout" can contain commands that Bash executes when a login shell exits.

Commands Practiced

Check Current Shell

echo $SHELL

Output:

/bin/bash

View Bash Configuration Files

ls -la ~ | grep bash

View ".bashrc"

cat ~/.bashrc

Create an Environment Variable

export MY_NAME="Zaineb"

Check its value:

echo $MY_NAME

Create an Alias

alias ec='echo $MY_NAME'

Now simply running:

ec

prints:

Zaineb

Save Settings in ".bashrc"

Open the file:

nano ~/.bashrc

Add:

export MY_NAME="Zaineb"
alias ec='echo $MY_NAME'

Then reload ".bashrc":

source ~/.bashrc

Remove an Alias

unalias ec

Remove an Environment Variable

unset MY_NAME

Key Takeaway

".bashrc" can be used as Bash's saved settings file. It allows us to save aliases, environment variables, and other shell customizations so Bash can load them when using an interactive shell.

Lab Status: Completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/9e06f26b-e21f-4e50-9666-16fa3ec2027d" />
