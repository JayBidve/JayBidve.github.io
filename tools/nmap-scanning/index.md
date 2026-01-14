---
title: Nmap Scanning
description: Practical usage of Nmap for network reconnaissance and port scanning.
---

# Nmap Scanning

Nmap (Network Mapper) is a powerful open-source tool used for **network discovery** and **security auditing**.  
This page documents my hands-on practice with Nmap and the key techniques I learned.

---

## Objective

- Identify open ports and services
- Detect operating systems and service versions
- Understand real-world reconnaissance workflows

- Observations & Learning
	•	Open ports often reveal unnecessary exposed services
	•	Version detection helps identify vulnerable software
	•	Aggressive scans are noisy and should be used carefully
	•	Firewall behavior can be inferred from filtered ports

⸻

Ethical Note

All scans were performed in controlled lab environments or with explicit authorization, strictly for educational purposes.

---

## Common Commands Used

### Basic Scan
```bash
nmap 19.167.1.1
nmap -p 80,443 19.167.1.1
nmap -sV 19.167.1.1
nmap -O 19.167.1.1
nmap -A 19.167.1.1
```






