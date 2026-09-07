Lab 44: Introduction to "/etc/fstab"

---

🎯 Objectives

- Understand the purpose of "/etc/fstab".
- Learn how to view and understand existing "/etc/fstab" entries.
- Learn about filesystems, mount points and UUIDs.
- Practice adding a filesystem mount entry to "/etc/fstab".
- Understand how "/etc/fstab" helps with persistent/automatic mounting.

---

🧠 What is "/etc/fstab"?

"fstab" stands for Filesystem Table.

It is a Linux configuration file located at:

/etc/fstab

It contains instructions about which filesystems should be mounted, where they should be mounted, and which options should be used.

Easy Definition

«"/etc/fstab" = Linux's saved instructions for mounting filesystems.»

---

💡 Why Do We Need "/etc/fstab"?

Normally, we can manually mount a filesystem:

sudo mount /dev/nvme1n1p2 /mnt/removable

But after a reboot, we may need to mount it again.

With "/etc/fstab", we can configure the filesystem once.

/etc/fstab
     ↓
Stores mounting instructions
     ↓
System reboots
     ↓
Linux reads the configuration
     ↓
Configured filesystem can be mounted automatically

Main Advantage

It prevents administrators from having to manually mount the same configured filesystems after every reboot.

---

💾 Disk

A disk is the actual storage device.

Example:

/dev/nvme1n1

Think:

«Disk = whole storage device.»

---

🧩 Partition

A partition is a section of a disk.

Example:

/dev/nvme1n1p2

Here:

nvme1n1 = disk
p2      = partition 2

Think:

«Partition = a section of the disk.»

---

📁 Filesystem

A filesystem organizes and manages files and directories on storage.

Common filesystems include:

ext4
xfs
btrfs
vfat

---

🐧 ext4

"ext4" is one of the commonly used Linux filesystems.

We created an ext4 filesystem on our partition using:

sudo mkfs.ext4 /dev/nvme1n1p2

Important

"mkfs.ext4" creates a new ext4 filesystem on the specified device.

⚠️ Formatting a device can erase existing data, so always verify the device before using "mkfs".

---

🔗 Mount

Mounting means making a filesystem accessible through a directory.

Example:

sudo mount /dev/nvme1n1p2 /mnt/removable

The filesystem is then accessible through:

/mnt/removable

Easy Definition

«Mount = connect a filesystem to a location in Linux.»

---

🔓 Unmount

Unmounting means removing the filesystem from its mount point.

Command:

sudo umount /mnt/removable

Easy Definition

«Unmount = safely disconnect the filesystem from that location.»

---

🆔 UUID

UUID stands for Universally Unique Identifier.

Each filesystem normally has its own UUID.

Example:

38523502-180c-4da2-8e04-a7dd63782ab2

We can find it using:

sudo blkid

or:

lsblk -f

Why UUID?

Instead of depending only on a device name such as:

/dev/sdb1

Linux can identify the filesystem using its UUID.

Easy Definition

«UUID = unique ID of a filesystem.»

---

📋 Understanding an "/etc/fstab" Entry

Example:

UUID=ABC123 /data ext4 defaults 0 2

The six fields are:

WHAT → WHERE → TYPE → OPTIONS → DUMP → CHECK

Field| Meaning
"UUID=ABC123"| Which filesystem?
"/data"| Where to mount it?
"ext4"| Filesystem type
"defaults"| Mount options
"0"| Dump/backup setting
"2"| Filesystem check order

---

🛠️ Practical Lab

Step 1 — Check existing disks

lsblk -f

---

Step 2 — Check the unused disk

We found an additional disk:

/dev/nvme1n1

We checked it using:

sudo fdisk -l /dev/nvme1n1

It was an empty 30 GiB disk.

---

Step 3 — Create a partition

We opened "fdisk":

sudo fdisk /dev/nvme1n1

Created a primary partition.

Our partition became:

/dev/nvme1n1p2

---

Step 4 — Create an ext4 filesystem

sudo mkfs.ext4 /dev/nvme1n1p2

This created an ext4 filesystem on the partition.

---

Step 5 — Find the UUID

sudo blkid /dev/nvme1n1p2

Our filesystem UUID was:
38523502-180c-4da2-8e04-a7dd63782ab2

---

Step 6 — Create a mount point

