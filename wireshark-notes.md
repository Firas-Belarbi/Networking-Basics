# Wireshark Notes

## What is Wireshark?
Wireshark is a packet analyzer used to capture and examine network traffic.

## Why It's Important
- Helps understand how protocols work (TCP, UDP, HTTP…)
- Detects suspicious traffic
- Used in cybersecurity investigations (Incident Response)
- Used for troubleshooting network problems

## Basic Filters
- `ip.addr == X.X.X.X` – Filter traffic from/to an IP
- `tcp` – Show only TCP packets
- `udp` – Show only UDP packets
- `http` – Show only HTTP packets
- `tcp.port == 80` – Filter packets on a port
- `dns` – Show DNS queries

## Key Things You Can Analyze
- Source & Destination IPs
- MAC addresses
- Ports
- HTTP requests (GET/POST)
- DNS requests
- Packet timing and delays
- TCP handshake (SYN, SYN-ACK, ACK)
- TLS negotiation in HTTPS

## Skills Gained
- Capturing packets
- Reading headers
- Identifying protocols
- Filtering traffic efficiently
- Understanding how devices communicate
