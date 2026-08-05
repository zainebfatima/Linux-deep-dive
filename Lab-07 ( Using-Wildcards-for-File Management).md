[2:25 pm, 07/07/2026] ...: #Lab 7: Using Wildcards for File Management

##Objectives

- Understand the concept of wildcards in file management
- Learn how to use wildcards to perform various file operations efficiently
- Gain hands-on experience with commands like "cp" and "rm" using wildcards

##Commands Practiced

Command| Purpose
"pwd"| Display the current working directory
"ls"| List files and directories
"ls -l"| List files with detailed information
"mkdir directory_name"| Create a new directory
"cd directory_name"| Change to a different directory
"touch file1 file2"| Create one or more empty files
"cp *.txt backup/"| Copy all ".txt" files to the "backup" directory
"rm *.jpg"| Remove all ".jpg" files
"ls *.txt"| List all text files
"ls *.jpg"| List all JPEG image files
"ls *.pdf"| List all PDF files
"ls a?.txt"| List files where "?" matches exactly one character
"ls [ab]*"| List files starting with "a" or "b"

##Key Concepts

- "*" (asterisk) matches zero or more characters in a filename.
- "?" (question mark) matches exactly one character.
- "[ ]" (character class) matches one character from a specified set or range.
- Wildcards simplify file management by allowing operations on multiple files at once.
- Commands like "cp" and "rm" become more efficient when combined with wildcards.
- Always verify the files matched by a wildcard using "ls" before deleting them with "rm".

##Practice Log

- Created a working directory for wildcard practice.
- Created multiple files with different extensions (".txt", ".jpg", ".pdf", and ".sh") using "touch".
- Listed files using "ls" and "ls -l".
- Created a "backup" directory.
- Copied all text files into the "backup" directory using "cp *.txt backup/".
- Verified copied files using "ls backup".
- Deleted all JPEG image files using "rm *.jpg".
- Created files "a1.txt", "a2.txt", and "a10.txt" to understand the "?" wildcard.
- Verified that "ls a?.txt" matched only filenames with a single character after "a".
- Created "f1.txt" and "f4.txt" and confirmed "ls f?.txt" displayed both files.
- Created "apple.txt", "banana.txt", "cat.txt", and "dog.txt" to practice character class matching.
- Used "ls [ab]*" to display all files and directories beginning with "a" or "b", including the "backup" directory.

##Status

✅ Lab completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/2e52d07d-e497-4cd7-9455-14bae99c2287" />
