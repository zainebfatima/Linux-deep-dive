# Lab 18: Archiving with tar

## Objectives
- Understand the purpose of tar archives
- Learn how to create a tar archive
- Learn how to list the contents of a tar archive
- Learn how to extract files from a tar archive
- Understand the difference between archiving and compression

## Commands Practiced

| Command | Purpose |
|---|---|
| tar -cvf files.tar eng.txt sci.txt urdu.txt | Create a tar archive containing multiple files |
| tar -tvf files.tar | View the contents of a tar archive without extracting it |
| tar -xvf ../files.tar | Extract files from a tar archive |
| alias T='tar -cvf' | Create a temporary alias for the tar create command |

## Key Concepts
- A tar archive combines multiple files and directories into a single file for easier storage, transfer, and backup.
- Archiving and compression are different concepts. A tar archive groups files together but does not significantly reduce their size.
- Compression reduces the file size using tools like gzip or bzip2.
- tar -cvf creates a new archive.
- tar -tvf displays the table of contents (lists the files inside the archive) without extracting them.
- tar -xvf extracts files from the archive.
- Creating a tar archive does not delete or modify the original files.
- A tar archive acts like a snapshot of files at the moment it was created. Changes made to the original files later are not reflected in the archive unless it is recreated or updated.
- Extracting archives into a separate folder helps avoid overwriting existing files and keeps extracted files organized.

## Practice Log
- Created a practice directory named TarLab.
- Created multiple text files using touch.
- Created the archive files.tar containing eng.txt, sci.txt, and urdu.txt.
- Verified that the original files remained after creating the archive.
- Listed the contents of the archive using tar -tvf and observed file permissions, owner, group, file size, modification date, and filenames.
- Created a temporary alias T for tar -cvf and successfully used it to create another archive.
- Created a separate directory for extraction and extracted the archived files successfully.
- Learned that deleted files can be restored if they still exist inside a tar archive.

## Real-World Uses
- Creating server backups
- Archiving log files before security investigations
- Transferring multiple files as a single package
- Software distribution
- Cloud and Linux system backups
- Disaster recovery and file restoration

## Interview Questions

### Q1. What is a tar archive?
*Answer:* A tar archive is a single file that combines multiple files and directories into one package for easier storage, transfer, and backup.

### Q2. Does a .tar file compress data?
*Answer:* No. A .tar file only archives files. Compression requires tools like gzip or bzip2, resulting in files such as .tar.gz.

### Q3. What does tar -cvf do?
*Answer:* It creates a new tar archive while displaying the names of the files being archived.

### Q4. What does tar -tvf do?
*Answer:* It lists the contents of a tar archive without extracting it.

### Q5. What does tar -xvf do?
*Answer:* It extracts files from a tar archive.

### Q6. If you modify a file after creating a tar archive, will the archive update automatically?
*Answer:* No. A tar archive is a snapshot of the files at the time it was created. Any later changes are not included unless the archive is recreated or updated.

### Q7. Why is it recommended to extract archives into a separate folder?
*Answer:* To avoid overwriting existing files, prevent mixing old and new files, and verify the extracted contents safely.

## Status
✅ Lab completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/b68901d9-1f39-4854-8d1c-cfcba6a66d18" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/a4a1ac50-5279-4ab9-b191-a97c3d1ba740" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/8abe0229-d6a6-40c7-92d9-5a497a7af733" />


