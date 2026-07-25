 💼 Office Simulation 04 - Package Management using APT

## 🏢 Scenario

You recently joined the IT Support team of a software company.

Your manager assigns you a Linux server and asks you to manage software packages using APT.

---

## 🎫 Ticket 1

### Task

Refresh the package list before installing any software.

### Command

bash
sudo apt update


### Result

Successfully updated the package list from Ubuntu repositories.

---

## 🎫 Ticket 2

### Task

Search whether *tree* is available in the repositories.

### Command

bash
apt search tree


### Result

Verified that the package exists and is available for installation.

---

## 🎫 Ticket 3

### Task

Install *Nmap* on the server.

### Command

bash
sudo apt install nmap


### Result

Nmap was installed successfully.

APT also installed required dependency packages automatically.

---

## 🎫 Ticket 4

### Task

The security team no longer requires Nmap.

Remove it from the server.

### Command

bash
sudo apt remove nmap


### Result

Nmap was removed successfully.

Ubuntu informed that some dependency packages were no longer required.

---

## 🎫 Ticket 5

### Task

Clean unnecessary packages left after removing Nmap.

### Command

bash
sudo apt autoremove


### Result

Unused dependency packages were removed, keeping the system clean.

---

# 📝 Lessons Learned

- Always run sudo apt update before installing software.
- apt search searches packages available in the repositories.
- apt install installs software and its dependencies.
- apt remove removes installed software.
- apt autoremove removes unnecessary dependency packages.
- Using official repositories is safer than downloading software from random websites.

---

# ✅ Skills Practiced

- Updating package lists
- Searching packages
- Installing software
- Removing software
- Cleaning unused dependencies
- Understanding package management using APT
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/aec0401c-dabd-4666-9209-96d19583d52e" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/d885f25c-2152-4105-b943-33011bc1c339" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/da10eb5b-b031-4486-9baa-aede98ab5538" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/653df11d-b9b1-49d1-bcaf-ae6904952f48" />

