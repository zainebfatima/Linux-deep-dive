[3:49 pm, 05/08/2026] ...: # 👥 Linux Lab 26 – Group Management Basics

## 🎯 Objectives

- Understand the basics of Linux group management.
- Create and manage user groups.
- Add and remove users from groups.
- Learn how groups simplify permission management.

---

## 📌 Commands Used

### 1️⃣ Create a Group

bash
sudo groupadd developers


*Purpose:*
Creates a new group.

---

### 2️⃣ Verify the Group

bash
grep developers /etc/group


*Purpose:*
Checks whether the group exists.

---

### 3️⃣ Create a User

bash
sudo useradd zoha


*Purpose:*
Creates a new user.

---

### 4️⃣ Set User Password

bash
sudo passwd zoha


*Purpose:*
Sets or changes the user's password.

---

### 5️⃣ Add User to a Group

bash
sudo usermod -aG developers zoha


*Purpose:*
Adds the user to the specified group while keeping existing group memberships.

---

### 6️⃣ View User Groups

bash
groups zoha


*Purpose:*
Displays all groups the user belongs to.

---

### 7️⃣ Remove User from a Group

bash
sudo gpasswd -d zoha developers


*Purpose:*
Removes the user from the specified group.

---

### 8️⃣ Delete a Group

bash
sudo groupdel developers


*Purpose:*
Deletes the group.

---

## 📝 What I Learned

- A group is a collection of users.
- /etc/group stores group information.
- groupadd creates a new group.
- usermod -aG adds a user to a group without removing existing groups.
- groups displays the groups a user belongs to.
- gpasswd -d removes a user from a group.
- groupdel deletes a group.
- Groups make permission management easier because permissions can be assigned to an entire group instead of individual users.

---

## 💡 Real-Life Use Cases

- Creating departments such as Developers, HR, Finance, and IT.
- Granting permissions to an entire team.
- Managing multiple users efficiently.
- Organizing users based on their roles.

---

## 📚 Key Takeaways

- groupadd → Create a group.
- usermod -aG → Add a user to a group.
- groups → View user groups.
- gpasswd -d → Remove a user from a group.
- groupdel → Delete a group.
- /etc/group → Stores group information.

Linux groups simplify user management by allowing administrators to assign permissions to multiple users at once instead of configuring each user individually.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/19b3c938-c0c5-4014-97c0-72fbef72b26e" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/3540e109-4538-4293-88eb-4dfeff64ac06" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/712076ad-223f-40d7-9003-feabe1e01968" />


