[6:26 pm, 22/07/2026] ...: # Lab 19: Compressing with gzip and bzip2

## Objectives
- Understand the basics of file compression and decompression.
- Learn to use gzip and bzip2 for compressing files.
- Practice using gunzip and bunzip2 for decompression.
- Understand the differences and use cases of gzip and bzip2.

## Commands Practiced

| Command | Purpose |
|---|---|
| gzip notes.txt | Compress a file using gzip |
| gunzip notes.txt.gz | Decompress a gzip-compressed file |
| bzip2 data.txt | Compress a file using bzip2 |
| bunzip2 data.txt.bz2 | Decompress a bzip2-compressed file |
| cat filename | Display file contents |
| ls | List files in the current directory |

## Key Concepts

- Compression reduces file size to save storage space and make file transfer faster.
- gzip and bzip2 are *lossless compression* tools, meaning no data is lost during compression.
- After decompression, the original file is restored exactly as it was.
- gzip replaces the original file with a compressed file having the .gz extension.
- bzip2 replaces the original file with a compressed file having the .bz2 extension.
- gunzip restores .gz files back to their original form.
- bunzip2 restores .bz2 files back to their original form.
- Compression is different from archiving.
- tar groups multiple files into one archive, while gzip and bzip2 reduce file size.
- A compressed file contains the complete original data and does not summarize or remove information.

## gzip vs bzip2

| Feature | gzip | bzip2 |
|---|---|---|
| Compression Speed | Faster | Slower |
| Compression Ratio | Lower | Higher |
| CPU Usage | Lower | Higher |
| Best Use Case | Quick compression | Better space saving |

## Practice Log

- Created a text file using touch.
- Added content using nano.
- Verified the file using cat.
- Compressed the file using gzip.
- Observed that the original file was replaced by a .gz file.
- Restored the original file using gunzip.
- Created another practice file.
- Compressed it using bzip2.
- Restored it using bunzip2.
- Compared gzip and bzip2 based on speed and compression efficiency.

## Real-World Uses

- Compressing server log files.
- Reducing backup storage requirements.
- Faster file transfer over networks.
- Saving cloud storage space.
- Compressing Linux software packages and archives.

## Interview Questions

### Q1. What is file compression?
*Answer:* File compression reduces the size of a file while preserving its data, making storage and file transfer more efficient.

### Q2. What is the difference between compression and archiving?
*Answer:* Archiving combines multiple files into a single file, while compression reduces the file size. A .tar file is an archive, whereas .gz and .bz2 are compressed files.

### Q3. Does gzip remove or summarize file contents?
*Answer:* No. gzip uses lossless compression, meaning all original data is preserved and restored perfectly during decompression.

### Q4. What happens to the original file after running gzip filename?
*Answer:* The original file is replaced with a compressed file ending in .gz.

### Q5. Which command restores a gzip-compressed file?
*Answer:* gunzip filename.gz

### Q6. Which command restores a bzip2-compressed file?
*Answer:* bunzip2 filename.bz2

### Q7. Which compression tool is faster?
*Answer:* gzip is faster.

### Q8. Which compression tool usually produces a smaller compressed file?
*Answer:* bzip2 usually provides better compression but is slower.

### Q9. Are gzip and bzip2 lossless or lossy compression tools?
*Answer:* Both use lossless compression, meaning no data is lost.

## Status

✅ Lab Completed Successfully
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/50334ed7-80ec-4949-a3fd-4164437b8f58" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/6470d470-7f43-444a-9b3f-c471d3fa861d" />

