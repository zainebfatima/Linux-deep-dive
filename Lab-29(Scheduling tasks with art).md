
## 📌 Objective
- Understand the purpose of the at command.
- Verify that at is installed.
- Schedule a one-time task.
- Learn how at differs from crontab.

---

## 🛠️ Commands Used

### Check at Version
bash
at -V


*Output*
text
at version 3.2.5


---

### Schedule a One-Time Task
bash
at now + 2 minutes


At the at> prompt:

bash
echo "Meeting Started" > /tmp/meeting.txt


Press:

text
Ctrl + D


---

## 📝 Result

The task was successfully scheduled.

Linux assigned a job ID and scheduled the command to run automatically after 2 minutes.

---

## 💡 Concepts Learned

### at
- Used for scheduling *one-time* tasks.
- Executes a command only once at the specified time.
- The scheduled command runs automatically without user interaction.

### crontab
- Used for *repeating* tasks.
- Suitable for daily, weekly, monthly, or recurring automation.

---

## 🔄 Difference Between at and crontab

| at | crontab |
|----|----------|
| Runs once | Runs repeatedly |
| One-time scheduling | Recurring scheduling |
| Example: Restart server tonight at 11 PM | Example: Backup every night at 2 AM |

---

## 🏢 Real-World Use Cases

### Using at
- Restart a server after maintenance.
- Run a script later today.
- Delete temporary files once.
- Execute a one-time backup.

### Using crontab
- Daily database backups.
- Weekly reports.
- Monthly payroll generation.
- Automatic log cleanup.

---

## 📝 Reflection

Today I learned how to use the at command to schedule one-time tasks in Linux. I verified that the package was installed, scheduled my first task, and understood how Linux executes scheduled commands automatically while the system is running. I also learned the difference between at for one-time automation and crontab for recurring automation, along with their real-world use in IT and system administration.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/42fb7069-3402-4e1e-96ec-de9b05bab5bc" />
