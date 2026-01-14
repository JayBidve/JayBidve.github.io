---
title: Nmap Scanning
description: Practical usage of Nmap for network reconnaissance and port scanning.
---

# Nmap Scanning

Nmap (Network Mapper) is a powerful open-source tool used for **network discovery** and **security auditing**.  
This page documents my hands-on practice with Nmap and the key techniques I learned.

---

## Objective

- Identify open ports and services<img width="1920" height="1080" alt="Screenshot_2026-01-13_06_01_18" src="https://github.com/user-attachments/assets/6c81299e-88b1-4cd0-9a3f-f45f5fcf481e" />
<img width="1920" height="1080" alt="Screenshot_2026-01-13_06_01_09" src="https://github.com/user-attachments/assets/4b9b11c4-2cec-45a4-8ecd-df664a33327b" />

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






