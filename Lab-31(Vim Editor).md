# Day 31 — Introduction to vi/vim

## Lab Objectives

- Understand the basic functionality and features of the vi/vim text editor.
- Learn how to navigate within the editor and manage files effectively.
- Practice editing text, using navigation commands, and performing search and replace operations.

## What is vi/vim?

vi and vim are terminal-based text editors commonly used in Linux systems.

They allow us to create, edit, navigate, search, and modify text files directly from the terminal.

Vim is an enhanced version of the original vi editor.

## Opening or Creating a File

```bash
vim practice.txt
This opens practice.txt in Vim.
If the file does not exist, Vim can create it when the file is saved.
Vim Modes
Normal Mode
Used for navigation and commands.
When a file is first opened, Vim starts in Normal Mode.
Insert Mode
Used for typing and editing text.
i
Pressing i enters Insert Mode.
Returning to Normal Mode
Ctrl + C
In my terminal environment, I used Ctrl + C to leave Insert Mode.
Saving and Quitting
Save
:w
w means write, which saves the file.
Quit
:q
Exits Vim.
Save and Quit
:wq
Saves the file and exits Vim.
Navigation Commands
Command
Function
h
Move left
j
Move down
k
Move up
l
Move right
G
Go to the last line
gg
Go to the first line
Searching in Vim
To search for text inside the file:
/Linux
Then press Enter.
Vim searches for the word Linux and moves the cursor to the matching text.
Comparison with grep
grep can search files from the terminal:
grep "Linux" practice.txt
Vim's / search searches within the file currently being edited.
Search and Replace
I practiced replacing text using:
:%s/Linux/Ubuntu/g
Meaning
% → entire file
s → substitute
Linux → text to find
Ubuntu → replacement text
g → replace all occurrences on each line
Vim displayed the number of substitutions made at the bottom, confirming that the replacements were successful.
Verification
After saving and exiting Vim, I used:
cat practice.txt
to view the file contents and confirm that my changes were saved.
What I Learned
Today I learned how to:
Open and create files using Vim.
Enter Insert Mode and edit text.
Return to Normal Mode.
Save and quit files.
Navigate through a file using h, j, k, and l.
Jump to the first and last lines using gg and G.
Search for text using /.
Perform search and replace operations using :%s.
Verify saved changes using cat.
Practice Completed
Created practice.txt
Added text using Vim
Edited the file
Saved the file
Navigated through the file
Searched for text
Replaced text
Verified the final contents
Key Takeaway
Vim is a powerful terminal-based editor that is especially useful when working with Linux servers where graphical text editors may not be available.
```

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/a160f210-8fc7-4323-b23b-9cd6564ab133" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/e5956064-0996-4288-9c85-78de75f6911b" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/8bf8f809-169b-444d-b42a-43b81bb5bace" />


