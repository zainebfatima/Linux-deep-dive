[4:45 pm, 29/07/2026] ...: # 👥 Linux Lab 25 – Creating and Managing Users

## 🎯 Objectives

- Understand the process of creating, managing, and deleting users in a Linux environment.
- Gain familiarity with essential commands such as useradd, passwd, and userdel.
- Learn the basics of user permissions and privilege management.

---

## 📌 Commands Used

### 1️⃣ Create a New User

bash
sudo useradd username


*Purpose:*
Creates a new user account on the Linux system.

*Example:*

bash
sudo useradd zoha


---

### 2️⃣ Set a Password

bash
sudo passwd username


*Purpose:*
Sets or changes the password of a user.

*Example:*

bash
sudo passwd zoha


---

### 3️⃣ Delete a User

bash
sudo userdel username


*Purpose:*
Deletes a user account.

*Example:*

bash
sudo userdel zoha


---

### 4️⃣ Delete a User Along with Home Directory

bash
sudo userdel -r username


*Purpose:*
Deletes the user account and removes the user's home directory.

---

### 5️⃣ Display Current Logged-in User

bash
whoami


*Purpose:*
Displays the username of the currently logged-in user.

---

### 6️⃣ Display User Information

bash
id


*Purpose:*
Displays the User ID (UID), Group ID (GID), and groups of the current user.

---

### 7️⃣ Display Information of a Specific User

bash
id username


*Purpose:*
Displays information about a specific user.

*Example:*

bash
id zoha


---

### 8️⃣ Switch User

bash
su username


*Purpose:*
Switches from the current user to another user.

*Example:*

bash
su zoha


---

### 9️⃣ View User Information File

bash
cat /etc/passwd


*Purpose:*
Displays all user accounts stored on the system.

---

### 🔟 Search for a Specific User

bash
grep username /etc/passwd


*Purpose:*
Searches for a specific user in the /etc/passwd file.

*Example:*

bash
grep zoha /etc/passwd


---

## 📝 What I Learned

- Linux allows multiple users to exist on the same system.
- Every user has a unique User ID (UID) and Group ID (GID).
- useradd creates a new user account.
- passwd sets or changes a user's password.
- userdel removes a user account.
- whoami displays the currently logged-in user.
- id displays information about the current user.
- id username displays information about a specific user.
- su switches to another user account.
- /etc/passwd stores user account information (not passwords).
- sudo runs commands with administrator (root) privileges.

---

## 💡 Real-Life Use Cases

- Creating user accounts for employees.
- Managing multiple users on Linux servers.
- Resetting user passwords.
- Removing inactive user accounts.
- Switching between user accounts for testing.
- Viewing user information for troubleshooting.

---

## 📚 Key Takeaways

- *useradd* → Create a new user.
- *passwd* → Set or change a password.
- *userdel* → Delete a user.
- *whoami* → Show the current logged-in user.
- *id* → Display user and group information.
- *su* → Switch to another user.
- *sudo* → Execute commands with administrator privileges.
- */etc/passwd* → Stores user account information.

Understanding Linux user management is essential for system administration, security, and access control. It helps administrators manage user accounts, assign privileges, and maintain a secure Linux environment.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/146bf9b8-f4ab-447b-bd3c-eeff7c9ee1fc" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/64106415-78d8-41c0-a7ab-03a49717497b" />


