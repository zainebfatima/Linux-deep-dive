Lab 48: Using and Creating Man Pages

📌 Introduction

Man pages (manual pages) are built-in Linux documentation that provide detailed information about commands, their syntax, options, and usage.

In this lab, I learned how to use existing man pages and created a custom man page for a simple script.

🎯 Lab Objectives

- Understand how to use existing man pages.
- Learn how to navigate and extract information from manual pages.
- Create a custom man page for a simple script.
- Install and view a custom manual page.

📖 Using Existing Man Pages

The "man" command is used to view the manual page of a Linux command.

Example:

man mkdir

The manual page provides information such as:

- Command name
- Syntax
- Description
- Available options

For example:

man mkdir

helped me understand options such as:

-p
-v

Quick Help vs Man Pages

mkdir --help

provides a quick summary, while:

man mkdir

provides more detailed documentation.

🛠️ Creating a Custom Script

I created a simple script named "greet".

nano greet

The script contained:

#!/bin/bash
echo "Hello, welcome to Linux!"

I then made the script executable:

chmod +x greet

And tested it:

./greet

📄 Creating a Custom Man Page

I created a custom manual page using Nano:

nano greet.1

The man page contained:

.TH GREET 1
.SH NAME
greet \- print a welcome message
.SH DESCRIPTION
The greet script prints a welcome message.
.SH EXAMPLE
./greet

📥 Installing the Custom Man Page

I copied the manual page into the Linux man-page directory:

sudo cp greet.1 /usr/share/man/man1/

Then I updated the manual-page database:

sudo mandb

Finally, I viewed my custom manual page:

man greet

🧠 Important Learning

Linux filenames are case-sensitive.

For example:

Greet
greet
greet.1

are different filenames.

During the lab, I encountered a filename issue because the file was initially saved with a different name. Troubleshooting this helped me understand how Linux handles filenames and paths.

🔑 Key Takeaways

- "man" is Linux's detailed built-in documentation system.
- "--help" provides quick command information.
- Man pages can be created for custom scripts.
- ".1" is used for section 1 manual pages.
- "mandb" updates the manual-page database.
- Custom manuals can be accessed using the same "man" command as built-in manuals.

✅ Lab Status

Lab 48 — Completed Successfully

I successfully created, installed, updated, and viewed my own custom Linux man page.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/5e359029-f76c-433c-9cf2-9fc9eec29439" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/775bccf9-de33-4e09-8774-a7a63da08f39" />

