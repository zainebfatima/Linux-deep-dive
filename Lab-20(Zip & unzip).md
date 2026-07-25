# 🧪 Lab 20: Working with zip and unzip

## 🎯 Objectives

- Understand how to compress files using zip.
- Learn how to extract compressed archives using unzip.
- Practice creating and recovering ZIP archives.
- Understand the difference between zip, tar, and gzip.

---

# 📚 Concepts Learned

## What is ZIP?

ZIP is an archive format that *archives and compresses files at the same time*.

Unlike tar, which only bundles files together, zip creates a compressed archive that is commonly used on Windows, Linux, and macOS.

Example:

report.txt  
budget.txt  
meeting.txt

↓

project.zip

---

## Difference between tar, gzip and zip

| Command | Purpose | Original Files |
|---------|----------|---------------|
| tar | Archives files | Remain unchanged |
| gzip | Compresses one file | Original replaced with .gz |
| bzip2 | Compresses one file | Original replaced with .bz2 |
| zip | Archives and compresses | Original files remain |

---

# 🛠️ Commands Practiced

## Check ZIP version

bash
zip -v


Purpose:
Displays the installed ZIP version and supported features.

---

## Create practice files

bash
touch report.txt budget.txt meeting.txt


---

## Create a ZIP archive

bash
zip project.zip report.txt budget.txt meeting.txt


Purpose:
Creates project.zip containing all three files.

---

## Verify files

bash
ls


---

## Delete original files

bash
rm report.txt budget.txt meeting.txt


Purpose:
Simulates accidental deletion.

---

## Recover files

bash
unzip project.zip


Purpose:
Extracts all files from the archive.

---

## Overwrite existing files automatically

bash
unzip -o project.zip


Purpose:
Extracts files without asking before replacing existing ones.

---

---

# 🧠 Interview Questions

## Q1. What is the difference between tar and zip?

*Answer:*

tar only archives files into one package and does not significantly compress them.

zip archives and compresses files simultaneously.

---

## Q2. What does unzip do?

*Answer:*

unzip extracts files from a ZIP archive.

Example:

bash
unzip project.zip


---

## Q3. Why did ZIP display "stored (0%)" instead of "deflated"?

*Answer:*

- The file was too small to benefit from compression.
- Compressing it would not reduce its size.

ZIP stored it without compression.

---

## Q4. What does "deflated" mean?

*Answer:*

It means the file was compressed successfully.

Example:


budget.txt (deflated 14%)


The file became 14% smaller.

---

## Q5. Why did unzip ask "Replace report.txt?"?

*Answer:*

Because a file with the same name already existed.

Linux asked whether to overwrite the existing file.

---

## Q6. Why is ZIP commonly used?

*Answer:*

- Works on Windows, Linux and macOS.
- Easy to email.
- Archives and compresses files together.
- Widely supported.

---

# ❓ Questions I Asked Myself During Practice

### Why were some files "stored" while others were "deflated"?

Small or already efficient files may not benefit from compression, so ZIP stores them without compressing.

---

### Why does ZIP keep the original files?

ZIP creates a new archive while leaving the originals untouched.

Unlike gzip, it does not replace the source files.

---

### Why did unzip ask before extracting?

Because files with the same names already existed.

Linux prevented accidental overwriting.

---

# 🚀 Key Takeaways

- zip archives and compresses simultaneously.
- unzip restores files from ZIP archives.
- ZIP keeps original files unchanged.
- stored means no compression.
- deflated means the file was compressed.
- unzip -o overwrites existing files automatically.
- ZIP is one of the most common archive formats used in professional environments.
- <img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/a8a160a8-c51d-4dc6-bcf2-7fe1e926af13" />
