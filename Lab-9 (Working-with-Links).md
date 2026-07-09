# Lab 9: Working with Links

## Objectives
- Understand the difference between hard links and symbolic links
- Learn how to create hard and symbolic links using command-line tools
- Explore and compare the file sizes and inodes of hard and symbolic links

## Commands Practiced

| Command | Purpose |
|---|---|
| ls -li filename | Show file details including the inode number |
| ln original.txt hardlink.txt | Create a hard link |
| ln -s original.txt symlink.txt | Create a symbolic (soft) link |

## Key Concepts
- An *inode* is the actual storage record for a file's data on disk — 
  it holds the content location, size, permissions, and owner. A 
  filename is just a label pointing to an inode, not the data itself.
- A *hard link* creates a new name pointing to the exact same inode as 
  the original file. Both names share identical data.
- A *symbolic link* creates a brand new, separate file (with its own 
  inode) that stores only the path to another file — like a shortcut.
- Symbolic links show a distinct file type in ls -l: they start with 
  l instead of - or d, and display an arrow to their target, e.g. 
  symlink.txt -> original.txt
- Symbolic link permissions typically show as rwxrwxrwx because actual 
  permission enforcement happens on the target file, not the link itself

## Practice Log
- Created original.txt, noted its inode number (266747)
- Created hardlink.txt using ln — confirmed it shared the exact same 
  inode number as original.txt
- Created symlink.txt using ln -s — confirmed it had a different 
  inode number, and its permission string started with l and showed 
  -> original.txt
- Deleted original.txt, then tested both links:
  - cat hardlink.txt — still worked, displayed original content, since 
    the data remains as long as any hard link still references the inode
  - cat symlink.txt — broke, returned an error, since the symlink only 
    stored a path that no longer resolved to anything

## Status
✅ Lab completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/50859400-cfa9-4104-b82f-b983251867ac" />
