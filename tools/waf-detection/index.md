# WAF Detection (wafw00f)

## Introduction

As part of my web application security practice, I worked with **wafw00f**, a tool used to detect the presence and type of Web Application Firewalls (WAFs) protecting a website.
This exercise helped me understand how defensive security mechanisms are deployed on real-world applications and how they affect reconnaissance activities.

---

## What is wafw00f?

wafw00f is an open-source reconnaissance tool that identifies Web Application Firewalls by analyzing HTTP responses and fingerprinting known WAF behaviors.
It is commonly used during the initial assessment phase of web security testing.

---

## Why WAF Detection Matters

Before performing any web security testing, it is important to know whether a target is protected by a WAF because:

* WAFs can block or modify requests
* Some attacks may trigger alerts or bans
* Testing techniques must be adjusted accordingly

Understanding WAF presence helps in choosing safer and more effective testing methods.

---

## My Hands-On Practice (Kali Linux)

I practiced wafw00f on my Kali Linux machine to gain practical experience.
For learning purposes, I tested the tool against **well-known, large-scale websites** to observe how enterprise-grade defenses behave.

### Commands Used

```bash
wafw00f https://paytm.com
wafw00f https://amazon.com
```

---

## Observations

* The tool successfully detected the presence of Web Application Firewalls.
* It provided insights into the type of protection being used.
* Responses differed based on how the WAF handled probes and filtering.
* This demonstrated how major platforms actively protect their infrastructure.

This practice helped me understand that modern web applications are rarely unprotected and rely heavily on layered security controls.

---

## Screenshots (Proof of Practice)

### wafw00f Scan on Paytm.com & Amazon.com

<img width="1920" height="1080" alt="Screenshot_2026-01-13_06_00_42" src="https://github.com/user-attachments/assets/efa070e8-d2eb-4ca9-95e2-52c821b1085c" />


*(Screenshots captured from my Kali Linux terminal)*

---

## Key Learnings

* How to identify WAF protection during reconnaissance
* How WAFs influence attack surface visibility
* Importance of respecting scope and responsible testing
* Difference between attacking **with knowledge** vs blindly scanning

---

## Conclusion

Practicing with wafw00f gave me a clearer understanding of defensive web security mechanisms.
This exercise reinforced the importance of reconnaissance and adapting testing techniques based on the security controls in place.

I plan to further explore how WAFs respond to different types of payloads in a controlled and ethical environment.
