# 🌐 Network Fundamentals Parts 1-3 — Cheat Sheet & Learning Reflection

This cheat sheet compiles essential commands, concepts, and reflections from **Network Fundamentals Parts 1, 2, and 3** on [TryHackMe](https://tryhackme.com/), covering networking basics, protocols, troubleshooting, and security.

---

## 📚 Table of Contents

- [Part 1: Networking Basics](#part-1-networking-basics)
- [Part 2: Protocols and Ports](#part-2-protocols-and-ports)
- [Part 3: Network Troubleshooting & Security](#part-3-network-troubleshooting--security)
- [Reflection: What I Learned](#reflection-what-i-learned)

---

## 🧩 Part 1: Networking Basics

### Key Concepts
- **IP Address**: Unique identifier for a device on a network  
- **Subnet Mask**: Divides IP into network and host parts  
- **Default Gateway**: Device that routes traffic outside the local network  
- **MAC Address**: Hardware address of network interface

### Basic Commands
```bash
ipconfig          # Windows - Display IP config
ifconfig          # Linux/macOS - Display IP config
ping <address>    # Test connectivity to an IP or domain
tracert <address> # Windows traceroute
traceroute <address> # Linux/macOS traceroute
```

---

## 🔌 Part 2: Protocols and Ports

### Common Protocols
| Protocol | Port | Description                |
|----------|------|----------------------------|
| HTTP     | 80   | Web traffic                |
| HTTPS    | 443  | Secure web traffic         |
| FTP      | 20/21| File transfer              |
| SSH      | 22   | Secure shell               |
| DNS      | 53   | Domain name resolution     |
| SMTP     | 25   | Sending emails             |
| POP3     | 110  | Receiving emails           |
| IMAP     | 143  | Receiving emails (advanced)|

### Port Scanning
```bash
nmap -p 1-65535 <target>   # Scan all ports
nmap -sV <target>          # Detect service versions
```

---

## 🔧 Part 3: Network Troubleshooting & Security

### Troubleshooting Commands
```bash
netstat -an          # List active connections and listening ports
nslookup <domain>    # Query DNS servers
arp -a               # Display MAC-IP mappings
route print          # View routing table
```

### Network Security Concepts
- **Firewalls**: Control incoming/outgoing network traffic  
- **VPNs**: Secure encrypted tunnels over the internet  
- **IDS/IPS**: Intrusion detection/prevention systems monitor malicious traffic

---

## 🧠 Reflection: What I Learned

- Developed a solid understanding of fundamental **networking concepts** such as IP addressing, subnetting, and gateways  
- Learned to identify and use common **network protocols and their ports** crucial for network communication and troubleshooting  
- Gained hands-on experience using powerful tools like **ping, traceroute, nslookup, netstat, and nmap** for diagnostics and scanning  
- Explored essential **network security basics** including firewall roles and VPNs  
- Overall, this combined knowledge equips me with the foundational skills to analyze, troubleshoot, and secure network environments confidently

---

## 🔗 Related Links

- [TryHackMe: Network Fundamentals](https://tryhackme.com/)

---
