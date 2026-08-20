Lab 37: Systemd Services Overview

🎯 Objectives

- Understand the fundamentals of "systemd" and its role in service management.
- Learn how to use "systemctl" to manage services.
- Practice starting, stopping, restarting, enabling, disabling, and checking the status of services.

📚 What I Learned

What is systemd?

"systemd" is the system and service manager used by many Linux distributions.

It manages system services and controls when they start, stop, and run.

What is systemctl?

"systemctl" is the command-line tool used to communicate with and manage "systemd".

I used "systemctl" to manage the SSH service during this lab.

🛠️ Commands Practiced

Check Service Status

systemctl status ssh

Checks whether the SSH service is currently active or inactive.

Start a Service

sudo systemctl start ssh

Starts the SSH service.

Stop a Service

sudo systemctl stop ssh

Stops the SSH service.

Restart a Service

sudo systemctl restart ssh

Stops and starts the service again.

Enable a Service

sudo systemctl enable ssh

Configures the service to start automatically when the system boots.

Disable a Service

sudo systemctl disable ssh

Prevents the service from starting automatically at boot.

🔍 Important Difference

Active/Inactive tells me whether the service is running right now.

Enabled/Disabled tells me whether the service is configured to start automatically at boot.

For example:

Active + Enabled
→ Running now + starts automatically at boot

Inactive + Enabled
→ Not running now + will start automatically at boot

Active + Disabled
→ Running now + will NOT automatically start at boot

💻 Practical Work

I practiced managing the SSH service by:

- Checking its status
- Starting it
- Stopping it
- Restarting it
- Enabling it
- Disabling it

✅ Lab Status

Completed

Key Takeaway

"systemd" manages services, while "systemctl" allows us to control those services from the Linux command line.
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/c12e39b0-9bb0-42f0-bce7-75bdfacb9de0" />
