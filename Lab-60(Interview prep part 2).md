---

⚙️ Processes

29. What is a process?

A process is a running instance of a program.

For example, when you start a program, Linux creates a process for it.

---

30. What is PID?

PID means Process ID.

Each running process has a unique process ID.

---

31. What does "ps" do?

"ps" displays information about running processes.

Example:

ps

A commonly used version is:

ps aux

---

32. What are "top" and "htop"?

They are system monitoring tools used to view running processes and resource usage.

They can show information such as:

- CPU usage
- Memory usage
- Processes
- PID
- Users

---

💾 Storage

33. What does "df" do?

"df" shows filesystem disk-space usage.

df -h

"-h" makes the output easier for humans to read.

---

34. What does "du" do?

"du" shows how much disk space files and directories are using.

du -sh directory

---

35. What is mounting?

Mounting makes a filesystem available at a directory in the Linux filesystem.

Example:

Disk/Partition
      ↓
   Mount
      ↓
 /mnt/data

---

36. What is "/etc/fstab"?

"/etc/fstab" contains information about filesystems that can be mounted automatically, commonly during boot.

---

37. What is LVM?

LVM stands for Logical Volume Manager.

It provides flexible management of storage volumes.

Basic structure:

Physical Volume
       ↓
Volume Group
       ↓
Logical Volume

---

🔄 Services

38. What is "systemctl"?

"systemctl" is used to manage services and other systemd resources.

Examples:

systemctl status ssh
systemctl start ssh
systemctl stop ssh

---

39. What is systemd?

systemd is a system and service manager commonly used by modern Linux distributions.

It helps manage:

- Services
- Startup
- Processes
- System states

---

🌐 Networking

40. What does SSH stand for?

SSH stands for Secure Shell.

It provides secure remote access to a Linux system.

Example:

ssh user@server

---

41. What is an IP address?

An IP address identifies a device/interface on a network.

Example:

192.168.1.10

---

42. What is DNS?

DNS stands for Domain Name System.

It translates domain names into IP addresses.

Example:

example.com → IP address

---

43. What is a port?

A port is a logical communication endpoint used by network services.

Examples:

22  → SSH
80  → HTTP
443 → HTTPS

---

🔥 Security

44. What is a firewall?

A firewall controls network traffic based on defined rules.

Linux systems can use firewall tools such as:

UFW
iptables

---

45. What is UFW?

UFW stands for Uncomplicated Firewall.

It provides a simpler interface for managing firewall rules.

Example:

sudo ufw status

---

46. What is iptables?

"iptables" is a Linux firewall/rule-management tool used to control network traffic.

---

📝 Logs

47. Where are many Linux logs stored?

Many system logs are stored under:

/var/log

---

48. Why are logs important?

Logs help administrators and security professionals:

- Troubleshoot problems
- Investigate events
- Monitor systems
- Detect suspicious activity
- Understand what happened on a system

---

49. What is log rotation?

Log rotation manages growing log files by periodically creating rotated copies and eventually removing older copies according to configured retention  rules.

A common tool is:

logrotate

---

⏰ Automation

50. What is cron?

Cron is used to schedule recurring tasks.

Example:

Run a backup every day

---

51. What is "crontab"?

"crontab" contains scheduled cron jobs for a user.

Command:

crontab -e

---

52. What is the difference between cron and "at"?

cron → recurring/scheduled tasks

at → a task scheduled for a specific future time

---

🐚 Shell

53. What is a shell?

A shell is a program that allows users to interact with the operating system through commands.

Examples:

Bash
Zsh
Fish

---

54. What is Bash?

Bash stands for Bourne Again Shell.

It is one of the most commonly used shells on Linux.

---

55. What is ".bashrc"?

".bashrc" is a Bash configuration file commonly used for interactive shell settings.

It can contain:

- Aliases
- Environment variables
- Shell configuration

Example:

alias l='ls -lah'

---

56. What is an alias?

An alias is a shortcut for a command.

Example:

alias ll='ls -lah'

---

🔎 Searching and Text Processing

57. What does "grep" do?

"grep" searches text for patterns.

Example:

grep "error" logfile.txt

---

58. What is regular expression (regex)?

A regular expression is a pattern used to search or match text.

For example, regex can help identify specific patterns inside files or command output.

---

🗑️ Secure File Deletion

59. What is "shred"?

"shred" is a command designed to overwrite the contents of a file before removal.

Example:

shred -n 3 file.txt

The "-n 3" option requests three overwrite passes.

---

🛡️ SELinux

60. What is SELinux?

SELinux stands for Security-Enhanced Linux.

It provides an additional security/access-control layer beyond traditional Linux permissions.

---

61. What are the three SELinux modes?

Enforcing
Permissive
Disabled

Enforcing → blocks policy violations.

Permissive → allows actions but logs violations.

Disabled → SELinux is not active.

---

🧠 Quick Interview Revision

Before answering a Linux interview question, try to explain the concept in your own words.

Important areas to revise:

Linux basics
↓
Filesystem
↓
Users & Groups
↓
Permissions
↓
Processes
↓
Services
↓
Networking
↓
Storage
↓
Logs
↓
Automation
↓
Shell
↓
Security

---

🎯 Final Interview Tip

Don't focus only on memorizing commands.

For each command, understand:

What does it do?
        ↓
Why would I use it?
        ↓
What does its output tell me?
        ↓
When would I use it in a real situation?

For example:

df -h

Don't just remember:

«"df shows disk space."»

Understand:

«"If a server is running out of storage, I can use "df -h" to check filesystem usage and identify where the space problem 

This lab serves as a revision bridge between Linux fundamentals and practical cybersecurity/system-administration work.

---


The goal is not to memorize every command.

The goal is to understand Linux well enough to work with it, troubleshoot it, secure it, and explain what you are doing.
