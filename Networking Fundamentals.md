# Networking Fundamentals

This document contains the essential networking concepts needed for beginners.  
It covers the OSI model, TCP/IP model, data encapsulation, IPv4, subnets, routing, TCP vs UDP, and core terminology.

---

## 1. OSI Model

The OSI (Open Systems Interconnection) model is a 7-layer conceptual framework used to understand how data travels across networks.

| Layer | Name             | Function                                    |
|------:|------------------|----------------------------------------------|
| 7     | Application      | User applications and protocols             |
| 6     | Presentation     | Encoding, encryption, compression           |
| 5     | Session          | Session creation and management             |
| 4     | Transport        | Reliable/unreliable delivery (TCP/UDP)      |
| 3     | Network          | IP addressing and routing                   |
| 2     | Data Link        | Frames, MAC addresses                        |
| 1     | Physical         | Bits, cables, frequencies                   |

---

## 2. TCP/IP Model (Internet Model)

| TCP/IP Layer  | OSI Layers Included | Examples                     |
|---------------|----------------------|------------------------------|
| Application   | 5 + 6 + 7            | HTTP, DNS, SMTP, FTP         |
| Transport     | 4                    | TCP, UDP                     |
| Internet      | 3                    | IP, ICMP, IPSec              |
| Link          | 1 + 2                | Ethernet, Wi-Fi              |

---

## 3. Network Data Units

| Layer        | Data Unit Name              |
|--------------|------------------------------|
| Application  | Data                         |
| Transport    | TCP Segment / UDP Datagram   |
| Network      | Packet                       |
| Data Link    | Frame                        |
| Physical     | Bits                         |

---

## 4. IPv4 Addressing

- IPv4 = 32 bits = 4 octets.
- Example: `192.168.66.89`

Special addresses:
- `.0` → Network address  
- `.255` → Broadcast address (in /24 networks)

---

## 5. Subnet Mask & CIDR

Example:
- IP: `192.168.66.89`
- Mask: `255.255.255.0`
- CIDR: `/24`

CIDR meaning:
- `/24` → the first 24 bits identify the network.
- Host range → `.1` → `.254`

---

## 6. Private vs Public IP

Private IPv4 ranges:

- `10.0.0.0/8`
- `172.16.0.0/12`
- `192.168.0.0/16`

Characteristics:
- Used in LANs.
- Not routable on the Internet.
- Require NAT for external communication.

Public IP:
- Globally routable on the Internet.

---

## 7. Routing Basics

A router:
- Operates at **Layer 3**.
- Forwards packets based on destination IP.
- Uses routing tables and next-hop decisions.

---

## 8. TCP vs UDP

### **TCP**
- Connection-oriented  
- Reliable  
- Uses 3-way handshake  
- Ensures correct ordering  

Used by:
- HTTPS
- SSH
- FTP

### **UDP**
- Connectionless  
- Unreliable (no retransmission)  
- Very fast  

Used by:
- DNS
- DHCP
- NTP
- VoIP

---

## 9. Encapsulation

### Sending:
Application Data  
→ TCP/UDP segment  
→ IP packet  
→ Ethernet/Wi-Fi frame  
→ Bits through medium

### Receiving:
Bits → Frame → Packet → Segment → Data

Encapsulation explains how **each layer adds its own header** during transmission.

---

## 10. Summary

This document covered:

- OSI & TCP/IP models  
- Layer responsibilities  
- Data units (Segment, Packet, Frame)  
- IPv4 addressing  
- Subnet masks & CIDR  
- Private/public IP  
- Routing fundamentals  
- TCP vs UDP  
- Encapsulation workflow  

These form the foundation of all networking and cybersecurity learning.
