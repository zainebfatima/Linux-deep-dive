# Lab 5: File Permissions Basics

## Objectives
- Understand the concept of Linux file permissions
- Learn how to check file permissions using commands
- Acquire skills to modify file permissions with chmod

## Commands Practiced

| Command | Purpose |
|---|---|
| ls -la filename | Check current permissions of a file |
| chmod 777 filename | Set full permissions (rwx) for owner, group, and others |
| chmod 764 filename | Set rwx for owner, rw for group, r for others |
| chmod 644 filename | Set rw for owner, r for group, r for others |

## Key Concepts

Permission string breakdown, e.g. -rwxrw-r--:
rwx   rw-   r--
│    │     │     │
│    │     │     └── Others
│    │     └──────── Group
│    └────────────── Owner
└─────────────────── File type (- = file, d = directory)
- r = read, w = write, x = execute, - = no permission
- Numeric values: read = 4, write = 2, execute = 1 — add them per group
  - rwx = 4+2+1 = 7
  - rw- = 4+2 = 6
  - r-- = 4 = 4
- chmod takes 3 digits: owner, group, others (e.g. chmod 644 = 
  owner rw-, group r--, others r--)
- Permissions can also be set with letter mode (e.g. chmod u+x file adds 
  execute for the owner only, without touching group/others)

## Practice Log
- Created permtest.txt, checked default permissions: -rw-rw-r--
- Applied chmod 777 → confirmed full permissions: -rwxrwxrwx
- Applied chmod 764 → confirmed: -rwxrw-r--
- Applied chmod 644 → confirmed: -rw-r--r--
- Verified each numeric mode matched the expected owner/group/others 
  breakdown before checking with ls -la

## Status
✅ Lab completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/0370ff37-c55e-4df5-8937-b1c592589940" />
