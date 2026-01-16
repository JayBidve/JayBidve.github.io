# WAF Detection

## Overview
Web Application Firewall (WAF) detection identifies whether a web application is protected by a security filtering layer and determines the WAF vendor.

## Tools Used
- wafw00f
- nmap (http-waf-detect script)

## Example Commands
```bash
wafw00f https://target.com
nmap --script http-waf-detect -p 80,443 target.com
