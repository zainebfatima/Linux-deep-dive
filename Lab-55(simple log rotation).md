 Linux Lab 55 — Simple Log Rotation

🎯 Objectives

- Understand the basics of log rotation in Linux.
- Learn how to inspect logrotate configuration files.
- Understand rotation frequency and log retention.
- Learn how old logs are compressed and numbered.
- Gain hands-on experience manually initiating log rotation.

---

📚 What is Log Rotation?

Log rotation is a Linux process that manages growing log files.

Instead of allowing one log file to grow forever, Linux can:

1. Rename the current log as an old/rotated copy.
2. Create a new empty log file.
3. Compress older copies.
4. Keep only a specified number of old copies.
5. Remove the oldest copy when the retention limit is reached.

Simple Example

If a configuration has:

weekly
rotate 4

It means:
- "weekly" → check/rotate the log weekly.
- "rotate 4" → keep 4 old rotated copies.

So there can be approximately:

current log
old copy 1
old copy 2
old copy 3
old copy 4

When another rotation occurs, the oldest copy is removed.

---

🔍 Checking Logrotate Version

Command:

logrotate --version

This showed that Logrotate was installed and available.

It also showed:

- Default compression: "gzip"
- Compressed extension: ".gz"
- State file: "/var/lib/logrotate/status"

---

⚙️ Main Logrotate Configuration

Command:

cat /etc/logrotate.conf

Important directives:

"rotate 4"

Keeps 4 old rotated copies.

"create"

Creates a new empty log file after rotation.

"include /etc/logrotate.d"

Loads additional log rotation configurations for individual services.

---

📂 Individual Service Configurations

Command:

ls /etc/logrotate.d/

This showed configurations for services such as:

apt
rsyslog
ufw
cloud-init
dpkg
chrony
unattended-upgrades

The main configuration provides general rules, while files inside "/etc/logrotate.d/" can define service-specific rules.

---

📦 Example: APT Log Configuration

Command:

cat /etc/logrotate.d/apt

APT logs had rules such as:

rotate 12
monthly
compress
missingok
notifempty

Meaning

- "monthly" → rotate monthly.
- "rotate 12" → keep 12 old copies.
- "compress" → compress old logs, usually into ".gz" files.
- "missingok" → don't report an error if the log is missing.
- "notifempty" → don't rotate an empty log.

This showed that not every log has to use the same rotation schedule or retention period.

---

🧪 Debug / Dry Run

Command:

sudo logrotate -d /etc/logrotate.conf

"-d" means debug mode.

It shows what Logrotate would do without actually performing the rotation.

The output showed Logrotate checking different logs and deciding whether they needed rotation based on their configured rules.

---

🔄 Manually Forcing Log Rotation

Command:

sudo logrotate -f /etc/logrotate.conf

"-f" means force rotation.

It tells Logrotate to perform rotation immediately, even when a log would normally not be due for rotation yet.

The command produced no visible output, which was normal because Logrotate can run silently when there are no errors.

---

👀 Verifying the Rotation

Command:

ls -lh /var/log/apt/

After forcing rotation, I could see files such as:

history.log
history.log.1.gz
history.log.2.gz
history.log.3.gz

term.log
term.log.1.gz
term.log.2.gz
term.log.3.gz

What this demonstrated

history.log
    ↓
history.log.1.gz
    ↓
history.log.2.gz
    ↓
history.log.3.gz

The current log remains available for new entries, while previous versions are stored as rotated copies.

The ".gz" extension showed that the older logs had been compressed.

---

🧠 Key Concepts Learned

"weekly"

Controls how often a log is normally rotated.

"monthly"

Rotates the log monthly.

"rotate 4"

Keeps 4 old rotated copies.

"rotate 12"

Keeps 12 old rotated copies.

"compress"

Compresses old rotated logs.

"create"

Creates a new empty current log after rotation.

"notifempty"

Does not rotate an empty log.

"missingok"
Does not complain if the log file is missing.

"-d"

Debug/dry-run mode — shows what would happen without actually rotating.

"-f"

Force rotation immediately.

---

📝 Final Understanding

Logrotate prevents log files from growing indefinitely.

The basic flow is:

Current Log
     ↓
Rotation
     ↓
Old Log → Compressed → Numbered
     ↓
New Empty Current Log
     ↓
Oldest Copy Eventually Removed

The important thing to remember is:

«Rotation decides what happens to old logs, while the "rotate" value controls how many old copies are retained.»

---
