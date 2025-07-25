# Pyramid of Pain (Deep Dive)

##  What is the Pyramid of Pain?

The Pyramid of Pain is a concept created by David Bianco.  
It shows how difficult it is for an attacker when you detect and block different types of indicators used in cyber attacks.

The higher you go on the pyramid, the more it hurts the attacker.

---

##  The Levels (From Bottom to Top)

###  1. **Hash Values** (Easiest for attacker to change)
- Example: `d41d8cd98f00b204e9800998ecf8427e`
- This is like a digital fingerprint of a file.
- Attackers can easily change one bit and create a new hash.

** Blocking impact:** Low  
** Useful for:** Detecting exact known malware files.

---

### 2. **IP Addresses**
- Example: `123.45.67.89`
- Many attackers use dynamic or shared IPs.
- They can switch IPs very quickly.

** Blocking impact:** Low–Medium  
** Useful for:** Quick detection of known bad infrastructure.

---

### 3. **Domain Names**
- Example: `malicious-site.com`
- Attackers can register many domains, but it takes time and money.

** Blocking impact:** Medium  
** Useful for:** Catching phishing sites and C2 servers.

---

###  4. **Network/Host Artifacts**
- Example: A script in a specific folder or a unique file name.
- These are traces left by tools or malware behavior on the system.

** Blocking impact:** Medium–High  
** Useful for:** Finding infections or tool usage patterns.

---

###  5. **Tools**
- Example: Mimikatz, Powersploit
- Attackers use tools to move laterally, dump credentials, etc.
- You can detect tools by behavior or file signatures.

** Blocking impact:** High  
** Useful for:** Detecting threat actors using public or custom tools.

---

### 6. **Tactics, Techniques & Procedures (TTPs)**
- Example: Using PowerShell to bypass antivirus
- TTPs are *how* attackers operate, not just what they use.
- Very hard for them to change — it’s part of their style.

** Blocking impact:** Very High  
** Useful for:** Threat hunting and building strong defense.

---

##  Why it matters to a SOC Analyst

As a SOC Level 1 Analyst, your job often starts with detecting low-level indicators like IPs or hashes.  
But the real value comes from understanding higher levels — **tools and TTPs** — to stop future attacks.

**The goal is not just to block — it's to make the attacker's job painful.**

---

## TL;DR

| Level | Example | Impact on Attacker |
|-------|---------|--------------------|
| Hash | File fingerprint | Easy to change |
| IP | `192.168.1.1` | Easy to rotate |
| Domain | `evil.com` | Slower to change |
| Artifacts | Script path | Harder to hide |
| Tools | Mimikatz | Expensive to replace |
| TTPs | PowerShell obfuscation | Very hard to change |

---

## 📚 References
- David J. Bianco – [Original Pyramid of Pain Blog](https://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html)
- TryHackMe – "Pyramid of Pain" Room
- MITRE ATT&CK Framework – [https://attack.mitre.org](https://attack.mitre.org)

