# CTF-Writeups
# 🚩 CTF Writeups & Security Research

Welcome to my cybersecurity repository dedicated to **Capture The Flag (CTF)** writeups, machine walkthroughs, and security research. Here I document step-by-step methodologies, vulnerability analysis, exploitation scripts, and technical remediation reports.

---

## 📊 Platform Statistics

| Platform | Profile / Rank | Solved Machines / Rooms |
| :--- | :--- | :--- |
| **TryHackMe** | [@hcktst](https://tryhackme.com/p/hcktst) | X Rooms |
| **HackMyVM** | [@HckTest](https://hackmyvm.eu/public/?u=HckTest) | X |
| **Vulnyx** | | X |

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

| Room Name | Difficulty | Main Categories | Writeup | Mitigations |
| :--- | :---: | :--- | :---: | :---: |
| **OWASP Top 10** | Easy | Web, SQLi, XSS, Command Injection | [Read Writeup](./TryHackMe/Web/OWASP_Top_10) | [Read Mitigations](./TryHackMe/Web/OWASP_Top_10/MITIGATIONS.md) |

---

### 🖥️ HackMyVM

| Machine | Operating System | Difficulty | Topics / Attack Vector | Writeup | Mitigations |
| :--- | :---: | :---: | :--- | :---: | :---: |
| **MachineName** | 🐧 Linux | Easy | Web, SUID binaries, Capabilities | [Read Writeup](./HackMyVM/Easy/MachineName) | [Read Mitigations](./HackMyVM/Easy/MachineName/MITIGATIONS.md) |
| **AnotherVM** | 🐧 Linux | Medium | WordPress, LFI, Cronjobs | [Read Writeup](./HackMyVM/Medium/AnotherVM) | [Read Mitigations](./HackMyVM/Medium/AnotherVM/MITIGATIONS.md) |

---

### 🛡️ Vulnyx

| Machine | Operating System | Difficulty | Topics / Attack Vector | Writeup | Mitigations |
| :--- | :---: | :---: | :--- | :---: | :---: |
| **ExampleVM** | 🐧 Linux | Easy | SQLi, Sudoers Abuse | [Read Writeup](./Vulnyx/Easy/ExampleVM) | [Read Mitigations](./Vulnyx/Easy/ExampleVM/MITIGATIONS.md) |

---

## 🛠️ Frequently Used Tools

- **Reconnaissance & Scanning:** `nmap`, `gobuster`, `ffuf`, `dirb`, `wfuzz`, `wpscan`
- **Exploitation & Web:** `Burp Suite`, `sqlmap`, `Metasploit`, `File upload`, `hydra`
- **Reverse Engineering & Binary Exploitation:** TO COMPLETE!!!
- **Privilege Escalation:** `linpeas.sh`

---

## ⚠️ Legal Disclaimer

All writeups, code snippets, and remediation reports in this repository are published exclusively for **educational purposes and authorized security research**. All tests were conducted in controlled environments and authorized lab platforms. Never use these techniques on systems without explicit authorization.
