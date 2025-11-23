# Nmap & Port Scanning Notes

## What is Nmap?
Nmap (Network Mapper) is a tool used to discover hosts, scan ports, detect services, and identify vulnerabilities on a network.

## Why It’s Important
- Essential for penetration testing
- Helps find open ports and services
- Used in reconnaissance (recon) on TryHackMe and HackTheBox
- Helps understand how attackers find weak entry points

## Basic Commands
- `nmap 192.168.1.1`  
  Scan a single target

- `nmap 192.168.1.0/24`  
  Scan an entire network

- `nmap -p 80 192.168.1.1` 
  Scan a specific port

- `nmap -p 1-65535 192.168.1.1`  
  Scan all ports

- `nmap -sV 192.168.1.1`  
  Detect service versions

- `nmap -O 192.168.1.1`  
  Detect OS

- `nmap -A 192.168.1.1`  
  Aggressive scan (OS + version + scripts)

## Common Ports
- **80** – HTTP  
- **443** – HTTPS  
- **22** – SSH  
- **53** – DNS  
- **21** – FTP  
- **25** – SMTP  
- **3306** – MySQL  
- **3389** – RDP  

## What You Learn From Nmap
- What services a machine is running
- If the machine is Windows/Linux
- Which ports are open/closed/filtered
- Possible vulnerabilities
