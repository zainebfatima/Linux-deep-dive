# 📦 Lab 22: Package Management – YUM/DNF

> "Learning package management across different Linux distributions." 📦🐧

---

## 🎯 Objectives

- Understand basic package management concepts using *YUM* and *DNF*.
- Perform common package management tasks: updating, searching, installing, and removing packages.
- Gain confidence in managing software packages on RPM-based Linux distributions.

---

## 📚 Key Concepts

### What is a Package Manager?

A package manager is a tool used to install, update, search, and remove software packages on a Linux system.

### Package Managers by Distribution

| Distribution | Package Manager |
|--------------|-----------------|
| Ubuntu / Debian | APT |
| Fedora | DNF |
| CentOS / RHEL | YUM / DNF |

Although this lab introduced *YUM/DNF, I practiced the equivalent commands using **APT* on Ubuntu.

---

## 💻 Commands Practiced

### Update Package Lists

bash
sudo apt update


### Install a Package

bash
sudo apt install nmap


### Search for a Package

bash
apt search tree


### View Package Details

bash
apt show tree


### Verify Installed Software

bash
curl --version


### View Command History

bash
history


---

## 🏢 Office Simulation

### 🎫 Ticket #001 – Install Network Tool

bash
sudo apt install nmap


Installed *Nmap* for network administration tasks.

---

### 🎫 Ticket #002 – Search for Software

bash
apt search tree


Searched the repository for the *tree* package.

---

### 🎫 Ticket #003 – Inspect Package Information

bash
apt show tree


Viewed package details including version, maintainer, dependencies, download size, and description.

---

### 🎫 Ticket #004 – Verify Installed Software

bash
curl --version


Verified that *curl* was installed and checked its version, supported protocols, and features.

---

### 🎫 Ticket #005 – Review Command History

bash
history


Reviewed previously executed commands for learning and troubleshooting.

---

## 🧠 What I Learned

- Linux distributions use different package managers.
- Ubuntu uses *APT, while Fedora uses **DNF* and CentOS/RHEL use *YUM/DNF*.
- apt search searches for available packages.
- apt show displays detailed package information.
- curl --version verifies installed software.
- history helps review previously executed commands.
- Package managers simplify software installation and maintenance.

---

## ✅ Lab Status

*Lab 22: Completed Successfully 🎉*
