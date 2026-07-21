# Lab 17: Network Tools Overview

## Objectives
- Understand network configuration using ip addr and ifconfig.
- Learn how to test network connectivity using ping.
- Explore DNS resolution using nslookup and dig.
- Understand how these tools are used in real-world networking, cloud computing, and cybersecurity.

---

# Commands Practiced

| Command | Purpose |
|---------|---------|
| ip addr | Display network interfaces, IP addresses, MAC addresses, and network configuration |
| ifconfig | Display network interface information (legacy command) |
| ping google.com | Test network connectivity and reachability |
| nslookup google.com | Query DNS to resolve a domain name into IP addresses |
| dig google.com | Perform an advanced DNS lookup with detailed information |
---

# Key Concepts

## Network Interface
A network interface is the connection through which a computer communicates with a network.

Examples:
- lo → Loopback interface
- ens5 → Main network interface
- docker0 → Docker virtual network

---

## Loopback Interface

- Interface: lo
- IP Address: 127.0.0.1

## IPv4 Address

Displayed after:

text
inet


Example:

text
172.31.10.78/24


The IPv4 address uniquely identifies a device on a network.

---

## MAC Address

Displayed after:

text
link/ether


Example:

text
0a:ff:f8:57:54:99


A MAC Address is the physical hardware address of a network interface.

---

## Docker Network

The docker0 interface is automatically created by Docker.

It provides networking for Docker containers running on the host machine.

---

## Ping

ping tests network connectivity by sending ICMP Echo Requests and receiving Echo Replies.

Important output:

- icmp_seq → Sequence number of packets
- time → Round-trip time
- ttl → Time To Live
- 64 bytes → Size of the received packet

A successful ping indicates that the destination is reachable over the network.

---

## DNS (Domain Name System)

DNS translates human-readable domain names into machine-readable IP addresses.

Example:


google.com
        ↓
142.251.xxx.xxx


Without DNS, users would need to remember IP addresses instead of domain names.

DNS primarily uses Port *53*.

---

## nslookup

nslookup queries a DNS server to obtain the IP address associated with a domain name.

It provides:

- DNS Server
- Domain Name
- IPv4 Address(es)
- IPv6 Address(es)

---

## dig

dig (Domain Information Groper) is a more advanced DNS diagnostic tool.

It provides:

- Query Status
- Query Time
- DNS Server
- Question Section
- Answer Section
- Record Types
- Message Size

---

# Practical Work

Successfully performed:

- Displayed network interfaces using ip addr
- Identified the loopback interface (lo)
- Identified the main network interface (ens5)
- Located the IPv4 address
- Located the MAC address
- Observed the Docker virtual network interface
- Tested internet connectivity using ping
- Understood ICMP sequence numbers
- Interpreted round-trip time
- Resolved Google's domain using nslookup
- Observed multiple IPv4 and IPv6 addresses
- Performed an advanced DNS lookup using dig
- Understood status: NOERROR
- Identified the Question Section and Answer Section
- Learned why Google returns multiple IP addresses

---

# Practice Questions

### Q1. Which interface is usually your primary network interface?

*Answer:*
The main interface (such as ens5, eth0, or wlan0) is responsible for network communication.

---

### Q2. Where can you find the IPv4 address in ip addr?

*Answer:*
After the keyword:


inet


---

### Q3. Where can you find the MAC Address?

*Answer:*
After:


link/ether


---

### Q4. Which interface allows a computer to communicate with itself?

*Answer:*


lo


---

### Q5. Why does Docker create the docker0 interface?
*Answer:*
To provide networking for Docker containers.

---

### Q6. What does ping test?

*Answer:*
Network connectivity and reachability.

---

### Q7. What is icmp_seq?

*Answer:*
The sequence number assigned to each ICMP packet.

---

### Q8. What does time=18 ms represent?

*Answer:*
The round-trip time taken for a packet to travel to the destination and back.

---

### Q9. Why do we press Ctrl + C after running ping?

*Answer:*
To stop the continuously running ping command.

---

### Q10. What does a successful ping indicate?

*Answer:*
The destination is reachable and network connectivity exists.

---

### Q11. What does nslookup do?

*Answer:*
It queries DNS to translate a domain name into one or more IP addresses.

---

### Q12. Which port does DNS use?

*Answer:*
Port *53*.

---

### Q13. Why does Google return multiple IP addresses?

*Answer:*
Google uses many servers worldwide for load balancing, redundancy, and faster access.

---

### Q14. What is a Non-authoritative Answer?

*Answer:*
A DNS response provided by a caching or recursive DNS server rather than the domain's official authoritative DNS server.

---

### Q15. What is the difference between a domain name and an IP address?

*Answer:*
Domain names are human-readable, while IP addresses are used by computers to communicate.

---

### Q16. What does status: NOERROR mean in dig?

*Answer:*
The DNS query completed successfully without errors.

---

### Q17. What does the Question Section show?

*Answer:*
The DNS record that was requested.

---

### Q18. What does Query Time represent?

*Answer:*
The time taken by the DNS server to process and return the DNS query.

---

### Q19. Which command provides more detailed DNS information?

*Answer:*
dig

---

# Interview Questions

## 1. What is the difference between ping, nslookup, and dig?

*Sample Answer:*

ping tests network connectivity using ICMP packets.

nslookup resolves a domain name into IP addresses using DNS.

dig performs advanced DNS lookups and provides detailed diagnostic information such as query time, record types, and DNS server information.

---

## 2. What is DNS?

*Sample Answer:*

DNS (Domain Name System) translates human-readable domain names into IP addresses that computers use for communication.

---

## 3. What is the purpose of the loopback interface?

*Sample Answer:*

The loopback interface (127.0.0.1) allows a computer to communicate with itself and is commonly used to test local services.

---

## 4. What is the difference between an IP Address and a MAC Address?

*Sample Answer:*

An IP address identifies a device on a network and can change depending on the network.

A MAC address is the permanent hardware address of a network interface.

---

## 5. Why are multiple IP addresses returned for Google?

*Sample Answer:*

Google operates multiple servers worldwide. DNS returns multiple IP addresses for load balancing, redundancy, and improved performance.

---

## 6. Explain how DNS works when you open google.com.

*Sample Answer:*

When a user enters google.com, the computer sends a DNS query to a DNS server. The DNS server returns the corresponding IP address. The browser then connects to that IP address to load the website.

---

## Real-World Relevance

These commands are widely used by:

- Network Engineers
- System Administrators
- Cloud Engineers
- DevOps Engineers
- SOC Analysts
- Penetration Testers
- Cybersecurity Analysts

They are essential for troubleshooting network connectivity, verifying DNS configuration, diagnosing connectivity issues, and investigating infrastructure problems.

---

# Status

✅ Lab Completed Successfully


---
