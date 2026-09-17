Linux Lab 56 — Setting Up Aliases in ".bashrc"

🎯 Objective

Learn how to create command aliases and save them in the ".bashrc" file so they can be loaded automatically in Bash sessions.

---

📚 What is an Alias?

An alias is a shortcut for a command.

Instead of typing a long or frequently used command, we can create a shorter name for it.

For example:

alias l='ls -lah'

Now instead of typing:

ls -lah

I can simply type:

l

---

🧪 Practical

1. Create an Alias

I created the following alias:

alias l='ls -lah'

This created "l" as a shortcut for "ls -lah".

---

2. Add the Alias to ".bashrc"

I added the alias to my Bash configuration file:

nano ~/.bashrc

The alias was added at the bottom of the file:

alias l='ls -lah'

---

3. Reload ".bashrc"

After saving the file, I reloaded the configuration using:

source ~/.bashrc

This makes the changes available in the current shell without needing to close and reopen the terminal.

«Note: I initially typed "sorce" instead of "source", which resulted in "command not found". After correcting the spelling, the command worked successfully.»

---

4. Verify the Alias

I used:

alias

The output showed:

alias l='ls -lah'

This confirmed that the alias was successfully loaded.

---

5. Test the Alias

I ran:

l

The command displayed the same type of detailed directory listing produced by:

ls -lah

✅ The alias worked successfully.

---

🔄 Temporary vs Persistent Aliases

Temporary Alias

If an alias is created directly in the terminal:

alias l='ls -lah'

it works in the current shell.

Persistent Alias

If the alias is added to:

~/.bashrc

and the configuration is reloaded with:

source ~/.bashrc

the alias becomes part of my Bash configuration and will be loaded when a new interactive Bash session starts.

---

🧠 Key Concepts Learned

Command / Concept| Meaning
"alias"| Displays currently defined aliases
"alias l='ls -lah'"| Creates "l" as a shortcut
"~/.bashrc"| Bash configuration file for interactive shells
"source ~/.bashrc"| Reloads ".bashrc" into the current shell
"l"| Runs the command assigned to the alias

---

💡 Important Understanding

The main idea is:

Long Command
     ↓
Create Alias
     ↓
Save Alias in ~/.bashrc
     ↓
source ~/.bashrc
     ↓
Use Short Command

Example:

ls -lah
   ↓
alias l='ls -lah'
   ↓
l

---
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/9fb55f14-2c74-4e5a-a343-f27d07e25a82" />
