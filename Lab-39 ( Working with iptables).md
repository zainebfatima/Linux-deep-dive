Lab 39: Working with iptables

🎯 Objectives

- Understand how to list existing "iptables" rules.
- Learn how to allow or block specific ports using "iptables".
- Understand how to save "iptables" rules.

📚 What is iptables?

"iptables" is a Linux firewall tool used to control network traffic.

It allows us to create rules that decide whether network traffic should be allowed or blocked.

Compared to UFW, "iptables" provides more detailed and lower-level control over firewall rules.

🏢 Real-Life Example

Think of a computer as an office building and "iptables" as the security guard.

The security guard checks network traffic and decides:

- ✅ ACCEPT → Allow the traffic
- ❌ DROP → Block the traffic

Main Chains

- INPUT → Traffic coming into the computer.
- OUTPUT → Traffic going out of the computer.
- FORWARD → Traffic passing through the computer.

🔍 Listing Existing Rules

To check the existing "iptables" rules:

sudo iptables -L

To see more detailed information:

sudo iptables -L -v -n

Important options

- "-L" → List rules
- "-v" → Show detailed information
- "-n" → Display addresses and ports numerically

🔓 Allowing a Port

To allow incoming TCP traffic on SSH port 22:

sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT

Command breakdown

- "-A" → Add a rule
- "INPUT" → Incoming traffic
- "-p tcp" → TCP protocol
- "--dport 22" → Destination port 22
- "-j ACCEPT" → Allow the traffic

In simple words:

«Allow incoming TCP traffic on port 22.»

🚫 Blocking a Port

To block incoming TCP traffic on port 23:

sudo iptables -A INPUT -p tcp --dport 23 -j DROP

This means:

«Block incoming TCP traffic on port 23.»

🧠 Important Concepts Learned

Term| Meaning
iptables| Linux firewall tool
INPUT| Incoming traffic
OUTPUT| Outgoing traffic
FORWARD| Traffic passing through
ACCEPT| Allow traffic
DROP| Block traffic
"--dport"| Destination port
"-A"| Add a rule
Chain| A list/group of firewall rules

💾 Saving iptables Rules

Firewall rules added with "iptables" may not automatically survive a system reboot.

On Debian/Ubuntu systems, one common method is using "iptables-persistent" and "netfilter-persistent".

Example:

sudo apt install iptables-persistent

Then rules can be saved with:

sudo netfilter-persistent save

And reloaded with:

sudo netfilter-persistent reload

Note: The saving method can vary depending on the Linux distribution and lab environment.

✅ Lab 40 Summary

In this lab, I learned how to:

- Check existing "iptables" firewall rules.
- Understand INPUT, OUTPUT, and FORWARD chains.
- Allow incoming traffic on a specific port.
- Block incoming traffic on a specific port.
- Understand ACCEPT and DROP actions.
- Understand why firewall rules may need to be saved for persistence.
- <img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/d0042a17-34e5-406b-be02-1602393a7f32" />
