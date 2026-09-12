Lab 49: Introduction to Shell Variables

Objectives

- Understand what shell variables are.
- Learn how to create and use variables.
- Understand local and global variables.
- Learn about special shell variables such as "$?", "$$", and "$#".

What I Learned

1. Shell Variables

A shell variable is used to store information.

NAME=Zaineb
echo $NAME

Output:

Zaineb

The "$" is used when we want to access the value stored in a variable.

2. Changing a Variable

The value of a variable can be changed:

NAME=Ali
echo $NAME

Output:

Ali

3. Local Variable

A local variable works in the current shell.

AGE=18
echo $AGE

4. Global / Environment Variable

Using "export" makes a variable available to programs started from the current shell.

export CITY=Lahore
echo $CITY

Output:

Lahore

5. Special Variable: "$?"

"$?" shows the exit status of the previous command.

If the command worked:

ls
echo $?

Output:

0

"0" means the command was successful.

If the command failed:

ls /doesnotexist
echo $?

Output:

2

A number other than "0" means the command had an error.

6. Special Variable: "$$"

"$$" shows the process ID of the current shell.

echo $$

Example output:

2944

The number can be different on different systems or sessions.

7. Special Variable: "$#"

"$#" tells us how many arguments were given to a script.

Example script:

#!/bin/bash
echo "Number of arguments: $#"

After making it executable:

chmod +x test.sh

Running without arguments:

./test.sh

Output:

Number of arguments: 0

Running with three arguments:

./test.sh apple banana mango

Output:

Number of arguments: 3

Key Takeaways

Variable| Meaning
"$NAME"| Gets the value stored in "NAME"
"$?"| Shows whether the previous command succeeded or failed
"$$"| Shows the current shell's process ID
"$#"| Counts the arguments given to a script

Final Understanding

Shell variables allow us to store and reuse information. Special variables give the shell useful information about commands, processes, and scripts.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/e0bad0b4-3ce8-4bb2-ad15-2f4539fc0ce5" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/b070a7b3-8741-4639-bc2f-6601e7b05b97" />

