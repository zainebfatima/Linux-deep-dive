# Lab 14: Basic Process Management

## Objectives
- Understand the basics of process management in a Unix/Linux environment
- Learn to list running processes and interpret the data
- Master the technique of killing a process using both the PID and the process name

## Commands Practiced

| Command | Purpose |
|---|---|
| ps aux | List all running processes with details (user, PID, CPU/memory usage, command) |
| ps -u $USER | List only the current user's processes |
| top | Interactive, real-time view of running processes (q to quit) |
| sleep 300 & | Start a process and run it in the background using & |
| ps aux \| grep processname | Find a specific process and its PID using piping |
| kill PID | Terminate a process using its process ID number |

## Key Concepts
- Every running program is a *process*, and each process gets a unique 
  *PID* (Process ID) assigned by the system
- ps aux output includes the owning user, PID, resource usage, and the 
  command that started the process
- & at the end of a command runs it in the background, freeing up the 
  terminal immediately instead of waiting for it to finish
- kill takes a plain PID number — no brackets, quotes, or the word "PID" 
  should be typed literally; the < and > symbols are redirection 
  operators (from Lab 13) and will cause a "No such file or directory" 
  error if mistakenly included
- System-owned processes (owned by root) should not be killed 
  carelessly, especially ones unrelated to what's being tested

## Practice Log
- Listed all running processes with ps aux, reviewed columns for user, 
  PID, and command
- Used top to view a live, auto-updating process list
- Started a safe test process: sleep 300 &, noted the returned PID
- Found the PID using piping: ps aux | grep sleep (applying Lab 13's 
  piping concept directly)
- First kill attempts failed: kill <PID 3893> and similar syntax 
  triggered bash: PID: No such file or directory, because < was 
  being interpreted as input redirection, not as a placeholder symbol
- Correct command: kill 3893 (plain PID number only) — successfully 
  terminated the process
- Verified termination by re-running ps aux | grep sleep — the sleep 
  process no longer appeared

## Status
✅ Lab completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/b7c3f50d-035a-437b-ab73-f20e05baee23" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/573212b9-2a5f-4c45-a345-cd9d3ef5f077" />

