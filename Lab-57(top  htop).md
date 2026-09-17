 Linux Lab 57 — Monitoring with "top" and "htop"

🎯 Objectives

- Understand the purpose of system monitoring tools "top" and "htop".
- Learn how to run "htop" on a Linux system.
- Compare the interfaces of "top" and "htop".
- Learn how to sort processes by CPU and memory usage.

---

📚 What is System Monitoring?

System monitoring means observing what is happening inside a Linux system in real time.

Monitoring tools can show:

- Running processes
- CPU usage
- Memory (RAM) usage
- Process IDs
- Users running processes
- System load
- Process states

Two commonly used Linux monitoring tools are:

top
htop

---

🔹 Part 1 — Using "top"

I started "top" with:

top

It displayed a live view of system activity.

The screen showed information such as:

Tasks
CPU usage
Memory usage
Swap
Load average
PID
USER
%CPU
%MEM
COMMAND

---

🧠 Important Information in "top"

Tasks

Example:

Tasks: 211 total, 1 running, 210 sleeping

This tells us how many processes/tasks are present and their current states.

CPU

The CPU section shows how the processor is being used.

Important values include:

- "us" → user processes
- "sy" → system/kernel activity
- "id" → idle CPU
- "wa" → waiting for I/O

Memory

The memory section shows how much RAM is:

- Total
- Used
- Free
- Available

---

🔥 Sorting Processes by CPU

Inside "top", I pressed:

P

This sorted the processes according to CPU usage.

The process using the highest CPU appeared near the top.

Key Point

P → Sort by CPU usage

---

🧠 Sorting Processes by Memory

Inside "top", I pressed:

M

This sorted processes according to memory (RAM) usage.

Key Point

M → Sort by memory usage

---

🔹 Part 2 — Using "htop"

I then ran:

htop

"htop" opened an interactive and more visual process-monitoring interface.

It displayed:

- Tasks
- CPU usage
- Memory usage
- Swap
- Load average
- Uptime
- Running processes

---

📊 Process Information

The process list included columns such as:

PID
USER
PRI
NI
VIRT
RES
SHR
S
CPU%
MEM%
TIME+
Command

Some important columns are:

- PID → Process ID
- USER → User who owns the process
- CPU% → CPU usage
- MEM% → Memory usage
- Command → Program/process name

---

🔄 Sorting Processes in "htop"

I pressed:

F6

This opened the Sort by menu.

The available options included:

PID
USER
PRIORITY
NICE
M_VIRT
M_RESIDENT
M_SHARE
STATE
PERCENT_CPU
PERCENT_MEM
TIME
Command

I selected:

PERCENT_CPU

This sorted the processes by CPU usage.

I then selected:

PERCENT_MEM

This sorted the processes by memory usage.

---

🆚 "top" vs "htop"

"top"| "htop"
Command-line monitoring tool| Interactive monitoring tool
Usually available by default| May need to be installed
Basic interface| More visual interface
"P" sorts by CPU| F6 allows sorting options
"M" sorts by memory| F6 → "PERCENT_MEM"
Keyboard controlled| More interactive controls

---

🧠 Key Understanding

The main purpose of both tools is:

«To monitor running processes and see how much CPU and RAM they are using.»

For example:

High CPU → Find the process using the most CPU
High RAM → Find the process using the most memory

This can help with troubleshooting slow systems and identifying resource-heavy processes.

---

🔑 Commands & Shortcuts Learned

top

Start the "top" monitoring tool.

htop

Start the "htop" monitoring tool.

Inside "top":

P → Sort by CPU
M → Sort by memory
q → Quit

Inside "htop":

F6 → Sort by
F10 → Quit

---

🏁 Lab Status

Lab 57 — Monitoring with "top" and "htop": COMPLETED ✅
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/548c4ac7-d012-4cea-8487-b57f4c140044" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/069367c1-b65c-4027-8c38-b1fe0e41dc77" />


