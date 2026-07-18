# Lab 16: Using Aliases

## Objectives
- Understand the concept of aliases in Linux.
- Learn how to create, use, and remove temporary aliases.
- Explore practical use cases for simplifying frequently used commands with aliases.

## Commands Practiced

| Command | Purpose |
|---|---|
| alias | Create a new alias or display all existing aliases |
| alias name='command' | Create a custom alias |
| unalias name | Remove an existing alias |
| pwd | Display the current working directory (used with an alias) |
| ls -al | List all files and directories with detailed information (used with an alias) |
| cd ~ | Navigate to the home directory (used with an alias) |
| date | Display the current system date and time (used with an alias) |

## Key Concepts
- An alias is a shortcut or nickname for a Linux command.
- Aliases reduce typing and improve productivity when frequently used commands need to be executed repeatedly.
- Aliases created using the alias command are temporary and remain available only during the current shell session.
- Permanent aliases can be created by adding them to the ~/.bashrc file.
- Multiple aliases can exist simultaneously, and all can be viewed using the alias command.
- Aliases can be removed at any time using the unalias command.
- In cloud-based lab environments like Al-Nafi, aliases disappear after the session ends because the virtual machine is temporary.

## Practice Log
- Created an alias named ll for ls -al and verified it displayed detailed directory contents.
- Created an alias named home for cd ~ to quickly navigate to the home directory.
- Created an alias named today for the date command and verified it displayed the current date and time.
- Created an alias named docs for the pwd command and confirmed it printed the current working directory.
- Displayed all configured aliases using the alias command.
- Removed the docs alias using unalias docs.
- Verified the alias was successfully removed by listing all aliases again.
- Learned that aliases are temporary unless stored in the ~/.bashrc configuration file.

## Real-World Relevance
- Linux administrators create aliases to speed up repetitive tasks.
- DevOps and Cloud Engineers use aliases for Docker, Kubernetes, Git, and system administration commands.
- Cybersecurity professionals often create aliases for log analysis, process monitoring, and reconnaissance commands to improve efficiency during investigations.

## Status
✅ Lab Completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/1c33a8d2-4a33-45fd-ac5e-de592da0f1d7" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/77a0fcba-6f7c-4771-86bc-f8ffa83ffca6" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/91c20a54-e160-4ca1-a897-a4ed533232e7" />


