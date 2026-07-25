# 🧪 Lab 21: Package Management - APT

## 🎯 Objectives

- Understand the basics of package management using APT (Advanced Package Tool).
- Learn how to update package lists.
- Learn how to search, install and remove software packages.
- Gain practical experience managing software on a Debian-based Linux system.

---

# 📚 Concepts Learned

## What is APT?

APT (Advanced Package Tool) is the package manager used in Debian-based Linux distributions such as Ubuntu.

It allows users to:

- Update package lists
- Search for software
- Install software
- Remove software
- Manage software dependencies

Think of APT as the Linux equivalent of the Play Store or Microsoft Store, but controlled through the terminal.

---

## Why do we use APT?

Instead of downloading software from random websites:

- It installs software from trusted repositories.
- It automatically installs required dependencies.
- It makes updating software easy.
- It is more secure and reliable.

---

# 🛠️ Commands Practiced

## Update package list

bash
sudo apt update


Purpose:

Refreshes the package database so Ubuntu knows about the latest available software.

---

## Search for a package

bash
apt search nmap


Purpose:

Searches the repositories for packages matching the given name.

---

## Install a package

bash
sudo apt install nmap


Purpose:

Downloads and installs the package along with any required dependencies.

---

## Remove a package

bash
sudo apt remove nmap


Purpose:

Removes the installed package from the system.

---

## Remove unused dependencies

bash
sudo apt autoremove


Purpose:

Removes packages that were automatically installed but are no longer needed.

---

# 🧠 Interview Questions

## Q1. What does APT stand for?

Advanced Package Tool.

---

## Q2. What is APT used for?

APT is used to search, install, update and remove software packages on Debian-based Linux systems.

---

## Q3. Does sudo apt update install software?

No.

It only refreshes the package list.

---

## Q4. Which command installs a package?

bash
sudo apt install package_name


---

## Q5. Which command removes a package?

bash
sudo apt remove package_name


---

## Q6. What is a dependency?

A dependency is another package that a program requires in order to work correctly.

APT installs dependencies automatically.

---

## Q7. What does sudo apt autoremove do?

It removes unnecessary packages that were installed automatically but are no longer required.

---

# ❓ Questions I Asked Myself During Practice

### Why does Linux use APT instead of downloading software from websites?

Because official repositories are more secure and reliable than downloading software from random websites.

---

### Can I create my own APT?

No.

APT is already an installed package manager provided by Ubuntu.

---

### Why did Ubuntu say "packages are no longer required"?

Because they were installed automatically as dependencies and became unnecessary after removing the main package.

---

### Does apt search verify that a package is installed?

No.

It searches the repositories.

To verify installation, run the program (e.g. tree) or check its version (e.g. tree --version).

---

# 🚀 Key Takeaways

- APT is Ubuntu's package manager.
- apt update refreshes the package list.
- apt search searches available packages.
- apt install installs software.
- apt remove removes installed software.
- apt autoremove cleans unused dependencies.
- APT automatically handles dependencies.

- 


