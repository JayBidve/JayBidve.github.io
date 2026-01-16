# Directory Bruteforcing

## Overview
Directory bruteforcing is used to discover hidden files and directories on a web server by systematically testing common paths.

## Tools Used
- dirsearch
- gobuster
- feroxbuster

## Example Commands
```bash
gobuster dir -u www.microsoft.com -w wordlist.txt
```
What I Learned

How hidden endpoints can expose sensitive functionality
Importance of proper access controls
Risks of directory listing and misconfigurations
