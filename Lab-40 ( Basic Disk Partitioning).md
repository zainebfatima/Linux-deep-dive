Lab 40: Basic Disk Partitioning

Objective

- Understand disk partitioning and its use in disk management.
- Learn how to list available disks and partitions.
- Create and delete partitions using open-source tools.

What I Learned

A disk is the main storage device where the operating system, files, applications, and other data are stored.

A partition is a smaller section created inside a disk. Partitioning helps organize and manage storage.

For safe practice, I created a 100 MB virtual disk instead of modifying the actual system disk.

Commands Used

1. List disks and partitions

lsblk

This displays available storage devices and their partitions.

Important columns for this lab:

- NAME – Name of the disk or partition
- SIZE – Storage size
- TYPE – Type of device, such as disk, partition, or loop device

2. Create a Practice Disk

truncate -s 100M ~/practice-disk.img

This created a 100 MB disk image file for safe practice.

3. Attach the Image as a Virtual Disk

sudo losetup --find --show ~/practice-disk.img

This attached the disk image as a loop device, such as:

/dev/loop10

4. Check the Disk

lsblk /dev/loop10

5. Open the Disk with fdisk

sudo fdisk /dev/loop10

Inside "fdisk":

n → Create a new partition
p → Select primary partition
w → Write/save changes

6. Verify the Partition

sudo fdisk -l /dev/loop10

The created partition appeared as:

/dev/loop10p1

7. Refresh the Loop Device

sudo losetup -P /dev/loop10

Then:

lsblk /dev/loop10

Practice

I created a partition on the 100 MB virtual disk and then deleted it using "fdisk".

The practice was performed on "/dev/loop10" instead of the real system disk, avoiding changes to the Ubuntu system.

Key Takeaway

Disk = big storage box 📦

Partition = smaller section inside the disk 🗂️

The basic workflow is:

List disks
   ↓
Identify the correct disk
   ↓
Create a partition
   ↓
Verify it
   ↓
Delete the partition

Lab Status

✅ Lab 41 Completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/1f6f8162-7e44-46a6-99b2-79efe0367232" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/84360765-2f02-4efc-b76a-6d7d20a39380" />

