# Day 34 — awk for Data Processing

## Lab Objectives

- Understand the basic syntax and functionality of awk.
- Learn how to print specific columns from a file.
- Filter rows based on a given condition.

## What is awk?

awk is a Linux text-processing and data-processing tool.

It is especially useful for working with structured text containing rows and columns.

It can be used to select specific columns, filter rows based on conditions, and perform basic calculations.

## Basic awk Syntax

```bash
awk 'pattern {action}' filename
For example:
awk '{print $1}' employees.txt
This prints the first column from the file.
Understanding Fields and Rows
In awk:
$0 → entire row
$1 → first column
$2 → second column
$3 → third column
For example, if the file contains:
NAME AGE DEPARTMENT
Aiyla 21 IT
Zaroon 24 IT
Zaheer 27 Finance
Alina 22 Marketing
Zara 26 HR
Then:
awk '{print $1}' employees.txt
prints the names.
awk '{print $3}' employees.txt
prints the departments.
Printing Multiple Columns
I practiced printing the name and department columns:
awk '{print $1, $3}' employees.txt
This displays:
NAME DEPARTMENT
Aiyla IT
Zaroon IT
Zaheer Finance
Alina Marketing
Zara HR
Printing the Entire Row
I practiced using $0:
awk '{print $0}' employees.txt
$0 represents the complete current row.
Filtering Rows
awk can filter rows using conditions.
For example, to display employees older than 25:
awk '$2 > 25 {print $0}' employees.txt
This checks the second column (Age) and prints the complete row when the age is greater than 25.
Output:
Zaheer 27 Finance
Zara 26 HR
Using Multiple Conditions
I also practiced combining conditions with &&.
awk '$2 > 25 && $2 < 27 {print $0}' employees.txt
This means:
Age must be greater than 25.
AND age must be less than 27.
Print the complete matching row.
The result is:
Zara 26 HR
Comparison Operators
Some useful comparison operators in awk are:
>   Greater than
<   Less than
>=  Greater than or equal to
<=  Less than or equal to
==  Equal to
!=  Not equal to
Basic Calculations
awk can also perform basic calculations.
For example:
awk '{print $1, $2 + 1}' employees.txt
This prints the employee's name and their age increased by 1.
Practical Use
awk is useful in real-world Linux and system administration tasks.
For example, an administrator may have a large employee, server, or log file and need to:
Extract specific columns.
Find records matching a condition.
Filter information from logs.
Process large amounts of structured text.
Perform simple calculations on data.
For example, to find failed login attempts in a structured log:
awk '$3 == "FAILED" {print $0}' login.log
This filters the rows where the third field contains FAILED.
grep vs sed vs awk
grep
Used mainly to search and filter text.
grep "Linux" practice.txt
sed
Used mainly to modify or transform text.
sed 's/Linux/Ubuntu/g' practice.txt
awk
Used mainly to process structured data, columns, rows, and conditions.
awk '$2 > 25 {print $0}' employees.txt
What I Learned
Today I learned how to:
Understand the basic syntax of awk.
Work with rows and columns.
Use $0 for the complete row.
Use $1, $2, $3 for specific columns.
Print specific columns.
Print multiple columns.
Filter rows using conditions.
Combine multiple conditions using &&.
Use comparison operators.
Perform basic calculations with awk.
Understand practical uses of awk in Linux and system administration.
Practice Completed
Created employees.txt.
Printed the department column.
Printed name and department together.
Printed complete rows using $0.
Filtered employees based on age.
Used greater-than and less-than conditions.
Combined multiple conditions.
Practiced basic calculations.
Connected awk with practical Linux and log-processing tasks.
Key Takeaway
awk is a powerful Linux data-processing tool.
The basic mental model I learned is:
$0 → whole row
$1 → column 1
$2 → column 2
$3 → column 3
The main pattern is:
awk 'condition {action}' file
awk is especially useful when working with structured data where I need to select columns, filter rows, or perform calculations.
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/e79032a0-e83b-4688-a5f2-cbf16aff5946" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/301cbfb9-b268-4f7d-bf51-44eaace241ed" />

