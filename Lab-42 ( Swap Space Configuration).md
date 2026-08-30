Lab 42: Swap Space Configuration
🎯 Objectives
Understand swap space and its importance.
Check current swap usage.
Create and configure a swap file.
Enable and test the swap file.
🧠 What I Learned
RAM is fast, temporary working memory.
Disk is permanent storage.
Swap is space on the disk that Linux can use as extra, slower memory when RAM needs help.
Swap can be a separate partition or a file.
For this lab, I created a swap file.
🧪 Practical Work
Checked RAM and swap:
free -h
Initially, swap showed:
Swap: 0B  0B  0B
Checked active swap:
swapon --show
Created a 512 MB swap file:
sudo fallocate -l 512M /swapfile
Checked the file:
ls -lh /swapfile
Converted the file into swap space:
sudo mkswap /swapfile
Enabled the swap:
sudo swapon /swapfile
Checked active swap:
swapon --show
The output showed:
NAME       TYPE  SIZE  USED  PRIO
/swapfile  file  512M  0B    -2
Verified with:
free -h
Swap appeared as approximately 511M, with 0B used.
💡 Key Concept
💾 Disk = Permanent storage
🧠 RAM = Fast temporary working space
🔄 Swap = Slower disk space used to support RAM
⚙️ CPU = Processes the data
🧠 My Mental Model
Disk → RAM → CPU
        ↕️
      Swap
The disk stores data permanently, RAM holds data currently being worked on, and the CPU processes that data. Swap can temporarily hold less-active data when RAM needs more space.

*Labs  43 complete 
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/0ec017dd-a1b8-42f9-81ce-26193ff48a84" />
