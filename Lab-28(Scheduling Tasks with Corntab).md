# ⏰ Linux Lab 28 – Scheduling Tasks with Crontab

## 🎯 Objectives

- Understand the basic functionality and utility of crontab.
- Learn how to list, create, edit, and remove cron jobs.
- Schedule automated tasks using crontab.

---

## 📌 Commands Used

### 1️⃣ List Current Cron Jobs

bash
crontab -l


*Purpose:*
Displays all scheduled cron jobs for the current user.

---

### 2️⃣ Create or Edit Cron Jobs

bash
crontab -e


*Purpose:*
Opens the crontab editor to create or modify scheduled tasks.

---

### 3️⃣ Remove All Cron Jobs

bash
crontab -r


*Purpose:*
Deletes all cron jobs for the current user.

---

## 📝 Cron Job Format

text
* * * * * command


| Field | Meaning |
|--------|---------|
| 1st * | Minute |
| 2nd * | Hour |
| 3rd * | Day of Month |
| 4th * | Month |
| 5th * | Day of Week |
| Command | Command to execute |

*Example:*

bash
* * * * * echo "Cron is working" >> /tmp/cron_test.txt


*Purpose:*
Runs the command every minute and appends the text to the file /tmp/cron_test.txt.

---

## 📝 What I Learned

- crontab is used to automate repetitive tasks in Linux.
- crontab -l lists scheduled cron jobs.
- crontab -e opens the cron editor to create or modify jobs.
- crontab -r removes all cron jobs.
- * means **every**.
- A cron job follows the format:
  - Minute
  - Hour
  - Day of Month
  - Month
  - Day of Week
  - Command
- Linux executes scheduled commands automatically without user intervention.

---

## 💡 Real-Life Use Cases

- Automatic database backups.
- Deleting temporary files.
- Running security scans.
- Generating system reports.
- Sending scheduled emails.
- Automating routine system maintenance tasks.

---

## 📚 Key Takeaways

- crontab -l → List cron jobs.
- crontab -e → Create/Edit cron jobs.
- crontab -r → Remove cron jobs.
- Cron helps automate repetitive administrative tasks.
- Automation saves time and reduces manual work.

Crontab is an essential Linux scheduling utility that allows system administrators to automate routine tasks, making systems more efficient and easier to manage.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/db991561-cf9a-4ab9-a2e8-7420b9da530c" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/09d53b83-839a-42d8-904b-5a062e516724" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/7898b10e-fd40-41c6-9023-836f4b9fb562" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/8d470e6d-3a72-441d-a75b-55daf8b09e22" />



