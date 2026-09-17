Linux Lab 59 — Basic Interview Questions & Concepts

🎯 Lab Objective

This lab is designed to revise the fundamental Linux concepts prepare for basic Linux technical interviews.

The focus is on understanding concepts rather than memorizing answers.

---

📚 Basic Linux Interview Questions

1. What is Linux?

Linux is an open-source operating system kernel used in many operating systems and servers.

Examples of Linux distributions include:

- Ubuntu
- Debian
- Fedora
- Red Hat Enterprise Linux
- Kali Linux
- Arch Linux

---

2. What is a Linux distribution?

A Linux distribution is a complete operating system built around the Linux kernel.

It usually contains:

- Linux kernel
- System utilities
- Package manager
- Applications
- Desktop environment (if applicable)

Example:

Ubuntu = Linux kernel + system tools + applications + package management

---

3. What is the root user?

The root user is the superuser in Linux.

Root has very high-level privileges and can perform administrative tasks that normal users cannot.

---

4. What is "sudo"?

"sudo" allows an authorized normal user to execute commands with elevated privileges.

Example:

sudo apt update

---

5. What is the difference between "su" and "sudo"?

"sudo" runs a specific command with elevated privileges.

sudo command

"su" can switch to another user, commonly the root user.

su -

---

📁 File System

6. What is "/" in Linux?

"/" is the root directory.

All other directories exist underneath it.

Example:

/
├── home
├── etc
├── var
├── usr
└── tmp

---

7. What is "/home"?

"/home" contains the personal directories of normal users.

Example:

/home/ubuntu

---

8. What is "/etc"?

"/etc" mainly contains system configuration files.

Examples include:

/etc/ssh
/etc/fstab
/etc/hosts

---

9. What is "/var"?

"/var" contains data that frequently changes during system operation.

Examples include:

- Logs
- Cache
- Spool data

A common directory is:

/var/log

---

10. What is "/tmp"?

"/tmp" is used for temporary files.

---

📝 Basic Commands

11. What does "pwd" do?

"pwd" means Print Working Directory.

It shows the directory you are currently in.

pwd

---

12. What does "ls" do?

"ls" lists files and directories.

ls

A commonly useful version is:

ls -lah

---

13. What does "cd" do?

"cd" means Change Directory.

cd /var/log

---

14. What does "mkdir" do?

Creates a directory.

mkdir test

---

15. What does "touch" do?

Creates an empty file if the file does not already exist.

touch file.txt

---

16. What does "cp" do?

Copies files or directories.

cp file.txt backup.txt

---

17. What does "mv" do?

Moves or renames files and directories.

mv old.txt new.txt

---

18. What does "rm" do?

Removes files.

rm file.txt

---

19. What does "cat" do?

Displays file contents.

cat file.txt

---

🔐 Permissions

20. What are Linux file permissions?

Linux permissions control who can:

- Read
- Write
- Execute

a file or directory.

The three permission categories are:

User
Group
Others

---

21. What does "rwx" mean?

r = read
w = write
x = execute

For example:

rwx

means read, write, and execute permissions are available.

---

22. What does "chmod" do?

"chmod" changes file permissions.

Example:

chmod 755 script.sh

---

23. What does "chown" do?

"chown" changes the owner of a file or directory.

Example:

sudo chown user:user file.txt

---

24. What does "chgrp" do?

"chgrp" changes the group ownership.

sudo chgrp developers file.txt

---

👥 Users and Groups

25. What does "whoami" do?

Shows the current username.

whoami

---

26. What does "id" do?

Displays information about the current user, including:

- UID
- GID
- Groups

id

---

27. What is UID?

UID means User ID.

Linux identifies users internally using numeric UIDs.

---

28. What is GID?

GID means Group ID.

It identifies a Linux group numerically.

---


