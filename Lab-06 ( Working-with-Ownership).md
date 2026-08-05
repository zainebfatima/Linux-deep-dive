# Lab 6: Working with Ownership

## Objectives
- Understand file and directory ownership in Linux
- Learn how to change file ownership using the chown command
- Learn how to change group ownership using the chgrp command
- Explore practical examples of managing file permissions and ownership

## Commands Practiced

| Command | Purpose |
|---|---|
| ls -la filename | Check current owner and group of a file |
| groups | List all groups the current user belongs to |
| sudo chgrp groupname filename | Change the group owner of a file |
| sudo chown username filename | Change the user owner of a file |
| sudo chown user:group filename | Change both user and group ownership at once |

## Key Concepts
- Every file has two owners: a *user owner* (a specific person) and a 
  *group owner* (a set of users)
- The ls -la output shows owner and group as the 3rd and 4th columns 
  (e.g. ubuntu ubuntu or ubuntu adm)
- A user can belong to multiple groups at once — checked with groups
- chgrp only changes the group; chown can change the user, or both 
  user and group together using user:group syntax
- Changing ownership generally requires sudo since it affects file 
  metadata that regular users can't modify on files unrelated to them

## Practice Log
- Created ownertest.txt, checked default ownership: ubuntu ubuntu
- Ran groups to see available groups: ubuntu adm cdrom sudo dip lxd
- Changed group ownership: sudo chgrp adm ownertest.txt → confirmed 
  group changed to adm
- Changed user ownership: sudo chown ubuntu ownertest.txt → confirmed 
  owner remained ubuntu (explicit set, no visible change since already 
  correct)
- Changed both at once: sudo chown ubuntu:sudo ownertest.txt → confirmed 
  owner ubuntu, group sudo — verified single-command syntax works for 
  updating both fields together

## Status
✅ Lab completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/09aea649-4416-45c8-9f92-762ad7b0f9cd" />
