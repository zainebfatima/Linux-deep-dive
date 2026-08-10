 # Day 30 — SSH Basics 🔐

## Lab: SSH Basics

### Objectives

- Understand the Secure Shell (SSH) protocol and its usage.
- Learn how to generate SSH keys.
- Transfer SSH public keys to a remote host.
- Connect to a remote server using SSH without requiring a password.

---

## What is SSH?

SSH (Secure Shell) is a protocol used to securely connect to and manage a remote computer over a network.

It is commonly used by system administrators, developers, and cybersecurity professionals to access and manage Linux servers remotely.

### Simple Example

```text
My Computer
     |
     | SSH
     ↓
Remote Linux Server
 Instead of physically sitting in front of the server, we can access its terminal remotely through SSH.
Commands Practiced
Check SSH version
ssh -V
Used to check whether SSH is available and which version is installed.
Check SSH service
sudo systemctl status ssh
Used to check whether the SSH server is running.
Start SSH service
sudo systemctl start ssh
Used to start the SSH server.
Generate SSH keys
ssh-keygen
This generates an SSH key pair:
id_ed25519 → Private key 🔒
id_ed25519.pub → Public key 🔓
View SSH files
ls -la ~/.ssh
Used to verify the SSH directory and key files.
View public key

cat ~/.ssh/id_ed25519.pub
Used to display the public key before transferring it to a remote server.
Private Key vs Public Key
Private Key 🔒
The private key must remain secret.
It should never be uploaded to GitHub or shared with anyone.
Public Key 🔓
The public key can be placed on the remote server.
The server uses it to verify the client during SSH authentication.
What I Learned
Today I understood that SSH allows us to securely access another computer/server remotely.
I also learned that SSH key authentication uses a pair of keys:
Private Key + Public Key
The private key stays with the client, while the public key is placed on the remote server.
The goal of key-based authentication is to allow secure SSH login without repeatedly entering the account password.
Practice Notes
I practiced:
Checking SSH installation
Starting and checking the SSH service
Generating Ed25519 SSH keys
Finding SSH key files
Understanding public vs private keys
Understanding how SSH authentication works
The actual remote-host key transfer and passwordless SSH connection will be practiced separately using two independent Linux environments.
Security Note 🔐
Never share or upload:
id_ed25519
The private key must remain secret.
Only the public key:
id_ed25519.pub
is intended to be transferred to a remote server
