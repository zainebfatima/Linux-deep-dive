## Lab 41: Mounting and Unmounting

### 🎯 Objectives
- Understand mounting and unmounting in Linux.
- Learn how to create and manage mount points.
- Mount a filesystem to a directory.
- Unmount a filesystem.

### 🧠 What I Learned

*Mount* means connecting a filesystem/storage device to a directory so that we can access its files through that directory.

*Unmount* means disconnecting the filesystem from the directory. The data is not deleted.

### 🧪 Practical Work

Created a 100 MB virtual disk:

```bash
truncate -s 100M ~/mount-practice.img
Attached it as a loop device:
sudo losetup --find --show ~/mount-practice.img
It appeared as:
/dev/loop10
Created an ext4 filesystem:
sudo mkfs.ext4 /dev/loop10
Created a mount point:
sudo mkdir /mnt/practice
Mounted the filesystem:
sudo mount /dev/loop10 /mnt/practice
Verified the mount:
lsblk
Created a test file:
sudo touch /mnt/practice/hello.txt
Checked the files:
ls -l /mnt/practice
Unmounted the filesystem:
sudo umount /mnt/practice
Verified that the mount point was no longer shown:
lsblk
💡 Key Concept
Storage → Filesystem → Mount Point → Files/Folders
Mounting makes the filesystem accessible through a directory
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/d022b1ea-d04f-457e-b5b0-279107af6c9e" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/1f0d3882-4dba-4f89-8921-49c0ae25be53" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/8e5caa5f-59fc-4826-a61c-ceb5dca77f9e" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/a92287de-0a11-4896-947a-668388bcfbe1" />



