---
title: Google Dorking
description: Using advanced search operators to discover exposed information through passive reconnaissance techniques.
---
# Google Dorking

## Introduction

I practiced **Google Dorking** to understand how sensitive information can be exposed through search engines due to misconfigurations or poor security practices.

---

## What is Google Dorking?

Google Dorking uses advanced search operators to locate sensitive data indexed by search engines, such as files, login pages, and error messages.

---

## Why Google Dorking is Important

Attackers often use search engines as reconnaissance tools because:

* No direct interaction with target servers
* Passive information gathering
* High success rate when misconfigurations exist

---

## My Hands-On Practice

I practiced Google Dorking using various search operators to identify exposed resources for educational purposes.

### Example Dorks Used

```text
site:example.com filetype:pdf
intitle:"index of"
inurl:admin
```

---

## Observations

* Many files are publicly indexed unintentionally
* Search operators can reveal deep information
* Passive recon is powerful and often overlooked
* Data exposure does not require hacking tools

---

## Screenshots (Proof of Practice)

### Google Dorking Result

<img width="1200" height="720" alt="Image 16-01-26 at 6 55 PM" src="https://github.com/user-attachments/assets/f973f446-86a0-4442-b976-53e491522f78" />

<img width="1200" height="720" alt="Image 16-01-26 at 6 56 PM" src="https://github.com/user-attachments/assets/492b01a7-3f29-4a87-8548-a7ae4d93fb59" />


*(Screenshot captured from browser)*

---

## Key Learnings

* Importance of search engine hygiene
* Risks of exposed files and directories
* Value of passive reconnaissance
* Responsible disclosure awareness

---

## Conclusion

Google Dorking showed me how publicly available information can become a serious security risk if not properly managed.
