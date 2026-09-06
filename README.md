# 🔐 Password Security Guidelines

A practical guide for creating, storing, managing, and protecting passwords across **personal accounts, servers, applications, devices, and network infrastructure**.

> **Goal:** Prevent unauthorized access caused by weak passwords, password reuse, credential theft, phishing, brute-force attacks, credential stuffing, and leaked credentials.

---

## 📋 Table of Contents

* [1. Strong Passwords](#1--strong-passwords)
* [2. Password Length](#2--password-length)
* [3. Password Uniqueness](#3--password-uniqueness)
* [4. Passphrases](#4--passphrases)
* [5. Password Managers](#5--password-managers)
* [6. Multi-Factor Authentication](#6--multi-factor-authentication)
* [7. Passkeys](#7--passkeys)
* [8. Recovery Codes](#8--recovery-codes)
* [9. Administrative Passwords](#9--administrative-passwords)
* [10. Server & SSH Passwords](#10--server--ssh-passwords)
* [11. Wi-Fi Passwords](#11--wi-fi-passwords)
* [12. Password Storage](#12--password-storage)
* [13. Password Sharing](#13--password-sharing)
* [14. Password Changes](#14--password-changes)
* [15. Leaked Passwords](#15--leaked-passwords)
* [16. Protection Against Phishing](#16--protection-against-phishing)
* [17. Account Lockout & Rate Limiting](#17--account-lockout--rate-limiting)
* [18. Backup & Recovery](#18--backup--recovery)
* [19. Recommended Password Policy](#19--recommended-password-policy)
* [20. Security Checklist](#20--security-checklist)
* [21. Golden Rules](#21--golden-rules)

---

# 1. 🔑 Strong Passwords

Use long, unpredictable passwords that are difficult to guess or crack.

A strong password should:

* Be unique
* Be sufficiently long
* Not contain easily guessed personal information
* Not be based on common passwords
* Not be reused between services
* Not be shared with other people

Avoid passwords such as:

```text
password
12345678
qwerty
admin123
welcome
letmein
password123
```

Also avoid predictable variations:

```text
Password2026!
Password2027!
Password123!
Admin@123
Company2026!
```

Attackers routinely test these patterns.

---

# 2. 📏 Password Length

**Length is one of the most important password security properties.**

Recommended minimums:

| Password Type            |           Recommended |
| ------------------------ | --------------------: |
| Important online account |    **16+ characters** |
| High-value account       |    **20+ characters** |
| Passphrase               |    **20+ characters** |
| Wi-Fi password           | **16–20+ characters** |
| Admin password           |    **20+ characters** |
| Generated password       | **20–32+ characters** |

When a password manager is available, prefer a randomly generated password rather than creating one manually.

Example:

```text
v7!Qm2#Lp9@Tx4$Nz8&Kr5
```

---

# 3. ♻️ Password Uniqueness

**Never reuse passwords between important services.**

If one website is compromised and your password is reused elsewhere, attackers may try the same credentials against:

```text
Email
Cloud storage
Social media
Banking
VPN
GitHub
Servers
Routers
Work accounts
```

### Recommended

```text
Google       → Password A
GitHub       → Password B
Cloud        → Password C
Router       → Password D
Email        → Password E
```

Every important account should have its own credential.

---

# 4. 🧠 Passphrases

A passphrase can be easier to remember while still providing substantial length.

Example:

```text
River-Moon-Coffee-Window-Planet
```

A stronger randomly generated passphrase could look like:

```text
correct-harbor-seven-lamp-canyon-orbit
```

Avoid using famous quotations, song lyrics, movie phrases, or common sentences.

Do not assume that adding a number or `!` to a common phrase makes it secure.

---

# 5. 🔐 Password Managers

Use a reputable **password manager** to generate and store unique passwords.

A password manager can provide:

* Random password generation
* Secure password storage
* Autofill
* Password auditing
* Breach monitoring
* Secure notes
* Passkey support
* Cross-device synchronization

### Recommended model

```text
                MASTER PASSWORD
                       │
                       ▼
               ┌──────────────┐
               │   PASSWORD   │
               │    MANAGER   │
               └──────┬───────┘
                      │
        ┌─────────────┼─────────────┐
        ▼             ▼             ▼
      Email         GitHub        Cloud
      Random        Random        Random
     Password      Password      Password
```

The password manager's master password is extremely important.

Protect it with:

* A long unique passphrase
* MFA where available
* Strong device security
* Secure recovery methods

---

# 6. 🛡️ Multi-Factor Authentication

Passwords alone are not always enough.

Enable **MFA (Multi-Factor Authentication)** on important accounts.

Recommended priority:

```text
1. Passkey / hardware security key
2. Authenticator app
3. TOTP
4. Push authentication
5. SMS
```

SMS-based authentication is generally weaker than phishing-resistant methods, but it can still be better than password-only authentication when stronger options are unavailable.

### Enable MFA first on:

* Primary email
* Password manager
* Cloud accounts
* GitHub / GitLab
* Financial accounts
* VPN
* Server administration
* Domain registrar
* Social media
* Work accounts

---

# 7. 🔐 Passkeys

Where supported, consider using **passkeys** instead of traditional passwords.

Passkeys use public-key cryptography and are designed to resist many forms of phishing.

Typical model:

```text
Device
   │
   ├── Biometric
   ├── PIN
   └── Device Authentication
             │
             ▼
          Passkey
             │
             ▼
           Account
```

Never share or export private authentication credentials unnecessarily.

---

# 8. 🧾 Recovery Codes

When enabling MFA, many services provide recovery codes.

Treat recovery codes like highly sensitive credentials.

### Recommended

```text
Generate recovery codes
        ↓
Store securely
        ↓
Keep an offline backup
        ↓
Do not publish or share them
```

Do not store recovery codes in:

```text
Public GitHub repositories
Public cloud documents
Chat messages
Screenshots
Social media
Unencrypted notes
```

---

# 9. 👑 Administrative Passwords

Administrative accounts require additional protection.

Examples:

```text
Router admin
Linux root
Windows Administrator
Database admin
Cloud administrator
Domain administrator
Server management
```

Use a dedicated credential.

Do not use:

```text
admin / admin
root / root
administrator / password
```

### Principle

```text
Normal Account
      │
      ▼
Daily Work

Admin Account
      │
      ▼
Administrative Tasks
```

Avoid using administrator accounts for everyday browsing, email, and general activities.

---

# 10. 🖥️ Server & SSH Passwords

For Linux and Unix servers, prefer **SSH keys** over password authentication.

Recommended architecture:

```text
Client
  │
  │ SSH Key
  ▼
Server
```

Use:

```text
Ed25519
```

where supported.

Example:

```bash
ssh-keygen -t ed25519
```

After confirming key-based authentication works, consider disabling SSH password authentication:

```text
PasswordAuthentication no
```

Do not disable password authentication until you have verified that your SSH key login works.

---

# 11. 📡 Wi-Fi Passwords

Wi-Fi passwords should also be unique and sufficiently long.

Recommended:

```text
WPA3-Personal
+
Strong unique password
+
WPS disabled
```

Example:

```text
Silver-River-Cloud-84!Mountain
```

Do not reuse your Wi-Fi password for:

```text
Email
GitHub
Router administration
Cloud accounts
VPN
SSH
```

Your router administrator password should always be different from your Wi-Fi password.

---

# 12. 💾 Password Storage

Never store passwords in plain-text files unless there is a specific, controlled technical requirement and appropriate protection.

Avoid:

```text
passwords.txt
credentials.txt
notes.txt
desktop.txt
```

Also avoid committing credentials to Git repositories.

Never put secrets directly into:

```text
GitHub
GitLab
Public repositories
README files
Screenshots
Public documentation
```

### For applications

Use:

```text
Environment variables
Secret managers
Encrypted configuration
Vault systems
OS credential stores
```

---

# 13. 🤝 Password Sharing

Do not send passwords through insecure channels.

Avoid sending credentials through:

```text
Public chats
Social media
Public email threads
GitHub issues
Forums
Screenshots
Public documents
```

If credentials must be shared:

* Use an approved secure password-sharing mechanism.
* Share the minimum necessary information.
* Change the password after temporary access is no longer required.
* Revoke access when the task is complete.

---

# 14. 🔄 Password Changes

Do **not** rely on arbitrary periodic password changes as your primary security strategy.

Instead, change a password when:

* It has been exposed.
* A service reports a breach.
* You suspect unauthorized access.
* Someone who knew the password should no longer have access.
* The password was reused elsewhere.
* The account's security requirements change.

For important accounts, use unique passwords from the beginning.

---

# 15. 🚨 Leaked Passwords

If you discover that a password has been leaked:

### Immediately

```text
1. Change the password.
2. Change it everywhere it was reused.
3. Enable MFA.
4. Review active sessions.
5. Revoke unknown sessions.
6. Check account recovery settings.
7. Review recent account activity.
```

If the leaked password was reused on multiple services, treat **all of those accounts as potentially compromised**.

---

# 16. 🎣 Protection Against Phishing

A strong password does not protect you if you voluntarily provide it to an attacker.

Before entering credentials:

```text
Check the domain
        ↓
Check HTTPS
        ↓
Check the website
        ↓
Check the login context
        ↓
Authenticate
```

Be suspicious of:

* Urgent password-reset messages
* Fake login pages
* Unexpected MFA requests
* Suspicious attachments
* Shortened URLs
* Look-alike domains
* Messages asking for verification codes

### Never provide

```text
Password
MFA code
Recovery code
Private key
Password manager master password
```

to someone who contacts you unexpectedly.

---

# 17. 🚦 Account Lockout & Rate Limiting

For systems you administer, protect authentication endpoints against automated attacks.

Consider:

```text
Rate limiting
Login throttling
Account lockout
CAPTCHA where appropriate
MFA
IP reputation controls
Fail2ban
```

For SSH servers, consider restricting access through:

```text
Firewall
VPN
Allowlisted IPs
Private network
```

rather than relying only on password protection.

---

# 18. 💾 Backup & Recovery

Security also requires reliable recovery.

Keep secure backups of:

```text
Password manager data
Recovery codes
Important configuration
SSH keys
Encryption keys
Router configuration
Server configuration
```

Backups should be:

* Encrypted
* Access-controlled
* Tested periodically
* Stored separately from the primary system

### Example

```text
Primary Password Manager
          │
          ├──────────────► Encrypted Backup
          │
          └──────────────► Offline Backup
```

A backup that has never been tested should not be considered reliable.

---

# 19. 🛡️ Recommended Password Policy

A strong general-purpose policy:

```text
Minimum password length     → 16 characters
High-value accounts         → 20+ characters
Unique passwords             → Required
Password manager             → Recommended
MFA                          → Enabled
Passkeys                     → Preferred where supported
Recovery codes               → Securely stored
Password reuse               → Prohibited
Default passwords            → Prohibited
Public credential storage    → Prohibited
Plain-text credential files  → Avoid
```

---

# 20. 📝 Security Checklist

### Passwords

* [ ] Passwords are unique
* [ ] Important passwords are 16+ characters
* [ ] High-value passwords are 20+ characters
* [ ] Passwords are randomly generated where possible
* [ ] Common passwords are avoided
* [ ] Personal information is not used
* [ ] Password reuse is avoided

### Authentication

* [ ] MFA enabled
* [ ] Passkeys enabled where available
* [ ] Hardware security keys considered for critical accounts
* [ ] Recovery codes securely stored
* [ ] Old sessions periodically reviewed

### Password Manager

* [ ] Password manager is used
* [ ] Master password is unique
* [ ] Master password is strong
* [ ] MFA enabled
* [ ] Secure backup configured
* [ ] Recovery process tested

### Servers

* [ ] SSH keys used
* [ ] Ed25519 preferred
* [ ] SSH password authentication restricted where appropriate
* [ ] Root login restricted
* [ ] Firewall configured
* [ ] Authentication attempts monitored

### Secrets

* [ ] Credentials are not stored in Git
* [ ] API keys are not published
* [ ] Tokens are not included in documentation
* [ ] `.env` files are excluded from repositories
* [ ] Secret management is used for applications
* [ ] Exposed credentials are revoked immediately

---

# 21. 🔥 Golden Rules

> **1. Use a different password for every important account.**

> **2. Prefer long passwords over complicated but short passwords.**

> **3. Use a password manager.**

> **4. Enable MFA on important accounts.**

> **5. Prefer passkeys or hardware security keys where available.**

> **6. Never store passwords in public repositories.**

> **7. Never share passwords or MFA codes with unexpected contacts.**

> **8. Change compromised passwords immediately.**

> **9. Never use default administrator credentials.**

> **10. Protect your password manager master password especially carefully.**

> **11. Keep recovery codes secure and offline when practical.**

> **12. Use SSH keys instead of passwords for server administration where possible.**

---

# 🔒 Security Model

A strong authentication setup should look like:

```text
                 ┌──────────────────┐
                 │   USER / DEVICE  │
                 └────────┬─────────┘
                          │
                    Passkey / MFA
                          │
                          ▼
                 ┌──────────────────┐
                 │     ACCOUNT      │
                 └────────┬─────────┘
                          │
                   Unique Password
                          │
                          ▼
                 ┌──────────────────┐
                 │ Password Manager │
                 └────────┬─────────┘
                          │
                  Encrypted Storage
                          │
                          ▼
                 Secure Backup / Recovery
```

### Core principle

```text
Unique Password
      +
Long Password
      +
Password Manager
      +
MFA / Passkey
      +
Secure Recovery
      +
Phishing Awareness
      =
Strong Authentication Security
```

---

## 📌 Final Recommendation

The best password is not necessarily the one you can memorize.

For most accounts, the ideal approach is:

```text
Password Manager
       +
Random Unique Password
       +
MFA / Passkey
       +
Secure Recovery Codes
       +
Device Security
```

For critical infrastructure:

```text
SSH Keys
   +
MFA
   +
VPN
   +
Firewall
   +
Least Privilege
   +
Monitoring
```

> **Your password is only one layer of security. Protect the account, the device, the recovery mechanisms, and the credentials themselves.**
