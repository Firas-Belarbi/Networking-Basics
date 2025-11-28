<p align="center">
  <img src="https://raw.githubusercontent.com/Firas-Belarbi/Networking-Basics/main/Concepts%20de%20R%C3%A9seau%20et%20Cybers%C3%A9curit%C3%A9.png" width="100%" alt="Networking Banner">
</p>

<h1 align="center">Networking Basics — Summary Notes</h1>

<p align="center">
  Foundations of computer networking, written from the perspective of a cybersecurity student.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Level-Beginner-blue?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Category-Networking-green?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/TryHackMe-Networking%20Rooms-red?style=for-the-badge"/>
</p>

---

# 📌 1. Introduction

Networking is the foundation of all modern communication systems.  
Understanding it is essential for cybersecurity, ethical hacking, system administration, and cloud technologies.

This repository is a clean, organized collection of my learning notes from:

- TryHackMe Rooms  
- Hands-on labs  
- Cybersecurity training  
- University networking courses  

---

# 📡 2. OSI Model (Open Systems Interconnection)

| Layer | Name           | Description |
|------|----------------|-------------|
| 7 | Application | Protocols used by end-user apps (HTTP, DNS, SMTP) |
| 6 | Presentation | Encoding, encryption, compression |
| 5 | Session | Opens/closes sessions between hosts |
| 4 | Transport | TCP/UDP, segmentation, reliability |
| 3 | Network | Routing, IP addressing, ICMP |
| 2 | Data Link | MAC addresses, switches, frames |
| 1 | Physical | Cables, radio signals, bits |

### Key Points:
- Layer 3 = IP + Routing  
- Layer 4 = TCP/UDP + Ports  
- Layer 2 = MAC + Switching  

---

# 🌐 3. TCP/IP Model

| TCP/IP Layer | OSI Equivalent | Examples |
|--------------|----------------|----------|
| Application | L5–7 | HTTP, HTTPS, DNS |
| Transport | L4 | TCP, UDP |
| Internet | L3 | IP, ICMP |
| Link | L1–2 | Ethernet, Wi-Fi |

---

# 🔢 4. Data Encapsulation

### When sending data:
Application → Transport (TCP/UDP) → Network (IP) → Data Link (Frame) → Physical (Bits)

### Data unit names:
- Application → Data  
- Transport → Segment / Datagram  
- Network → Packet  
- Data Link → Frame  
- Physical → Bits  

---

# 🌍 5. IPv4 Addressing & Subnetting

### Basic concepts:
- IPv4 = 32-bit address  
- Format: A.B.C.D  
- Example: 192.168.1.45

### CIDR Examples:
| CIDR | Netmask | Hosts |
|------|---------|--------|
| /24 | 255.255.255.0 | 254 hosts |
| /16 | 255.255.0.0 | 65,534 hosts |
| /8  | 255.0.0.0     | 16+ million hosts |

### Private IP ranges:
- 10.0.0.0/8  
- 172.16.0.0/12  
- 192.168.0.0/16  

---

# 🚦 6. Ports & Protocols

### TCP (reliable & connection-oriented):
- 22 SSH  
- 80 HTTP  
- 443 HTTPS  
- 3389 RDP  

### UDP (fast & connectionless):
- 53 DNS  
- 67/68 DHCP  
- 123 NTP  

---

# 🔍 7. Packet Analysis (Wireshark)

Things to check:
- Source & Destination IP  
- TCP Flags (SYN, ACK, FIN)  
- Protocol  
- Layer 7 content (HTTP/DNS)  
- Packet length & timing  

Useful filters:
http
tcp.flags.syn == 1
dns
ip.addr == 192.168.1.10



---

# 📡 8. Nmap Essentials

Common scans:
nmap -sV -sC TARGET
nmap -p- TARGET
nmap -A TARGET
nmap --top-ports 1000 TARGET


