# 🖥️ Linux Lab 24 – Disk Usage and File Size

## 🎯 Objectives

- Understand how to determine disk usage and file sizes in a Linux environment.
- Learn to use commands to identify and manage large files and directories.
- Gain proficiency in interpreting disk usage data to optimize storage.

---

## 📌 Commands Used

### 1️⃣ Display Disk Usage

bash
du


*Purpose:*
Displays the disk usage of files and directories in the current location.

---

### 2️⃣ Display Disk Usage in Human-Readable Format

bash
du -h


*Purpose:*
Displays disk usage in an easy-to-read format such as KB, MB, and GB.

---

### 3️⃣ Display Total Size of the Current Directory

bash
du -sh


*Purpose:*
Shows the total disk usage of the current directory in a human-readable format.

---

### 4️⃣ Display Size of Each File and Directory

bash
du -sh *


*Purpose:*
Displays the size of each file and directory inside the current directory.

---

### 5️⃣ Display Filesystem Disk Usage

bash
df -h


*Purpose:*
Shows the total disk size, used space, available space, and usage percentage of all mounted filesystems.

---

## 📝 What I Learned

- du displays the disk usage of files and directories.
- du -h displays the same information in a human-readable format.
- du -sh displays the total size of the current directory.
- du -sh * displays the size of each file and directory inside the current directory.
- df -h displays the overall disk usage, including total, used, and available space.
- du helps identify which files or folders are using storage, while df shows how much storage is available on the filesystem.

---

## 💡 Real-Life Use Cases

- Finding folders that consume the most storage.
- Monitoring available disk space on a Linux system.
- Cleaning up unnecessary files to free storage.
- Troubleshooting "Disk Full" issues.
- Managing storage on Linux servers and workstations.

---

## 📚 Key Takeaways

- *du* → Shows the disk usage of files and directories.
- *du -h* → Displays disk usage in KB, MB, or GB.
- *du -sh* → Shows the total size of the current directory.
- *du -sh ** → Shows the size of every file and directory in the current location.
- *df -h* → Shows total, used, and available disk space for the filesystem.

Understanding these commands helps monitor storage usage, identify large files or directories, and efficiently manage disk space in Linux systems.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/88d38350-006b-4fe8-9329-0bc11016f5d4" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/76b76dae-d90c-4a0e-b636-4de41877c4f0" />

