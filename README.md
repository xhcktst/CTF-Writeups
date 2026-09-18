# CTF-Writeups
# 🚩 CTF Writeups & Security Research

Welcome to my cybersecurity repository dedicated to **Capture The Flag (CTF)** writeups, machine walkthroughs, and security research. Here I document step-by-step methodologies, vulnerability analysis, exploitation scripts, and technical remediation reports.

---

## 📊 Platform Statistics

| Platform | Profile / Rank | Solved Machines / Rooms |
| :--- | :--- | :--- |
| **TryHackMe** | [@hcktst](https://tryhackme.com/p/hcktst) | 2 Rooms |
| **HackMyVM** | [@HckTest](https://hackmyvm.eu/public/?u=HckTest) | 17 VM |
| **Vulnyx** | | 2 VM |

---

## 📊 Writeup Structure

Each machine folder contains two core documents:
- **`README.md` (Writeup):** Step-by-step walkthrough detailing initial access, exploitation, and privilege escalation.
- **`MITIGATIONS.md` (Mitigations Report):** Hardening recommendations and technical fixes for the identified vulnerabilities.

| Document Type | Description |
| :--- | :--- |
| **Writeup (`README.md`)** | Detailed technical analysis and exploitation flow |
| **Mitigations (`MITIGATIONS.md`)** | Security recommendations and remediation steps |

---

## 🗂️ Writeups Index

### 🦈 TryHackMe

| Machine / Room | Difficulty | Topics / Attack Vector | Writeup | Mitigations |
| :--- | :---: | :--- | :---: | :---: |
| **Mr ROBOT CTF** |Medium| wordpress, reverse-php, user-brute, pass-brute, BurpSuite | [Read Writeup](./Vulnyx/MrRobot/writeup.md) | [Read Mitigations](./HackMyVM/MrRobot/mitigations.md) |
| **Anonymous** |Medium| SMB, Samba, anonymous-ftp, bash-scripting | [Read Writeup](./Vulnyx/Anonymous/writeup.md) | [Read Mitigations](./HackMyVM/Anonymous/mitigations.md) |

---

### 🖥️ HackMyVM

| Machine / Room | Difficulty | Topics / Attack Vector | Writeup | Mitigations |
| :--- | :---: | :--- | :---: | :---: |
| **Canto** | Easy | WordPress, Fuzzing | [Read Writeup](./HackMyVm/Canto/writeup.md) | [Read Mitigations](./HackMyVm/Canto/mitigations.md) |
| **BaseME** | Easy | Base64, Password Cracking, Web Fuzzing | [Read Writeup](./HackMyVm/BaseME/writeup.md) | [Read Mitigations](./HackMyVm/BaseME/mitigations.md) |
| **Gift** | Easy | Hydra, Password Cracking | [Read Writeup](./HackMyVm/Gift/writeup.md) | [Read Mitigations](./HackMyVm/Gift/mitigations.md) |
| **Quick** | Easy | — | [Read Writeup](./HackMyVm/Quick/writeup.md) | [Read Mitigations](./HackMyVm/Quick/mitigations.md) |
| **Animetronic** | Easy | Steganography, Fuzzing, Social Engineering, CUPP | [Read Writeup](./HackMyVm/Animetronic/writeup.md) | [Read Mitigations](./HackMyVm/Animetronic/mitigations.md) |
| **CoffeeShop** | Easy | Fuzzing, Crontab, Virtual Host | [Read Writeup](./HackMyVm/CoffeeShop/writeup.md) | [Read Mitigations](./HackMyVm/CoffeeShop/mitigations.md) |
| **Medusa** | Easy | Fuzzing, LFI, Log Poisoning, Virtual Host | [Read Writeup](./HackMyVm/Medusa/writeup.md) | [Read Mitigations](./HackMyVm/Medusa/mitigations.md) |
| **Longshao** | Easy | Fuzzing, Scripting | [Read Writeup](./HackMyVm/Longshao/writeup.md) | [Read Mitigations](./HackMyVm/Longshao/mitigations.md) |
| **Quick3** | Easy | Fuzzing, Web Research, PHP, Credential Scattering, Hydra | [Read Writeup](./HackMyVm/Quick3/writeup.md) | [Read Mitigations](./HackMyVm/Quick3/mitigations.md) |
| **Quick4** | Easy | Fuzzing, Web Login, SQLmap, SQL Injection, File Upload Bypass, Burp Suite, Script Injection | [Read Writeup](./HackMyVm/Quick4/writeup.md) | [Read Mitigations](./HackMyVm/Quick4/mitigations.md) |
| **Helium** | Easy | Fuzzing, Audio Steganography | [Read Writeup](./HackMyVm/Helium/writeup.md) | [Read Mitigations](./HackMyVm/Helium/mitigations.md) |
| **Alzheimer** | Easy | Anonymous FTP, Fuzzing | [Read Writeup](./HackMyVm/Alzheimer/writeup.md) | [Read Mitigations](./HackMyVm/Alzheimer/mitigations.md) |
| **Aria** | Easy++ | File Upload, MIME Bypass, Aria2c Vulnerability, Zero-Width Hidden, SSH Key Substitution | [Read Writeup](./HackMyVm/Aria/writeup.md) | [Read Mitigations](./HackMyVm/Aria/mitigations.md) |
| **Art** | Easy | URL Parameters, Steganography, Fuzzing, Config File Escalation | [Read Writeup](./HackMyVm/Art/writeup.md) | [Read Mitigations](./HackMyVm/Art/mitigations.md) |
| **Nebula** | Easy | Fuzzing, Brute Force, Lateral Movement, PATH Hijacking | [Read Writeup](./HackMyVm/Nebula/writeup.md) | [Read Mitigations](./HackMyVm/Nebula/mitigations.md) |
| **Liceo** | Easy | Fuzzing, File Upload, PHP Reverse Shell | [Read Writeup](./HackMyVm/Liceo/writeup.md) | [Read Mitigations](./HackMyVm/Liceo/mitigations.md) |
| **Encrypt** | Easy | SSH, File Capabilities, SSLscan | [Read Writeup](./HackMyVm/Encrypt/writeup.md) | [Read Mitigations](./HackMyVm/Encrypt/mitigations.md) |

---

### 🛡️ Vulnyx

| Machine / Room | Difficulty | Topics / Attack Vector | Writeup | Mitigations |
| :--- | :---: | :--- | :---: | :---: |
| **Basic** |Easy| Fuzz, Brute Force | [Read Writeup](./Vulnyx/Basic/writeup.md) | [Read Mitigations](./HackMyVM/Basic/mitigations.md) |
| **Hunter** |Easy|  File Upload, Beanshell, .htaccess, subdomain FUZZ| [Read Writeup](./Vulnyx/Hunter/writeup.md) | [Read Mitigations](./HackMyVM/Easy/Hunter/mitigations.md) |

---

## 🛠️ Frequently Used Tools

- **Reconnaissance & Scanning:** `nmap`, `gobuster`, `ffuf`, `dirb`, `wfuzz`, `wpscan`
- **Exploitation & Web:** `Burp Suite`, `sqlmap`, `Metasploit`, `File upload`, `hydra`, `Samba`, `SMB client`
- **Reverse Engineering & Binary Exploitation:** `reverse shell`, `msfvenom`
- **Privilege Escalation:** `linpeas.sh`

---

## ⚠️ Legal Disclaimer

All writeups, code snippets, and remediation reports in this repository are published exclusively for **educational purposes and authorized security research**. All tests were conducted in controlled environments and authorized lab platforms. Never use these techniques on systems without explicit authorization.
