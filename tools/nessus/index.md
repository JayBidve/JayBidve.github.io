---

title: Nessus Vulnerability Scanning
description: Practical hands-on usage of Nessus for vulnerability assessment with ethical consent.
--------------------------------------------------------------------------------------------------

## Objective

The objective of this practice was to understand how **Nessus** is used for **vulnerability assessment** in a real-world environment. I performed an ethical scan on a friend’s device after taking proper consent, strictly for learning and educational purposes. This helped me understand how vulnerabilities are detected, categorized, and reported using an industry-standard security tool.

---

## Tool Overview

**Nessus** is a widely used vulnerability assessment tool developed by **Tenable**. It is designed to identify security weaknesses such as misconfigurations, outdated software, weak services, and known vulnerabilities (CVEs) in systems and networks.

Nessus is commonly used by:

* Penetration testers
* Security analysts
* Blue teams
* Compliance and audit professionals

It does not exploit vulnerabilities but safely **detects and reports** them.

---

## Ethical Considerations

Before starting the scan, I ensured:

* Explicit permission was taken from the device owner
* The scan was performed only on the authorized target
* The activity was strictly for educational and ethical learning

This aligns with ethical hacking principles and legal compliance.

---

## Environment Setup

* Platform: Kali Linux
* Nessus Version: Nessus Essentials
* Target: Friend’s personal device (with consent)
* Scan Type: Basic Network Scan

Nessus was accessed via the web interface:

```
https://localhost:8834
```

---

## Scan Configuration Process

1. Logged into the Nessus web dashboard
2. Created a new scan
3. Selected **Basic Network Scan** template
4. Entered the target IP address
5. Adjusted scan settings (default safe checks enabled)
6. Launched the scan

The scan took several minutes to complete depending on the services running on the target system.

---

## Scan Results and Observations

After the scan completed, Nessus categorized the findings based on severity:

* **Low Severity Issues**

  * Informational disclosures
  * Open services running with default configurations

* **Medium Severity Issues**

  * Outdated software versions
  * Weak protocol configurations

No critical vulnerabilities were found, which indicates that the system was relatively secure but still had areas for improvement.

Each vulnerability included:

* Description
* Risk level
* CVE reference (if applicable)
* Suggested remediation steps

---

## Vulnerability Analysis

Nessus provided clear explanations of:

* Why the vulnerability exists
* How it can potentially be abused
* Recommended fixes or mitigation steps

This helped me understand not only *what* the issue was, but *why* it matters from a security perspective.

---

## Screenshots Evidence

Below are screenshots taken during the practical session:

* Nessus dashboard
* Scan configuration page
* Scan progress
* Vulnerability results summary

<img width="1920" height="1080" alt="Screenshot_2026-01-14_05_30_49" src="https://github.com/user-attachments/assets/87fe40c4-858a-451c-8c33-dcf53c709bc3" />

<img width="1920" height="1080" alt="Screenshot_2026-01-14_05_30_44" src="https://github.com/user-attachments/assets/f645dcc6-dc8b-4bd4-b798-ab9cc868851d" />

<img width="1920" height="1080" alt="Screenshot_2026-01-14_05_15_14" src="https://github.com/user-attachments/assets/b9c5af89-5858-4722-9f8a-a850036eca93" />


*(Screenshots attached for documentation and proof of practice)*

---

## Learning Outcome

From this practical exercise, I learned:

* How to set up and run a Nessus scan
* How vulnerability severity levels are classified
* How to analyze scan reports
* The importance of ethical permission before scanning

This hands-on experience improved my understanding of real-world vulnerability assessment workflows.

---

## Conclusion

Nessus is a powerful and reliable tool for identifying security weaknesses in systems. Even small or low-severity vulnerabilities can become serious risks if ignored. This practice session gave me practical exposure to vulnerability scanning and reinforced the importance of proactive security assessment.

I will continue using Nessus in controlled and ethical environments to further strengthen my cybersecurity skills.