sudo mkdir -p /mnt/removable

---

Step 7 — Add the filesystem to "/etc/fstab"

We opened:

sudo nano /etc/fstab

Added:

UUID=38523502-180c-4da2-8e04-a7dd63782ab2 /mnt/removable ext4 defaults 0 2

---

Step 8 — Test mounting

We tried:

sudo mount -a

The UUID-based mount produced an error in our environment even though "blkid" showed the UUID correctly.

We then tested the device directly:

sudo mount /dev/nvme1n1p2 /mnt/removable

This worked successfully. ✅

We verified that the filesystem was mounted at:

/mnt/removable

---

🔍 Troubleshooting Lesson

An important lesson from this lab:

blkid
 ↓
UUID can be found ✅

Manual mount
 ↓
Filesystem mounts successfully ✅

mount -a
 ↓
UUID-based mount failed in our environment ❌

This showed that the filesystem itself was working, while the problem was specifically related to the UUID-based "/etc/fstab" mount attempt.

Troubleshooting principle:

«Don't immediately recreate or format the filesystem when a mount fails. First determine whether the problem is with the filesystem, device, mount point, or configuration.»

---

🔄 Mount vs "/etc/fstab"

"mount"

sudo mount /dev/nvme1n1p2 /mnt/removable

Means:

«"Mount this filesystem now."»

"/etc/fstab"

UUID=... /mnt/removable ext4 defaults 0 2

Means:

«"Remember that this filesystem should be mounted at this location with these settings."»

---

🏢 How "/etc/fstab" Is Used in Real Work

Linux administrators, system administrators, cloud engineers and DevOps engineers may configure persistent storage using "/etc/fstab".

For example, a server might have:

System storage
     ↓
/

Application storage
     ↓
/data

Backup storage
     ↓
/backup

The administrator can configure these filesystems in:

/etc/fstab

They don't normally edit `/etc/fstab every day.

It is usually changed when:

- New storage is added.
- A new filesystem needs to be mounted.
- A mount point changes.
- Mount options need to change.
- Persistent mounting needs to be configured.

---

🔥 Complete Concept

DISK
  ↓
PARTITION
  ↓
FILESYSTEM
  ↓
UUID
  ↓
MOUNT POINT
  ↓
/etc/fstab
  ↓
Persistent mounting configuration
  ↓
REBOOT
  ↓
Linux can mount the configured filesystem

---

🧠 Quick Revision

Disk
= Actual storage device

Partition
= Section of a disk

Filesystem
= Organizes files on storage

ext4
= Common Linux filesystem

UUID
= Unique identifier of a filesystem

Mount
= Make a filesystem accessible at a directory

Unmount
= Safely disconnect a filesystem from its mount point

Loop Device
= A file that can be used like a block device

Mount Point
= Directory where a filesystem is attached

/etc/fstab
= Stores persistent filesystem mounting configuration

mount -a
= Attempts to mount filesystems configured in /etc/fstab

---

🎯 Interview Questions

1. What is "/etc/fstab"?

"/etc/fstab" is a Linux configuration file containing information about filesystems, mount points, filesystem types and mount options. It allows configured filesystems to be mounted automatically, including during system boot.

2. Why is UUID
3. UUID uniquely identifies a filesystem and is generally more reliable than depending on a device name such as "/dev/sdb1".

3. What is mounting?

Mounting makes a filesystem accessible through a directory in Linux.

4. What is unmounting?

Unmounting safely removes a filesystem from its mount point.

5. What is ext4?

ext4 is a commonly used Linux filesystem.

6. What does "mount -a" do?

It attempts to mount filesystems configured in "/etc/fstab".

7. Do we edit "/etc/fstab" every day?

No. It is normally modified when filesystem or storage configuration needs to be added or changed.

---

⭐ Final Takeaway

«"/etc/fstab" is like a saved map of filesystem mounting instructions. It tells Linux which filesystem to mount, where to mount it, and which options to use.»

Disk
 ↓
Partition
 ↓
Filesystem
 ↓
UUID
 ↓
Mount Point
 ↓
fstab
 ↓
Automatic/Persistent Mounting

Day 44 Complete ✅🐧
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/7630ee1c-24a9-4d6b-9ba6-02e085a5184a" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/aef5c8e4-c7c3-4777-8854-1c9a324bf3d2" />




