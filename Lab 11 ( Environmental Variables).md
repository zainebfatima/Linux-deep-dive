# Lab 11: Environment Variables

## Objectives
- Understand what environment variables are and how they function within an operating system
- Learn how to view, set, and unset environment variables using command-line tools
- Demonstrate the use of environment variables in scripts and shell operations

## Commands Practiced

| Command | Purpose |
|---|---|
| echo $VARNAME | Print the value of a specific environment variable |
| env | List all currently set environment variables |
| export VARNAME="value" | Create/set a new environment variable |
| env \| grep VARNAME | Search the environment list for a specific variable |
| unset VARNAME | Remove an environment variable |

## Key Concepts
- Environment variables are named values the shell stores, which programs 
  and commands can read — e.g. $HOME (home directory), $USER 
  (username), $PATH (where the system looks for commands)
- A variable has a *name* and a *value* — these are different things. 
  export MYNAME="AIYLA" means the variable name is MYNAME and its 
  value is AIYLA; accessing it requires echo $MYNAME, not echo $AIYLA
- unset only works on the actual variable name — attempting to unset 
  a value (mistaking it for the name) does nothing and produces no error
- env lists every currently active environment variable in NAME=value 
  format, useful for confirming a variable was set correctly

## Practice Log
- Viewed common environment variables: $HOME, $USER, $PATH
- Ran env to see the full list of active environment variables
- First attempt: created MYNAME="AIYLA" but mistakenly tried accessing 
  it as $AIYLA (the value) instead of $MYNAME (the name) — this 
  returned nothing, since AIYLA was never a variable name
- Corrected the mistake by properly using $MYNAME to retrieve the value, 
  confirmed with env | grep MYNAME
- Removed the variable using unset MYNAME, confirmed echo $MYNAME 
  returned empty afterward

## Status
✅ Lab completed
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/32f58079-ff8b-4b78-95d3-fb16e12deb47" />

