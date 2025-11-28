<p align="center">
  <img src="https://raw.githubusercontent.com/Firas-Belarbi/Networking-Basics/main/Concepts%20de%20R%C3%A9seau%20et%20Cybers%C3%A9curit%C3%A9.png" width="100%" alt="Networking Banner">
</p>

<h1 align="center">📡 Networking Basics — Summary Notes</h1>
<p align="center">
  Foundations of modern computer networking — written from the perspective of a cybersecurity student.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Level-Beginner-blue?style=flat-square">
  <img src="https://img.shields.io/badge/Category-Networking-green?style=flat-square">
  <img src="https://img.shields.io/badge/Platform-TryHackMe-red?style=flat-square">
  <img src="https://img.shields.io/badge/Labs-Included-orange?style=flat-square">
</p>

---

# 📘 Table of Contents

- [1. Introduction](#1-introduction)
- [2. OSI Model](#2-osi-model-open-systems-interconnection)
- [3. TCP/IP Model](#3-tcpip-model-internet-stack)
- [4. Ports & Protocols](#4-ports--protocols)
- [5. Packet Structure](#5-packet-structure)
- [6. Wireshark Basics](#6-wireshark-basics)
- [7. Nmap CheatSheet](#7-nmap-cheatsheet)
- [8. Advanced Networking Concepts](#8-advanced-networking-concepts)
- [9. Packet Life Journey](#9-packet-life-journey)
- [10. Author](#10-author)

---

# 🔥 1. Introduction

Networking is the foundation of all communication systems.  
Understanding it is essential for:

- Cybersecurity  
- Ethical hacking  
- SOC analysis  
- Penetration testing  
- System administration

This repo is a clean, organized collection of notes from:

- TryHackMe networking rooms  
- University networking courses  
- Hands-on labs  
- Wireshark captures  
- TCP/IP analysis  

---

# 🛰️ 2. OSI Model (Open Systems Interconnection)

| Layer | Name | Description |
|------|------|-------------|
| 7 | Application | End-user protocols (HTTP, DNS, SMTP) |
| 6 | Presentation | Encoding, encryption, compression |
| 5 | Session | Manages sessions between hosts |
| 4 | Transport | TCP/UDP, segmentation, reliability |
| 3 | Network | Routing, IP addresses, ICMP |
| 2 | Data Link | MAC addresses, frames |
| 1 | Physical | Bits, cables, radio |

---

# 🌐 3. TCP/IP Model (Internet Stack)

| Layer | Equivalent in OSI | Examples |
|------|-------------------|----------|
| Application | 5–7 | HTTP, DNS, FTP, SSH |
| Transport | 4 | TCP, UDP |
| Internet | 3 | IP, ICMP, IPSec |
| Network Access | 1–2 | Ethernet, Wi-Fi |

---

# 🔌 4. Ports & Protocols

| Port | Protocol | Description |
|------|----------|-------------|
| 22 | SSH | Secure remote login |
| 53 | DNS | Name resolution |
| 80 | HTTP | Web traffic |
| 443 | HTTPS | Encrypted web |
| 67/68 | DHCP | IP assignment |
| 25 | SMTP | Email sending |
| 110 | POP3 | Email retrieval |
| 445 | SMB | Windows file sharing |

**Port Ranges**

- **0–1023** → Well-known  
- **1024–49151** → Registered  
- **49152–65535** → Dynamic  

---

# 📦 5. Packet Structure

[ Ethernet Frame ]
├── Dest MAC
├── Source MAC
├── EtherType
└── [ IP Packet ]
├── Src/Dst IP
├── TTL
├── Protocol (TCP/UDP)
└── [ TCP/UDP Segment ]
├── Src/Dst Ports
├── Flags
└── [ Application Data ]


---

# 🧪 6. Wireshark Basics

**Useful Filters:**

http
dns
tcp.flags.syn == 1
tcp.port == 80
udp.port == 53
ip.addr == 192.168.1.1



**Shortcuts:**

- Follow → TCP Stream  
- Apply as Filter → Selected  
- Statistics → Protocol Hierarchy  

---

# 🛰️ 7. Nmap CheatSheet

nmap -sV -sC IP
nmap -p- IP
nmap -A IP
nmap -Pn IP
nmap --script vuln IP



---

# 🚀 8. Advanced Networking Concepts

## 🔵 ARP (Address Resolution Protocol)

Maps **IP → MAC address**

arp -a # View ARP cache



**ARP Cache Example:**

| IP | MAC | Type |
|----|------|------|
| 192.168.1.1 | 00:11:22:33:44:55 | Dynamic |
| 192.168.1.10 | aa:bb:cc:dd:ee:ff | Static |

---

## 🔵 DNS Resolution Flow

Client → Resolver → Root → TLD → Authoritative → Response


---

## 🔵 DHCP (DORA)

- Discover  
- Offer  
- Request  
- Acknowledge  

---

## 🔵 NAT Types

- **SNAT** → Change Source IP  
- **DNAT** → Change Destination IP  
- **PAT** → Many→One (Router uses one public IP)

---

## 🔵 VLANs Basics

- Traffic segmentation  
- Access vs Trunk ports  
- VLAN ID tagging (802.1Q)

---

## 🔵 Routing Overview

- **Static Routing**  
- **Dynamic Routing** → OSPF, EIGRP, RIP  
- **Distance Vector vs Link State**

---

# 🧭 9. Packet Life Journey

Application → Transport → Network → Data Link → Physical
Bits → Cable/WiFi → Switch → Router → Internet → Server



---

# 🖊️ 10. Author

**Firas Belarbi**  
CyberSecurity Student  

📌 *This repo is part of my cybersecurity learning roadmap (Networking → Linux → Cryptography → SOC).*

---
