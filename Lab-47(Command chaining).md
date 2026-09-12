Lab 47: Command Chaining

📌 Introduction

Command chaining is a feature in Unix-like operating systems that allows multiple commands to be executed in a single line.

Different operators can control whether the next command runs depending on the success or failure of the previous command.

🎯 Lab Objectives

- Understand the concept of command chaining.
- Learn the "&&", "||", and ";" operators.
- Analyze the behavior of different command chaining operators.
- Practice using command chains in different scenarios.

🛠️ Commands & Operators

1. "&&" — AND

The next command runs only if the previous command succeeds.

mkdir demo && cd demo

If "mkdir demo" succeeds, "cd demo" is executed.

2. "||" — OR

The next command runs only if the previous command fails.

cd nonexistent || echo "Failed to enter directory"

If the directory does not exist, the error message is displayed.

3. ";" — Semicolon

The next command runs regardless of whether the previous command succeeds or fails.

cd nonexistent ; pwd

Even though "cd nonexistent" fails, "pwd" still executes.

🧪 Practice

Using "&&"

touch file.txt && echo "File created successfully"

Using "||"

ls xyz.txt || echo "File does not exist"

Using ";"

echo "First" ; echo "Second"

Combining Commands

mkdir test && cd test && echo "Inside test"

🧠 Key Takeaways

Operator| Behavior
"&&"| Run the next command if the previous command succeeds
`| 
";"| Run the next command regardless of the previous result

✅ Lab Status

Lab 47 — Completed and Practiced Successfully
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/d147c87a-e9c8-4239-845a-c2b8af4c2721" />
