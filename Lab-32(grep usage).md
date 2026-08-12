# Day 32 — Basic Grep Usage

## Lab Objectives

- Understand the basic usage of the grep command in Linux.
- Learn how to search for strings within files and directories.
- Explore advanced options to provide context around matching lines.

## What is grep?

grep is a Linux command used to search for specific text or patterns within files.

It searches through the contents of files and displays the lines that match the given search pattern.

## Basic grep Usage

To search for a specific word inside a file:

```bash
grep "Linux" practice.txt
This searches for Linux in practice.txt and displays the matching lines.
Case-Insensitive Search
grep -i "linux" practice.txt
-i makes the search case-insensitive.
This means Linux, linux, and LINUX can all match.
Showing Line Numbers
grep -n "Linux" practice.txt
-n displays the line number where the matching text was found.
For example:
2:Linux is an operating system.
4:I am learning Linux.
Combining grep Options
Multiple options can be used together without a pipe.
grep -i -n "Saleena" employees.txt
Here:
-i → ignores uppercase/lowercase differences
-n → displays line numbers
The options can also be combined:
grep -in "Saleena" employees.txt
Context Around Matching Lines
Lines After the Match
grep -A 3 "Ayesha" employees.txt
-A 3 displays the matching line and 3 lines after it.
Lines Before the Match
grep -B 2 "Linux" practice.txt
-B 2 displays the matching line and 2 lines before it.
Lines Before and After the Match
grep -C 2 "Linux" practice.txt
-C 2 displays the matching line and 2 lines before and after it.
Recursive Search
To search through a directory and its subdirectories:
grep -r "Linux" .
-r means recursive.
The . means the current directory.
This searches for Linux in files throughout the current directory and its subdirectories.
It can produce many results because grep searches through all accessible files under that directory.
grep and Pipes
A pipe | is different from grep options.
Multiple options for the same command do not require a pipe:
grep -i -n "Linux" practice.txt
A pipe is used to send the output of one command into another command:
cat practice.txt | grep -i "linux"
In this example, cat produces the file contents and the pipe sends that output to grep.
Common grep Options
Option
Function
-i
Ignore case
-n
Show line numbers
-A
Show lines after the match
-B
Show lines before the match
-C
Show lines before and after the match
-r
Search recursively through directories
What I Learned
Today I learned how to:
Use grep to search for text in files.
Perform case-insensitive searches using -i.
Display line numbers using -n.
Combine multiple grep options.
Display context around matching lines using -A, -B, and -C.
Search recursively through directories using -r.
Understand the difference between grep options and pipes.
Use grep for practical Linux file searching.
Practice Completed
Searched for text using grep
Used case-insensitive searching
Displayed matching line numbers
Combined -i and -n
Used -A to display lines after a match
Used -B to display lines before a match
Used -C to display surrounding context
Used -r for recursive directory searching
Key Takeaway
grep is a powerful Linux command for finding specific text within files and directories. Its options allow us to control how matching results are displayed, while pipes can be used to connect grep with other commands.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/d67e4204-5a16-4857-a20f-2049fdfac63a" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/db8fe54f-af35-4e4b-8656-7a1021415b57" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/7e417e5b-7943-4ab8-8a5b-aa3bfacb6bf8" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/9b149b50-ea6c-4193-8fec-285fa1a0a7a6" />



