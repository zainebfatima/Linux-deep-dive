# Lab 2: Working with Directories

## Objectives
- Understand basic operations for managing directories in a filesystem
- Learn how to create, remove, move, and rename directories using 
  command-line tools

## Commands Practiced

| Command | Purpose |
|---|---|
| mkdir foldername | Create a new directory |
| mkdir -p parent/child | Create nested directories in one command, even if parent doesn't exist yet |
| rmdir foldername | Remove an *empty* directory only (safety check) |
| rm -r foldername | Remove a directory and everything inside it (recursive) |
| mv oldname newname | Rename a directory (or move it to a new location) |

## Key Concepts
- rmdir fails on non-empty directories — this is a built-in safety net 
  to prevent accidentally deleting folders full of files
- rm -r is required to delete a non-empty directory; -r means recursive
- There is no dedicated "rename" command — mv handles both moving and 
  renaming depending on how it's used
- mkdir cannot create nested directories by default unless the parent 
  already exists — -p flag solves this

## Practice Log

*Round 1 — guided practice:*
- Created practice_folder with two subfolders
- Renamed it using mv
- Attempted rmdir on a non-empty folder — got expected error:
  rmdir: failed to remove 'my_renamed_folder': Directory not empty
- Successfully removed it using rm -r

*Round 2 — independent practice:*
- Built a project structure: project/src, project/docs, project/tests
- Hit a real error: mkdir dua/effa failed with 
  No such file or directory because parent folder dua didn't exist
- Learned to use mkdir -p to create nested directories in one step
- Practiced navigating between nested folders with cd and confirming 
  location with pwd

## Status
✅ Lab completed — terminal screenshot to be added
## Terminal Screenshots

![Lab 2 practice - nested directory creation](lab2-directory-practice-1.png)

![Lab 2 practice - navigation and cd shortcuts](lab2-directory-practice-2.png)
<img width="714" height="517" alt="image" src="https://github.com/user-attachments/assets/cf1d657d-7606-4060-a95c-bb963dcf4f29" />
<img width="722" height="523" alt="image" src="https://github.com/user-attachments/assets/8889c28d-62e0-4911-bf6c-02e9e8166179" />


