# Lab 13: Linux Piping

## Objectives
- Understand how pipes (|) work in Linux
- Learn how to pass the output of one command as input to another
- Practice filtering, sorting, counting, and extracting data using pipelines
- Gain hands-on experience with common Linux text-processing commands

## Commands Practiced

| Command | Purpose |
|---|---|
| cat filename | Display the contents of a file |
| grep pattern | Search for lines containing a specific pattern |
| sort | Sort lines alphabetically or numerically |
| uniq | Remove duplicate consecutive lines |
| wc -l | Count the number of lines |
| awk '{print $1}' | Display the first column of each line |
| awk '{print $2}' | Display the second column of each line |
| | | Pipe the output of one command into another command |

## Key Concepts

- A pipe (|) connects two or more commands, sending the output of one command directly as the input of the next.
- Piping eliminates the need to create temporary files when processing data.
- grep filters matching lines from input.
- sort arranges data alphabetically (or numerically with options).
- uniq removes duplicate adjacent lines, so it is commonly used after sort.
- wc -l counts the total number of lines received from standard input.
- awk is a powerful text-processing tool that extracts specific fields from each line.
- Combining multiple commands in a pipeline allows complex data processing with simple, reusable tools.

## Practice Log

- Created fruits.txt containing multiple fruit names with duplicate entries.
- Displayed the file contents using cat fruits.txt.
- Filtered matching entries using:
  bash
  cat fruits.txt | grep APPLE
  
- Counted the number of lines using:
  bash
  cat fruits.txt | wc -l
  
- Sorted the file alphabetically using:
  bash
  cat fruits.txt | sort
  
- Removed duplicate entries using:
  bash
  cat fruits.txt | sort | uniq
  
- Created students.txt containing student names and marks.
- Filtered students with a score of 91 using:
  bash
  cat students.txt | grep 91
  
- Displayed only student names using:
  bash
  cat students.txt | awk '{print $1}'
  
- Learned that forgetting the closing single quotation (') in an awk command causes Bash to display the > secondary prompt, indicating that the command is incomplete.
- Cancelled the incomplete command using Ctrl + C and reran the correct command successfully.

## Status

✅ Lab completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/7eea253d-2cb0-4242-b910-3c917f54751a" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/8a7e318e-7a92-4dbc-951c-2ac30e094a71" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/38a976b6-ed2c-4c69-9d6a-0286b21b9e37" />


