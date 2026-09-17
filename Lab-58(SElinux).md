Linux Lab 58 — Introduction to SELinux

🎯 Lab Objectives

- Understand the basics of Security-Enhanced Linux (SELinux).
- Learn how to check and manage SELinux status.
- Understand SELinux operating modes.
- Verify SELinux configuration through practical commands.
- Understand the difference between SELinux configuration and its current runtime state.

---

🔐 What is SELinux?

SELinux (Security-Enhanced Linux) is a security mechanism that provides an additional layer of access control on Linux systems.

Normal Linux permissions control access using things such as:

- Users
- Groups
- File permissions

SELinux adds another layer of security by applying security policies that control what processes and users are allowed to do.

Simple analogy

Think of normal Linux permissions as one security guard checking your ID.

SELinux is like having a second security guard who checks whether you are actually allowed to perform a particular action.

---

⚙️ SELinux Modes

SELinux has three main modes:

Mode| Meaning
Enforcing| SELinux actively enforces its security policies and blocks violations.
Permissive| SELinux allows actions but logs policy violations.
Disabled| SELinux is not active and no SELinux policy is loaded.

Easy way to remember

Enforcing  → Block + Log
Permissive → Allow + Log
Disabled   → Not Active

---

🔎 Practical Work

1. Check SELinux Status

Command:

sestatus

Initially, the command was not available, so the SELinux management utilities were installed:

sudo apt install policycoreutils

After installation, "sestatus" was run again.

Result

SELinux status: disabled

This showed that SELinux was not currently active on the Ubuntu system.

---

2. Check Operating System

Command:

cat /etc/os-release

Result

The system was running:

Ubuntu 24.04.3 LTS

This was important because Ubuntu commonly uses AppArmor as its default mandatory access-control framework rather than SELinux.

---

3. Check SELinux Configuration

Command:

cat /etc/selinux/config

The configuration contained:

SELINUX=permissive
SELINUXTYPE=default

Important observation

Although the configuration file specified:

SELINUX=permissive

"sudo sestatus" reported:

SELinux status: disabled

This demonstrated an important Linux concept:

«The configuration file and the current runtime state are not always the same thing.»

The configuration represents how SELinux is intended to be configured, while "sestatus" reports the current state of the running system.

---

4. Check SELinux Filesystem

Command:

ls -ld /sys/fs/selinux

The SELinux filesystem was not available because SELinux was not currently active.

This provided additional confirmation that SELinux was not loaded on the running system.

---

🔄 Changing SELinux Modes

When SELinux is properly enabled, the current mode can be checked with:

getenforce

The runtime mode can normally be changed with:

sudo setenforce 0

This changes SELinux to:

Permissive

And:

sudo setenforce 1

changes it to:

Enforcing

These commands were studied as part of the lab, but were not executed on this machine because SELinux was disabled.

---

🧠 Key Concepts Learned

1. SELinux provides an additional security layer

It works alongside traditional Linux permissions to provide more controlled access.

2. Enforcing vs Permissive

Enforcing  → violations are blocked
Permissive → violations are allowed but logged

3. Disabled

When SELinux is disabled:

No SELinux policy is loaded

4. Configuration vs Runtime

The configuration file showed:

SELINUX=permissive

while the running system reported:

SELinux status: disabled

This taught me that a configuration setting does not necessarily represent the current runtime state.

---

🛠️ Important Commands

sestatus

Check detailed SELinux status.

getenforce

Check the current SELinux mode.

sudo setenforce 0
Set SELinux to Permissive mode when SELinux is active.

sudo setenforce 1

Set SELinux to Enforcing mode when SELinux is active.

cat /etc/selinux/config

View SELinux configuration.

ls -ld /sys/fs/selinux

Check whether the SELinux filesystem is available.


This was the final lab of my Linux 60-Lab Roadmap.

I learned how to:

- Understand SELinux.
- Check SELinux status.
- Understand Enforcing, Permissive, and Disabled modes.
- Inspect SELinux configuration.
- Understand runtime state vs configuration.
- Verify whether SELinux is active on a Linux system.
- <img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/79243cd5-e4ca-417f-a5a1-1e105cbf4767" />
