# 🔐 Password Security Guidelines

A practical guide for creating, storing, managing, and protecting passwords across **personal accounts, servers, applications, devices, and network infrastructure**.

> **Goal:** Prevent unauthorized access caused by weak passwords, password reuse, credential theft, phishing, brute-force attacks, credential stuffing, and leaked credentials.

---

## 📋 Table of Contents

* [1. Strong Passwords](#1--strong-passwords)
* [2. Password Length](#2--password-length)
* [3. Strong Password Examples](#3--strong-password-examples)
* [4. Password Uniqueness](#4--password-uniqueness)
* [5. Passphrases](#5--passphrases)
* [6. Password Managers](#6--password-managers)
* [7. Multi-Factor Authentication](#7--multi-factor-authentication)
* [8. Passkeys](#8--passkeys)
* [9. Recovery Codes](#9--recovery-codes)
* [10. Administrative Passwords](#10--administrative-passwords)
* [11. Server & SSH Passwords](#11--server--ssh-passwords)
* [12. Wi-Fi Passwords](#12--wi-fi-passwords)
* [13. Password Storage](#13--password-storage)
* [14. Password Sharing](#14--password-sharing)
* [15. Password Changes](#15--password-changes)
* [16. Leaked Passwords](#16--leaked-passwords)
* [17. Protection Against Phishing](#17--protection-against-phishing)
* [18. Account Lockout & Rate Limiting](#18--account-lockout--rate-limiting)
* [19. Backup & Recovery](#19--backup--recovery)
* [20. Recommended Password Policy](#20--recommended-password-policy)
* [21. Security Checklist](#21--security-checklist)
* [22. Golden Rules](#22--golden-rules)

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

---

# 3. 🔐 Strong Password Examples

The following are examples of **strong password formats**.

> ⚠️ **Important:** These passwords are examples only. Do not use the exact passwords below for real accounts because they are publicly documented.

### Random complex passwords

```text
v7!Qm2#Lp9@Tx4$Nz8&Kr5
G4@xP9!rL2#Vm7$Qz8^Nt6
R8#kT4!wP7@Lm2$Xq9&Vc5
mQ7$Zp3!Kx9@Hr5#Tw8&Ln2
Y5@vN8#qR2!Km7$Xp4^Ld9
```

### Longer random passwords

```text
F7@qL2#vN9!xR4$kT8%pM6&zC3
W9!rK4@xP7#nL2$V8^qT5&hM6
aR8#Lm3!Qv7@Xp2$K9&Nt5%Z4
```

### High-entropy style

```text
7x!Q9@Lm#2Vr$8Tp%4Nz&6Kp
@9Fq#7Lm2!Rx$8Vt4%Np6&Zk
3$Kx!9Qv@7Lm#2Rt8^Np4&Yz
```

These examples demonstrate a combination of:

```text
Uppercase letters
Lowercase letters
Numbers
Special characters
Long length
Randomness
```

However, **randomness and uniqueness are more important than simply adding many special characters**.

---

## 🎲 Best Practice: Generate Passwords Automatically

Instead of manually creating passwords, use a password manager or a cryptographically secure password generator.

For example:

```text
Length:        32 characters
Uppercase:     Enabled
Lowercase:     Enabled
Numbers:       Enabled
Symbols:       Enabled
Randomness:    Cryptographically secure
```

Example output:

```text
N7@xQ2!vL9#rT4$kP8&mZ5^wC3
```

Another example:

```text
pR8$2v!Kq7@Lm4#Xz9&Tn6%Fw
```

Again, these are **demonstration examples only**.

---

# 🧠 Memorable Strong Passwords

If a password must be memorized, use a long passphrase rather than a short complicated password.

Examples:

```text
River-Coffee-Mountain-Window-Planet
```

```text
Silver!Forest!Rocket!Candle!Ocean
```

```text
Purple-Harbor-7-Cloud-Morning-Train
```

Long random passphrases can be significantly easier to remember than strings of random characters.

However, for most accounts, a password manager can generate and store a completely random password.

---

# 🏆 Recommended Password Examples by Use Case

### 👤 Normal Account

```text
v7!Qm2#Lp9@Tx4$Nz8&Kr5
```

### 📧 Email Account

```text
F7@qL2#vN9!xR4$kT8%pM6&zC3
```

### 🛡️ Administrator Account

```text
W9!rK4@xP7#nL2$V8^qT5&hM6
```

### 📡 Wi-Fi

```text
Silver-River-84!Mountain-Cloud
```

### 🖥️ Server

```text
aR8#Lm3!Qv7@Xp2$K9&Nt5%Z4
```

### 🔐 Password Manager Master Password

Prefer a long unique passphrase:

```text
River-Moon-Glass-Orange-Planet-47
```

For a password manager master password, prioritize **length, memorability, and uniqueness**.

---

# ❌ Weak vs Strong

| Weak          | Strong                       |
| ------------- | ---------------------------- |
| `password123` | `v7!Qm2#Lp9@Tx4$Nz8&Kr5`     |
| `Admin123!`   | `F7@qL2#vN9!xR4$kT8%pM6&zC3` |
| `Qwerty2026!` | `W9!rK4@xP7#nL2$V8^qT5&hM6`  |
| `MyPassword!` | `aR8#Lm3!Qv7@Xp2$K9&Nt5%Z4`  |
| `Summer2026!` | `N7@xQ2!vL9#rT4$kP8&mZ5^wC3` |
| `Company@123` | `3$Kx!9Qv@7Lm#2Rt8^Np4&Yz`   |

---

# ⚠️ Do Not Make Passwords Predictable

Avoid patterns such as:

```text
Password1!
Password2!
Password3!
```

or:

```text
Summer2026!
Summer2027!
Summer2028!
```

or:

```text
Admin@123
Admin@1234
Admin@12345
```

Changing only one or two characters does not create a truly independent password.

---

# 4. ♻️ Password Uniqueness

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

Every important account should have its own credential.

---

# 5. 🧠 Passphrases

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

---

# 6. 🔐 Password Managers

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

The password manager's master password is extremely important.

Protect it with:

* A long unique passphrase
* MFA where available
* Strong device security
* Secure recovery methods

---

# 7. 🛡️ Multi-Factor Authentication

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

Enable MFA first on:

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

# 8. 🔐 Passkeys

Where supported, consider using **passkeys** instead of traditional passwords.

Passkeys use public-key cryptography and are designed to resist many forms of phishing.

---

# 9. 🧾 Recovery Codes

When enabling MFA, many services provide recovery codes.

Treat recovery codes like highly sensitive credentials.

Never store recovery codes in:

```text
Public GitHub repositories
Public cloud documents
Chat messages
Screenshots
Social media
Unencrypted notes
```

---

# 10. 👑 Administrative Passwords

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

Avoid using administrator accounts for everyday activities.

---

# 11. 🖥️ Server & SSH Passwords

For Linux and Unix servers, prefer **SSH keys** over password authentication.

Recommended key type:

```text
Ed25519
```

Example:

```bash
ssh-keygen -t ed25519
```

After confirming key-based authentication works, consider disabling SSH password authentication.

---

# 12. 📡 Wi-Fi Passwords

Wi-Fi passwords should be unique and sufficiently long.

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

Do not reuse your Wi-Fi password for other services.

---

# 13. 💾 Password Storage

Never store passwords in public repositories or plain-text files unnecessarily.

Never put credentials directly into:

```text
GitHub
GitLab
Public repositories
README files
Screenshots
Public documentation
```

For applications, use:

```text
Environment variables
Secret managers
Encrypted configuration
Vault systems
OS credential stores
```

---

# 14. 🤝 Password Sharing

Do not send passwords through insecure channels.

Avoid:

```text
Public chats
Social media
Public email threads
GitHub issues
Forums
Screenshots
Public documents
```

If credentials must be shared, use an approved secure password-sharing mechanism and rotate the credential afterward when appropriate.

---

# 15. 🔄 Password Changes

Do not rely on arbitrary periodic password changes as your primary security strategy.

Change a password when:

* It has been exposed.
* A service reports a breach.
* You suspect unauthorized access.
* Someone who knew the password should no longer have access.
* The password was reused elsewhere.

---

# 16. 🚨 Leaked Passwords

If you discover that a password has been leaked:

```text
1. Change the password.
2. Change it everywhere it was reused.
3. Enable MFA.
4. Review active sessions.
5. Revoke unknown sessions.
6. Check account recovery settings.
7. Review recent account activity.
```

Treat reused credentials as potentially compromised across all affected services.

---

# 17. 🎣 Protection Against Phishing

A strong password does not protect you if you voluntarily provide it to an attacker.

Before entering credentials:

```text
Check the domain
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
* Look-alike domains
* Messages asking for verification codes

Never provide your:

```text
Password
MFA code
Recovery code
Private key
Password manager master password
```

to someone who contacts you unexpectedly.

---

# 18. 🚦 Account Lockout & Rate Limiting

For systems you administer, protect authentication endpoints against automated attacks.

Consider:

```text
Rate limiting
Login throttling
Account lockout
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

---

# 19. 💾 Backup & Recovery

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

---

# 20. 🛡️ Recommended Password Policy

```text
Minimum password length     → 16 characters
High-value accounts         → 20+ characters
Generated passwords         → 20–32+ characters
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

# 21. 📝 Security Checklist

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

# 22. 🔥 Golden Rules

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

## 🔒 Security Model

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
