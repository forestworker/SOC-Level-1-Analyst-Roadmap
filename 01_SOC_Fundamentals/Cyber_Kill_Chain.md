# Cyber Kill Chain

## Overview

The Cyber Kill Chain is a framework developed by Lockheed Martin to describe the stages of a cyber attack from initial planning to execution. The idea is that every attack progresses through a series of steps, and that defenders can detect and interrupt the attacker at any of these stages to stop or mitigate the attack.

The model consists of the following seven stages:

## 1. Reconnaissance

The attacker gathers information about the target. This may include scanning for open ports, finding employee email addresses, collecting data from social media, identifying public-facing systems, and more.

**Detection opportunities:**
- Web server logs
- DNS logs
- Threat intelligence
- Honeytokens

## 2. Weaponization

The attacker builds a malicious payload. This usually combines an exploit (to take advantage of a system vulnerability) and a backdoor or malware component.

**Note:** This step typically happens on the attacker’s side and is not directly observable by the defender.

## 3. Delivery

The attacker delivers the weaponized payload to the victim. This can be done through various means such as email attachments (spearphishing), malicious links, compromised websites, or USB drives.

**Detection opportunities:**
- Email gateway filtering
- Web proxy logs
- User reports
- Threat intelligence feeds

## 4. Exploitation

The delivered payload is triggered, exploiting a vulnerability in the target system. This is when code execution begins.

**Detection opportunities:**
- Endpoint detection and response (EDR)
- Application logs
- Antivirus alerts
- Crash reports

## 5. Installation

The malware installs itself on the victim system, establishes persistence, and prepares for further actions. Examples include installing a rootkit, creating scheduled tasks, or modifying startup configurations.

**Detection opportunities:**
- File system changes
- Registry modifications (Windows)
- Sysmon logs
- Unusual process behavior

## 6. Command and Control (C2)

The attacker establishes a communication channel with the compromised system to control it remotely. This often involves connecting to a command-and-control server over HTTP, HTTPS, DNS, or other protocols.

**Detection opportunities:**
- Network traffic analysis
- DNS tunneling detection
- Firewall and proxy logs
- Beaconing behavior

## 7. Actions on Objectives

The attacker performs the final objective, which could be data theft, ransomware deployment, privilege escalation, lateral movement, or system disruption.

**Detection opportunities:**
- Data exfiltration monitoring
- Large file transfers
- Abnormal database queries
- Insider threat detection tools

## Application to SOC and Blue Team Operations

Understanding the Cyber Kill Chain helps SOC analysts identify where they can insert detection and response mechanisms in the attack lifecycle. Effective defense involves:

- Detecting early-stage reconnaissance through deception or anomaly detection
- Filtering and sandboxing incoming files and URLs
- Monitoring endpoint behavior for signs of exploitation and installation
- Logging and correlating network traffic for signs of C2 activity
- Preventing data loss and maintaining system integrity

## Example Attack Mapping

| Stage                 | Technique                              |
|----------------------|----------------------------------------|
| Delivery             | Spearphishing attachment               |
| Exploitation         | Exploit public-facing application      |
| Installation         | PowerShell / Dynamic Linker Hijacking |
| Command & Control    | Fallback channels                      |
| Actions on Objectives| Data from local system                 |

## References

- Lockheed Martin Cyber Kill Chain: https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html
- MITRE ATT&CK Framework: https://attack.mitre.org/
