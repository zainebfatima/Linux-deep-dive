# Lab 8: Viewing File Contents

## Objectives
- Familiarize with basic commands for viewing file contents in a Linux terminal
- Learn how to extract and search for specific text within files
- Understand the differences and use cases of head, tail, more, and grep commands

## Commands Practiced

| Command | Purpose |
|---|---|
| cat filename | Display entire file content at once |
| more filename | View file page-by-page (Space = next page, q = quit) |
| head filename | Show first 10 lines of a file |
| tail filename | Show last 10 lines of a file |
| grep "word" filename | Search for lines containing a specific word |
| grep -i "word" filename | Case-insensitive search (matches Hello and hello) |

## Key Concepts
- cat dumps the whole file immediately; more shows it screen-by-screen, 
  useful for long files
- grep scans a file and prints only the lines containing the matched 
  text — everything else is hidden from output
- grep highlights the matched word/text within the output line
- grep is case-sensitive by default — "Hello" and "hello" are treated as 
  different; use -i flag to ignore case
- Reinforced from Lab 3: > overwrites file content, >> appends it. 
  Using > repeatedly in multiple echo commands erases everything except 
  the last write — confirmed this by accident, then fixed it using >>

## Practice Log
- Generated a 30-line test file with seq 1 30 > numbers.txt, confirmed 
  tail correctly showed lines 21–30
- Built a log file using echo with > for each line by mistake — cat 
  revealed only the last line survived, since each > overwrote the 
  previous content
- Rebuilt the file correctly using > for the first line and >> for 
  the rest, preserving all lines
- Ran grep "error" and grep "good" — confirmed grep correctly filters 
  and highlights matching lines
- Practiced grep "hello" on a new log file with multiple "Hello"/"hello" 
  lines — confirmed matches and understood case sensitivity behavior

## Status
✅ Lab completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/77e4c226-5f94-4fb5-9171-579e01357a95" />
