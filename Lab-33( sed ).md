# Day 33 — sed for Text Manipulation

## Lab Objectives

- Understand how to use the sed command for basic text manipulation.
- Learn to replace text in a file using sed.
- Practice removing lines that match a specific pattern with sed.

## What is sed?

sed stands for *Stream Editor*.

It is a Linux command used to search, modify, replace, and delete text from files.

Unlike an interactive editor such as Vim, sed can perform text manipulation directly from the command line and is useful for automation.

## Basic sed Syntax

```bash
sed 'command' filename
By default, sed displays the modified result on the screen without changing the original file.
Replacing Text
I practiced replacing Linux with Ubuntu:
sed 's/Linux/Ubuntu/g' practice.txt
Meaning
s → substitute
Linux → text to find
Ubuntu → replacement text
g → replace all matching occurrences on each line
The replacement was displayed on the screen, but the original file was not modified.
Modifying the Original File
To make the replacement directly in the original file, I used the -i option:
sed -i 's/Linux/Ubuntu/g' practice.txt
After using cat, I confirmed that the original file had been changed.
Important Difference
sed 's/Linux/Ubuntu/g' practice.txt
→ Shows the modified output but does not change the original file.
sed -i 's/Linux/Ubuntu/g' practice.txt
→ Modifies the original file directly.
-i means in-place.
Removing Matching Lines
I created a separate remove.txt file for deletion practice.
To remove lines containing Windows from the output:
sed '/Windows/d' remove.txt
Meaning
/Windows/ → search for lines containing Windows
d → delete the matching lines from the output
Without -i, the original file remains unchanged.
Removing Lines from the Original File
To actually remove the matching lines from the original file:
sed -i '/Windows/d' remove.txt
I then verified the result using:
cat remove.txt
The Windows line was successfully removed from the original file.
grep vs sed
grep
grep is mainly used to search and filter text.
grep "Linux" practice.txt
It displays matching lines without modifying the file.
sed
sed is used to manipulate text, such as replacing or deleting text.
sed 's/Linux/Ubuntu/g' practice.txt
What I Learned
Today I learned how to:
Use sed for text manipulation.
Replace text using the s command.
Delete matching lines using the d command.
Understand the difference between normal sed output and in-place editing.
Use -i to modify the original file.
Verify file changes using cat.
Understand the difference between grep and sed.
Practice Completed
Created a practice file.
Replaced text using sed.
Previewed replacements without changing the original file.
Used -i to modify the original file.
Created a separate file for deletion practice.
Removed matching lines using sed.
Used -i to permanently remove matching lines.
Verified the changes with cat.
Key Takeaway
grep is mainly used to find and filter text, while sed is used to manipulate text.
The most important commands practiced were:
sed 's/old/new/g' file
sed -i 's/old/new/g' file
sed '/pattern/d' file
sed -i '/pattern/d' file
-i means that the modification is made in-place, directly in the original file.
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/2bacca2e-b1e2-41f9-a45a-516e6cc4f74e" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/68b422fd-f96e-440b-9508-49889a98fada" />

