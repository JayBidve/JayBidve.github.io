---
title: Directory Bruteforcing
description: Practical exploration of directory and file enumeration techniques using common web reconnaissance tools.
---

# Directory Bruteforcing

## Introduction

I practiced **directory bruteforcing** to understand how hidden files and directories are discovered on web servers.
This technique is commonly used during web application testing to find exposed endpoints.

---

## What is Directory Bruteforcing?

Directory bruteforcing is a technique where predefined wordlists are used to discover hidden directories and files on a web server.

---

## Why Directory Bruteforcing Matters

Many web applications expose sensitive paths unintentionally, such as:

* Admin panels
* Backup files
* Configuration folders

Finding these can lead to serious security issues.

---

## My Hands-On Practice (Kali Linux)

I practiced directory enumeration using tools like **dirb** and **gobuster** on test targets.

### Commands Used

```bash
dirb http://target.com
gobuster dir -u http://target.com -w wordlist.txt
```

---

## Observations

* Different wordlists produce different results
* HTTP status codes help identify valid paths
* Some servers block aggressive scanning
* Rate limiting and WAFs affect results

---


## Key Learnings

* Importance of wordlist selection
* Understanding HTTP response codes
* Ethical scanning practices
* Avoiding unnecessary noise during testing

---

## Conclusion

Directory bruteforcing taught me how misconfigurations can expose hidden parts of web applications and why proper access control is essential.

