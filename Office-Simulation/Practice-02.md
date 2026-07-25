# 🏢 Office Simulation

## Scenario

Your manager asked you to:

- Create employee documents.
- Compress them into a ZIP archive.
- Delete the originals.
- Recover everything from the backup.

### Files Created

- salary.txt
- attendance.txt
- leave.txt

### Created Archive

bash
zip employee.zip salary.txt attendance.txt leave.txt


### Deleted Original Files

bash
rm salary.txt attendance.txt leave.txt


### Restored Files

bash
unzip employee.zip


Result:

All deleted files were successfully recovered.

---
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/0498003c-747e-4441-8e39-ce11d098d27a" />
