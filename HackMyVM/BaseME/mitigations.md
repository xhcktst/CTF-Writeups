# Mitigations 🔐

> **Note:** While reviewing this mitigation plan, keep in mind that these are preventive actions designed for a vulnerable lab environment whose design is very unlikely to be encountered in a real-world operational environment.

That said, for this specific scenario, several key configuration fixes would have prevented this attack:
### 1) Public exposure of sensitive files on the web server 💾
We gained initial access because an SSH private key was accessible via the web server. The file paths and contents were Base64-encoded; however, **Base64 is an encoding format, not an encryption method**, and offers no security or confidentiality. Anyone can trivially detect and decode Base64 data.

Private SSH keys and sensitive configuration files should **never** be placed inside a web-accessible directory. While the key was protected by a passphrase (requiring offline cracking), storing private keys on a public web server represents a critical security risk.

**Recommendation:** Remove all private keys and sensitive backup files from the web root immediately. Restrict access so that private SSH keys are stored exclusively in user home directories (`~/.ssh/id_rsa`) with strict file permissions (`chmod 600`), accessible only by their respective owners or root.

### 2) Weak SSH key passphrases 👁️
We successfully cracked the SSH key passphrase for user `lucas` using a standard wordlist (`rockyou.txt`) combined with Base64 transformation. 

Using weak or predictable passphrases undermines key-based authentication, as offline brute-force tools (such as John the Ripper) can test thousands of combinations per second without triggering network lockout controls.

**Recommendation:** Enforce a strong password and passphrase policy across the organization. Passphrases for SSH keys should be long, complex, and unique. Employing an enterprise password manager helps users generate, store, and manage strong credentials securely while enforcing periodic rotation policies.

### 3) Excessive Sudo permissions 👮‍♂️
We escalated privileges to `root` due to a misconfigured sudo entry containing the `NOPASSWD` directive. User `lucas` was permitted to run `/usr/bin/base64` as `root` without providing credentials, allowing us to read arbitrary root-owned files (specifically `/root/.ssh/id_rsa`) and obtain a root shell.

**Recommendation:**
1. **Primary fix (Principle of Least Privilege):** Remove unnecessary binaries and users from the `/etc/sudoers` configuration. Standard users should not be granted `sudo` access to binaries like `base64` that allow arbitrary file reading.
2. **Alternative lab-specific fix:** If `lucas` strictly requires execution rights for `base64` as `root`, remove `NOPASSWD` and enforce password authentication. In this scenario, configuring `Defaults rootpw` forces `sudo` to prompt for the root password, preventing an attacker who only possesses Lucas's account credentials from abusing the binary. To learn how to do this, visit the mitigation actions from lab "Canto" [here.](https://github.com/xhcktst/CTF-Writeups/blob/main/HackMyVM/Canto/mitigations.md)