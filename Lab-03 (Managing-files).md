# Lab 3: Managing Files

## Objectives
- Demonstrate basic file management tasks in a Unix/Linux environment
- Get familiar with creating, viewing, and deleting files using command-line tools

## Commands Practiced

| Command | Purpose |
|---|---|
| touch filename | Create a new empty file (or update its timestamp if it exists) |
| cat filename | Display the entire contents of a file |
| head filename | Show the first 10 lines of a file |
| tail filename | Show the last 10 lines of a file |
| echo "text" > file | Write text into a file, overwriting existing content |
| echo "text" >> file | Append text to a file, keeping existing content |
| rm filename | Delete a file |
| seq 1 20 > file | Generate a sequence of numbers, useful for testing multi-line file behavior |

## Key Concepts
- touch creates files, mkdir creates directories — these are not interchangeable
- > overwrites file content; >> appends to it without erasing what's there
- head and tail only show a visible difference when a file has more than 
  10 lines — on short files, both commands display the entire file, which 
  is expected behavior, not an error
- rm deletes files directly (no -r needed, unlike directories) since a 
  file has no contents to recurse into
- Attempting to cat a deleted file correctly throws: 
  cat: filename: No such file or directory — confirms deletion worked

## Practice Log
- Created notes.txt using touch, confirmed it was empty with cat
- Wrote content using echo >, viewed it with cat, head, and tail
- Deleted the file with rm, verified deletion via the expected cat error
- Practiced multi-line files using echo >> to append lines — noticed a 
  duplicate-line issue caused by a terminal input glitch, not a command 
  misunderstanding; fixed by recreating the file cleanly
- Used seq 1 20 > numbers.txt to generate a 20-line file, which properly 
  demonstrated the real difference between head (first 10) and tail 
  (last 10)

## Status
✅ Lab completed
