Linux Lab 52 — Using "df" and "du"

📌 Overview

In this lab, I learned how to check disk space and directory usage in Linux using the "df" and "du" commands.

These commands are useful for monitoring storage and troubleshooting situations where a Linux system is running out of disk space.

---

🎯 Objectives

- Understand and use the "df" command to check disk space usage.
- Learn how to use the "du" command to assess directory usage.
- Analyze disk usage results to identify where storage is being consumed.

---

🔹 1. "df" — Check Disk Space

The "df" command shows the available and used space on filesystems.

Command:

df

For a human-readable format:

df -h

Important columns:

- Filesystem — The filesystem or disk being checked.
- Size — Total available size.
- Used — Space currently being used.
- Avail — Available space.
- Use% — Percentage of space being used.
- Mounted on — Location where the filesystem is mounted.

Example:

df -h

This is useful for quickly checking whether a disk or filesystem is becoming full.

---

🔹 2. "du" — Check Directory Usage

The "du" command shows how much disk space files and directories are using.

Command:

du

Human-readable output:

du -h

To check the total usage of the home directory:

du -sh ~

Here:

- "-s" → Show only a summary.
- "-h" → Human-readable format.
- "~" → Current user's home directory.

---

🔹 3. Check Main Directories

To see the storage used by the main directories inside the home directory:

du -h --max-depth=1 ~

"--max-depth=1" means that it shows the home directory and its immediate directories without going deeper into all their subdirectories.

---

🔹 4. Sort by Storage Usage

To arrange the directories from largest to smallest:

du -h --max-depth=1 ~ | sort -hr

Here:

- "du" → Checks disk usage.
- "-h" → Human-readable sizes.
- "--max-depth=1" → Shows only the main/immediate directories.
- "sort -hr" → Sorts human-readable sizes in reverse order, so the largest appears first.

---

🧠 "df" vs "du"

Command| Purpose
"df -h"| Shows overall filesystem/disk space
"du -h"| Shows space used by files/directories
"du -sh ~"| Shows total size of the home directory
"du -h --max-depth=1 ~"| Shows usage of main directories
"du -h --max-depth=1 ~ | sort -hr"| Shows main directories from largest to smallest

Easy way to remember:

«"df" = How much space is available on the disk?
"du" = What is using that space?»

---

🔧 Real-World Linux Administration

If a server reports that its disk is almost full, an administrator can investigate it using:

df -h

Then identify large directories:

du -h --max-depth=1 ~ | sort -hr

After identifying the largest directory, the data should be investigated before taking action.

Depending on the situation, the solution could be:

- Remove unnecessary data.
- Move or archive required data.
- Mount an additional disk.
- Extend an LVM logical volume if additional space is available.
- Configure proper log rotation if logs are consuming excessive space.

⚠️ Important: A large directory should never be deleted blindly. First determine what the data is and whether it is safe to remove or move.

---

💡 Connection With Previous Linux Labs

This lab connected with concepts I learned earlier:

Disk → Partition → Filesystem → Mount → Directory

I also connected disk-space management with:

- Partitions
- Mounting
- Virtual disks
- LVM
- Filesystems
- Swap

I learned that swap is different from normal disk storage. Swap helps with memory pressure and is not a solution for a filesystem that is simply running out of storage.

---

🧪 Commands Practiced

df
df -h
du
du -h
du -sh ~
du -h --max-depth=1 ~
du -h --max-depth=1 ~ | sort -hr

---

📝 Key Takeaway

"df" and "du" are important Linux administration tools for understanding and troubleshooting disk usage.

The general troubleshooting workflow is:

Find → Investigate → Decide → Clean / Move / Expand

🐧 Lab 52 completed!
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/3982ffdd-ca7c-461f-b0bd-56c64a6e89de" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/190714e9-4b9d-4198-aa3c-a07cefb5351b" />


