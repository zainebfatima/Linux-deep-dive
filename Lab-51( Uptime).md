 Lab 51: Checking System Uptime

🎯 Objectives

- Understand how to check how long a Linux system has been running.
- Learn how to find the system's last boot time.
- Understand and interpret load average.
- Learn how to check the number of available CPU cores.

---

🛠️ Commands Practiced

1. Check system uptime

uptime

Example:

08:00:20 up 7 min, 1 user, load average: 0.23, 0.46, 0.31

Understanding the output

- "08:00:20" → Current system time
- "up 7 min" → System has been running for 7 minutes
- "1 user" → One user is currently logged in
- "0.23" → Load average over the last 1 minute
- "0.46" → Load average over the last 5 minutes
- "0.31" → Load average over the last 15 minutes

---

2. Check CPU cores

nproc

Output:

2

This means the system has 2 available CPU processing units/cores.

---

3. Check the last boot time

who -b

Example:

system boot 2026-09-14 07:52

This shows when the system was last booted.

---

4. Display uptime in a simple format

uptime -p

Example:

up 10 minutes

The "-p" option displays uptime in a more readable format.

---

📊 Understanding Load Average

Load average tells us roughly how much work the system has been dealing with over different periods of time.

For example:

load average: 0.23, 0.46, 0.31

These represent:

0.23 → Last 1 minute
0.46 → Last 5 minutes
0.31 → Last 15 minutes

Load average is not a CPU usage percentage.

It should be considered together with the number of CPU cores.

For example, my system had:

2 CPU cores

So a load of "0.23" represents a relatively light workload for this system.

---

🔐 Cybersecurity Connection

System uptime and load information can be useful during security and system administration work.

For example, they can help us:

- Check whether a server has recently restarted.
- Monitor system performance.
- Investigate unusual system activity.
- Understand the current state of a Linux server during troubleshooting.

---

🧠 What I Learned

«Uptime tells us how long a system has been running since its last boot.»

«Load average shows the system's workload over the last 1, 5, and 15 minutes.»

«nproc tells us how many CPU processing units are available.»

Lab Status

✅ Lab 51 Completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/868232ae-473d-4b28-b851-ffe9a8304d45" />
