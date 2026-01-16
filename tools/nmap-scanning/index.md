---
title: Nmap Scanning
description: Practical usage of Nmap for network reconnaissance and port scanning.
---

# Nmap Scanning

## Introduction

During my cybersecurity learning journey, I practiced **Nmap** to understand how network reconnaissance and service enumeration work in real-world environments.
This tool helped me learn how attackers and defenders identify open ports, running services, and system details.

---

## What is Nmap?

Nmap (Network Mapper) is an open-source tool used for network discovery and security auditing.
It is widely used to identify live hosts, open ports, service versions, and operating systems.

---

## Why Nmap is Important

Nmap is usually the **first tool used** during penetration testing because:

* It reveals the attack surface
* Identifies exposed services
* Helps prioritize vulnerabilities
* Supports both offensive and defensive security

---

## My Hands-On Practice (Kali Linux)

I practiced Nmap on Kali Linux using both **basic and advanced scans** to understand how different flags affect results.

### Commands Used

```bash
nmap -sS -p- <target>
nmap -sV <target>
nmap -A <target>
```

---

## Observations

* SYN scans provided stealthy results
* Version detection revealed service details
* Aggressive scans combined OS, service, and script scanning
* Scan time and verbosity varied based on flags used

This helped me understand how scanning techniques must be chosen carefully.

---

## Screenshots (Proof of Practice)

### Nmap Port Scan on amazon.com

<img width="1200" height="720" alt="Screenshot_2026-01-13_06_01_18" src="https://github.com/user-attachments/assets/29f8ce51-93ec-44ff-9f27-34440125b8f4" />

<img width="1200" height="720" alt="Screenshot_2026-01-13_06_01_09" src="https://github.com/user-attachments/assets/84f8ecef-538d-4988-9292-093119b3bd38" />


*(Screenshot captured from my Kali Linux terminal)*

---

## Key Learnings

* Difference between TCP connect and SYN scans
* Importance of service version detection
* How open ports expose potential vulnerabilities
* Ethical use of scanning tools

---

## Conclusion

Nmap gave me a strong foundation in network reconnaissance.
It showed me how much information can be gathered before even attempting exploitation.







