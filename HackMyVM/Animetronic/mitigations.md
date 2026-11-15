# Mitigations 🔐

> **Disclaimer:** While reviewing this mitigation plan, keep in mind that these are preventive actions designed for a vulnerable lab environment whose design is unlikely to be encountered in a real-world operational environment.

That said, for this specific scenario, several key configuration fixes would have prevented this attack:
### 1) Public exposure of sensitive information on the web server 💾
The main weakness that allowed the attack was the availability of sensitive information in the web server. Specifically, after researching we were able to obtain all personal information from a current user: `michael`

```txt
name: Michael
age: 27
birth date: 19/10/1996
number of children: 3 (" Ahmed - Yasser - Adam ")
Hobbies: swimming
```

Discovering this information increased the attack surface by enabling some more options to attacker:

- Impersonation (social engineering)
- Further research and online background
- Bruteforce attacks

We are in a simulated lab, so no all the options are available in this case but the bruteforce attack. 

> **Note**: The disclosure of this information does not immediatelly means we can obtain a password/credentials in all scenarios. It also requires another "vulnerability" which is the use of weak passwords or easy to guess passwords which is what allowed as to gain access in this 
> scenario as we point out in section 2 of this page.

**Recommendation:** Remove all sensitive files/information and backups from the web root immediately. If file transfer is necessary, use specific tools for this purpose. For example, upload the file via SSH to a folder where only the users in the organization that requires such information has access.

### 2) Weak password and plain-text password storing 👁️
We successfully obtained credentials using a brute-force tool and a custom wordlist made from the users information.

Using weak or predictable passwords undermines password-based authentication security, as tools such as hydra can systematically test thousands of passwords.

In this laboratory, the user henry left the password accesible in case anyone needs to do something on the server. This is critical, because compromising michael's credentials immediately compromises henry's.

**Recommendation:** Enforce a strong password and password policy across the organization. Passwords should be long, complex, unique and avoid using any personal information. Employing an enterprise password manager helps users generate, store, and manage strong credentials securely while enforcing periodic rotation policies.

Additionally, plain-text password storing should be restricted, so no one can get access to a content they should not. In this scenario, if any user needs to do something on the web server a correct application of permissions should work fine. One possible solution is to define a group for working on web server and assign users to that group in order to give access and permissions to work. To learn more on how to set groups on Linux, visit this [page](https://wiki.archlinux.org/title/Users_and_groups)
### 3) Excessive Sudo permissions 👮‍♂️
We escalated privileges to `root` due to a misconfigured sudo entry containing the `NOPASSWD` directive. User `henry` was permitted to run `/usr/bin/socat` as `root` without providing credentials, allowing us to run commands as root and escalate the privilege.

**Recommendation:**
1. **Primary fix (Principle of Least Privilege):** Remove unnecessary binaries and users from the `/etc/sudoers` configuration. Standard users should not be granted `sudo` access to binaries like `socat` that allow arbitrary command execution or shell spawning.
2. **Alternative lab-specific fix:** If `henry` strictly requires execution rights for `socat` as `root`, remove `NOPASSWD` and enforce password authentication. In this scenario, configuring `Defaults rootpw` forces `sudo` to prompt for the root password, preventing an attacker who only possesses henry's account credentials from abusing the binary. To learn how to do this, visit the mitigation actions from lab "Canto" [here.](https://github.com/xhcktst/CTF-Writeups/blob/main/HackMyVM/Canto/mitigations.md)