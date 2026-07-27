# 🖥️ Linux Lab 23 – System Hardware Information

## 🎯 Objectives

- Understand how to retrieve and interpret basic system hardware information.
- Learn to use Linux commands to gather details about the CPU, memory (RAM), disk usage, and storage devices.

---

## 📌 Commands Used

### 1️⃣ Display CPU Information

bash
lscpu


*Purpose:*
Displays detailed information about the CPU, including its architecture, model, cores, threads, and other hardware details.

---

### 2️⃣ Display Memory (RAM) Usage

bash
free -h


*Purpose:*
Displays RAM and swap memory usage in a human-readable format.

---

### 3️⃣ Display Disk Usage

bash
df -h


*Purpose:*
Shows the total, used, and available disk space for all mounted file systems in a human-readable format.
[2:38 am, 27/07/2026] ...: ### 4️⃣ Display Disks and Partitions

bash
lsblk


*Purpose:*
Lists all available storage devices and their partitions.

---

## 📝 What I Learned

- lscpu displays CPU (processor) information.
- free -h displays RAM and swap memory usage.
- df -h displays disk usage and available storage.
- lsblk displays storage devices and their partitions.
- These commands are useful for checking a system's hardware configuration and available resources.

---

## 💡 Real-Life Use Cases

- Checking a computer's hardware specifications.
- Monitoring available RAM and disk space.
- Verifying system resources before installing software.
- Troubleshooting performance issues.
- Gathering system information during Linux administration and cybersecurity assessments.

---

## 📚 Key Takeaways

- *CPU:* lscpu
- *Memory (RAM):* free -h
- *Disk Usage:* df -h
- *Disks & Partitions:* lsblk

Understanding these commands helps in monitoring system hardware and managing Linux systems efficiently.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/06961395-2592-434c-860a-d454d5677e25" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/9453e2bc-c5a1-4fca-81ae-6de33b96352d" />

