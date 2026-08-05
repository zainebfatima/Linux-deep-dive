# Lab 4: Using Text Editors

## Objectives
- Understand the basic functionalities of text editors such as nano and vi
- Learn how to create, open, edit, and save files using these editors
- Develop skills to efficiently navigate and execute commands within the 
  text editor environment

## Commands Practiced

| Command | Purpose |
|---|---|
| nano filename | Open/create a file in the nano editor |
| Ctrl + O | Save (write out) the current file in nano |
| Ctrl + X | Exit nano |
| vi filename | Open/create a file in the vi editor |
| i | Switch from Command mode to Insert mode in vi |
| Esc | Switch from Insert mode back to Command mode in vi |
| :wq | Save and quit in vi (write + quit) |

## Key Concepts
- nano is beginner-friendly — shows shortcuts on screen at all times, 
  works similar to a simple notepad
- vi uses two main modes:
  - *Command mode* (default on open) — keypresses trigger actions, not text input
  - *Insert mode* — entered via i, allows normal typing
- Must press Esc to leave Insert mode before running save/exit commands 
  like :wq
- In vi, clicking away from the terminal before pressing Esc can cause 
  the keypress to affect the browser instead of the editor — always click 
  inside the terminal first to ensure focus is correct

## Practice Log
- Created and edited a file using nano, saved with Ctrl+O, exited with Ctrl+X
- Verified saved content using cat
- Created a second file using vi, entered Insert mode with i, typed content
- Initially pressed Esc while terminal focus was lost, which affected the 
  browser instead of vi — resolved by clicking inside the terminal first
- Successfully returned to Command mode and saved/exited using :wq
- Verified content was saved correctly using cat

## Status
✅ Lab completed

<img width="1366" height="768" alt="fff01075-5025-4e4d-959c-37e07b3eb1bc" src="https://github.com/user-attachments/assets/4e972a08-c8c3-459f-9de6-5e7ec4b1d77c" />
