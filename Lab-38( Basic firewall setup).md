Lab 38: Basic Firewall Setup (UFW)

Objectives

- Understand the basic concept of a firewall and its importance in system security.
- Learn to install and configure UFW (Uncomplicated Firewall) on a Linux-based system.
- Enable and configure basic firewall rules using UFW.
- Verify and test the firewall setup to ensure traffic is being correctly controlled.

What I Learned

A firewall is a security mechanism that controls network traffic entering or leaving a system. It can allow or block connections based on configured rules.

UFW (Uncomplicated Firewall) is a simple firewall management tool for Linux.

It works like a security guard that decides which network connections are allowed and which are blocked.

Commands Practiced

Check UFW Status

sudo ufw status

Used to check whether the firewall is active or inactive.

Enable UFW

sudo ufw enable

Enabled the firewall.

Set Default Incoming Policy

sudo ufw default deny incoming

Blocks incoming connections by default unless they are specifically allowed.

Set Default Outgoing Policy

sudo ufw default allow outgoing

Allows outgoing connections by default.

Allow SSH

sudo ufw allow 22/tcp

Allowed TCP traffic on port 22, which is commonly used by SSH.

Check Detailed Status

sudo ufw status verbose

The "verbose" option displays more detailed information about the firewall, including:

- Firewall status
- Logging status
- Default incoming policy
- Default outgoing policy
- Routed traffic policy
- Configured rules

Add a Deny Rule

sudo ufw deny 23/tcp

Temporarily denied TCP traffic on port 23.

View Numbered Rules

sudo ufw status numbered

Displays firewall rules with numbers, making them easier to identify and manage.

Delete the Test Rule

sudo ufw delete deny 23/tcp

Removed the temporary deny rule for port 23.

Final Configuration

After completing the lab:

- UFW was active.
- Incoming traffic was denied by default.
- Outgoing traffic was allowed by default.
- TCP port 22 (SSH) was allowed.
- Port 23 was temporarily denied for testing and then the rule was removed.

Key Terms

- Firewall: Controls network traffic.
- UFW: Uncomplicated Firewall for Linux.
- Incoming: Traffic coming into the system.
- Outgoing: Traffic going out from the system.
- Port: A numbered endpoint used by network services.
- TCP: A transport protocol used for reliable network communication.
- Verbose: Shows detailed information.
- Numbered: Displays firewall rules with rule numbers.

Practical Environment

The practical commands were successfully practiced using Killercoda because the Al-Nafi lab machine was repeatedly being terminated due to a cloud-service issue.

Lab Status

Completed ✅
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/9b6eab01-f502-496c-a3a7-b6dea257fd78" />
