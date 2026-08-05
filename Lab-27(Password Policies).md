# 🔐 Linux Lab 27 – Password Policies

## 🎯 Objectives

- Understand the importance of password policies in enhancing system security.
- Learn to view and modify current password policies on a Linux system.
- Implement password expiry and password ageing requirements.

---

## 📌 Commands Used

### 1️⃣ Create a New User

bash
sudo adduser username


*Purpose:*
Creates a new user account, home directory, and prompts for a password.

*Example:*

bash
sudo adduser zoha


---

### 2️⃣ View Password Policy

bash
sudo chage -l username


*Purpose:*
Displays the current password ageing policy for a user.

*Example:*

bash
sudo chage -l zoha


---

### 3️⃣ Set Maximum Password Age

bash
sudo chage -M 90 username


*Purpose:*
Sets the maximum number of days a password remains valid.

*Example:*

bash
sudo chage -M 90 zoha


---

### 4️⃣ Set Minimum Password Age

bash
sudo chage -m 7 username


*Purpose:*
Specifies the minimum number of days before a user can change the password again.

*Example:*

bash
sudo chage -m 7 zoha


---

### 5️⃣ Set Password Warning Days

bash
sudo chage -W 5 username


*Purpose:*
Displays a warning to the user before the password expires.

*Example:*

bash
sudo chage -W 5 zoha


---

### 6️⃣ Force Password Change

bash
sudo chage -d 0 username


*Purpose:*
Forces the user to change their password at the next login.

*Example:*

bash
sudo chage -d 0 zoha


---

## 📝 What I Learned

- Password policies improve Linux system security.
- chage stands for *Change Age*.
- chage -l displays the current password policy.
- -M sets the maximum password age.
- -m sets the minimum password age.
- -W sets the warning period before password expiry.
- -d 0 forces a user to change their password at the next login.
- Linux warns users when weak passwords are used, but the password may still be accepted depending on the system policy.

---

## 💡 Real-Life Use Cases

- Enforcing company password policies.
- Requiring employees to change passwords regularly.
- Preventing users from changing passwords repeatedly in a short period.
- Warning users before passwords expire.
- Forcing first-time users to set their own secure passwords.

---

## 📚 Key Takeaways

- chage -l → View password policy.
- chage -M → Set maximum password age.
- chage -m → Set minimum password age.
- chage -W → Set password expiry warning period.
- chage -d 0 → Force password change on next login.
- Strong password policies help protect user accounts and organizational data.

Password policies are an essential part of Linux system administration and cybersecurity. They help organizations improve account security by enforcing password ageing, warning users before expiry, and requiring regular password updates.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/8e1c330b-1ebd-45a1-8705-88982ace8f1a" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/e7df3545-3b71-4295-8793-3af677eaa09c" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/173d1927-ba38-460f-a4fa-cad926f8f90e" />


