# CTF-Writeups
# 🚩 CTF Writeups & Security Research

Welcome to my cybersecurity repository dedicated to **Capture The Flag (CTF)** writeups, machine walkthroughs, and security research. Here I document step-by-step methodologies, vulnerability analysis, exploitation scripts, and technical remediation reports.

---

## 📊 Platform Statistics

| Platform      | Profile / Rank                                    | Solved Machines / Rooms |
| :------------ | :------------------------------------------------ | :---------------------- |
| **TryHackMe** | [@hcktst](https://tryhackme.com/p/hcktst)         | 2 Rooms                 |
| **HackMyVM**  | [@HckTest](https://hackmyvm.eu/public/?u=HckTest) | 17 VM                   |
| **Vulnyx**    | -                                                 | 2 VM                    |

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

| Machine / Room   | Difficulty | Topics / Attack Vector                                    |  Writeup   | Mitigations |
| :--------------- | :--------: | :-------------------------------------------------------- | :--------: | :---------: |
| **Mr ROBOT CTF** |   Medium   | wordpress, reverse-php, user-brute, pass-brute, BurpSuite | IN PROCESS | IN PROCESS  |
| Anonymous        |   Medium   | SMB, Samba, anonymous-ftp, bash-scripting                 | IN PROCESS | IN PROCESS  |


---

### 🖥️ HackMyVM

| Machine / Room  | Difficulty | Topics / Attack Vector                                                                      |                   Writeup                   |                     Mitigations                     |
| :-------------- | :--------: | :------------------------------------------------------------------------------------------ | :-----------------------------------------: | :-------------------------------------------------: |
| **Canto**       |    Easy    | WordPress, Fuzzing                                                                          | [Read Writeup](./HackMyVM/Canto/writeup.md) | [Read Mitigations](./HackMyVM/Canto/mitigations.md) |
| **BaseME**      |    Easy    | Base64, Password Cracking, Web Fuzzing                                                      |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Gift**        |    Easy    | Hydra, Password Cracking                                                                    |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Quick**       |    Easy    | —                                                                                           |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Animetronic** |    Easy    | Steganography, Fuzzing, Social Engineering, CUPP                                            |                 IN PROCESS                  |                     IN  PROCESS                     |
| **CoffeeShop**  |    Easy    | Fuzzing, Crontab, Virtual Host                                                              |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Medusa**      |    Easy    | Fuzzing, LFI, Log Poisoning, Virtual Host                                                   |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Longshao**    |    Easy    | Fuzzing, Scripting                                                                          |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Quick3**      |    Easy    | Fuzzing, Web Research, PHP, Credential Scattering, Hydra                                    |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Quick4**      |    Easy    | Fuzzing, Web Login, SQLmap, SQL Injection, File Upload Bypass, Burp Suite, Script Injection |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Helium**      |    Easy    | Fuzzing, Audio Steganography                                                                |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Alzheimer**   |    Easy    | Anonymous FTP, Fuzzing                                                                      |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Aria**        |   Easy++   | File Upload, MIME Bypass, Aria2c Vulnerability, Zero-Width Hidden, SSH Key Substitution     |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Art**         |    Easy    | URL Parameters, Steganography, Fuzzing, Config File Escalation                              |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Nebula**      |    Easy    | Fuzzing, Brute Force, Lateral Movement, PATH Hijacking                                      |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Liceo**       |    Easy    | Fuzzing, File Upload, PHP Reverse Shell                                                     |                 IN PROCESS                  |                     IN  PROCESS                     |
| **Encrypt**     |    Easy    | SSH, File Capabilities, SSLscan                                                             |                 IN PROCESS                  |                     IN  PROCESS                     |

---

### 🛡️ Vulnyx

| Machine / Room | Difficulty | Topics / Attack Vector                            |  Writeup   | Mitigations |
| :------------- | :--------: | :------------------------------------------------ | :--------: | :---------: |
| **Basic**      |    Easy    | Fuzz, Brute Force                                 | IN PROCESS | IN PROCESS  |
| **Hunter**     |    Easy    | File Upload, Beanshell, .htaccess, subdomain FUZZ | IN PROCESS | IN PROCESS  |

---

## 🛠️ Frequently Used Tools

- **Reconnaissance & Scanning:** `nmap`, `gobuster`, `ffuf`, `dirb`, `wfuzz`, `wpscan`
- **Exploitation & Web:** `Burp Suite`, `sqlmap`, `Metasploit`, `File upload`, `hydra`, `Samba`, `SMB client`
- **Reverse Engineering & Binary Exploitation:** `reverse shell`, `msfvenom`
- **Privilege Escalation:** `linpeas.sh`

---

## ⚠️ Legal Disclaimer

All writeups, code snippets, and remediation reports in this repository are published exclusively for **educational purposes and authorized security research**. All tests were conducted in controlled environments and authorized lab platforms. Never use these techniques on systems without explicit authorization.
