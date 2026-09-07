Lab 43 — Basic LVM Concepts

🎯 Objectives

- Understand the fundamentals of Logical Volume Manager (LVM) in Linux.
- Learn to create and manage Volume Groups and Logical Volumes.
- Practice mounting and using an LVM logical volume.
- Practice removing a Logical Volume safely.

---

🧠 What is LVM?

LVM (Logical Volume Manager) is a Linux storage management system that provides a flexible way to manage disk storage.

Instead of working directly with fixed disk partitions, LVM allows administrators to create logical storage volumes that can be managed and resized more easily.

Basic LVM structure

Physical Disk
     ↓
Physical Volume (PV)
     ↓
Volume Group (VG)
     ↓
Logical Volume (LV)
     ↓
Filesystem
     ↓
Mount Point
     ↓
Files & Directories

In this lab

myvg
  ↓
mylv
  ↓
ext4
  ↓
/mnt/office-data
  ↓
Office files & directories

---

🏢 Real-World Office Example

Imagine a company has a Linux server and the manager says:

«"Create a separate storage area for the Finance department."»

As a Linux administrator, I would manage the storage underneath the normal file system.

For example:

Server Storage
      ↓
     LVM
      ↓
   Logical Volume
      ↓
   ext4 filesystem
      ↓
 /data/finance
      ↓
Invoices / Reports / Budgets

The important idea is that LVM manages the storage, while normal Linux commands such as "mkdir", "touch", "cp", and "ls" are used to work with the files stored on that storage.

---

🛠️ Practical Work

1. Created a Mount Point

A mount point is the directory where a filesystem becomes accessible.

sudo mkdir /mnt/office-data

This created:

/mnt/office-data

At this point, it was just a normal empty directory.

---

2. Mounted the Logical Volume

I connected the LVM logical volume to the mount point:

sudo mount /dev/myvg/mylv /mnt/office-data

Now the storage represented by "mylv" became accessible through:

/mnt/office-data

---

3. Used the LVM Storage

To make the example more realistic, I created an office file inside the mounted storage:

sudo touch /mnt/office-data/report.txt

I verified the file with:

ls -l /mnt/office-data

This demonstrated that normal files and directories can be stored on a filesystem that is backed by an LVM logical volume.

---

4. Created an Office-Style Directory Structure

To understand how this could be used in an actual organization, I created directories such as:

office-data/
├── invoices/
├── reports/
├── budgets/
├── payroll/
└── documents/

The important concept was:

«LVM doesn't replace normal directories. LVM provides/manage the storage underneath them.»

---

🔍 Checking LVM

I used the following commands to inspect the LVM configuration.

Display Logical Volumes

sudo lvs

This displays information about logical volumes.

Display Volume Groups

sudo vgs

This displays information about volume groups.

Display Physical Volumes

sudo pvs

This displays information about physical volumes.

---

🗑️ Safely Removing a Logical Volume

After finishing the practical work, I practiced safely removing the Logical Volume.

Step 1 — Check the data

ls -lah /mnt/office-data

I checked the files before removing the storage.

Step 2 — Unmount the filesystem

sudo umount /mnt/office-data

The logical volume should not be actively mounted before removing it.

Step 3 — Remove the Logical Volume

sudo lvremove /dev/myvg/mylv

I confirmed the removal when prompted.

Step 4 — Verify

sudo lvs

The "mylv" logical volume was no longer listed.

---

🧠 Key Understanding

The most important thing I learned from this lab is that LVM is not simply a way to create folders.

For example:

mkdir reports

creates a directory.

But LVM manages the storage underneath the filesystem where those directories and files are stored.

Without thinking about LVM:

Directory → Files

With LVM:

Physical Storage
       ↓
      LVM
        ↓
Logical Volume
       ↓
Filesystem
       ↓
Mount Point
       ↓
Directories
       ↓
Files

---

💼 Real-World Use

In an actual Linux/server administration job, I might receive tasks such as:

- "Create storage for the Finance department."
- "Give the application server additional storage."
- "Mount storage at "/data/finance"."
- "Check how much storage is available."
- "Increase a logical volume because an application is running out of space."
- "Remove a logical volume that is no longer required."

LVM makes these storage-management tasks more flexible.

---

📝 Commands Practiced

sudo mkdir /mnt/office-data

sudo mount /dev/myvg/mylv /mnt/office-data

sudo touch /mnt/office-data/report.txt

ls -lah /mnt/office-data

sudo lvs
sudo vgs
sudo pvs

sudo umount /mnt/office-data

sudo lvremove /dev/myvg/mylv

---

✅ Lab 44 Completed

Skills Practiced

- Understanding LVM architecture
- Working with Volume Groups
- Working with Logical Volumes
- Mounting an LVM filesystem
- Storing files on LVM-backed storage
- Inspecting LVM configuration
- Safely unmounting storage
- Removing a Logical Volume

 Key Takeaway

«LVM is a flexible storage-management layer in Linux. It allows administrators to manage logical storage independently from the physical disk layout, making it easier to organize, expand, and remove storage when required.»
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/cc0f8dbe-f28f-48ae-bade-2b6ef64ee1b7" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/bb82cd36-5721-4c50-8f2f-9423dc77a79a" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/be610068-8aea-4639-95e3-fcb073e83ac5" />


