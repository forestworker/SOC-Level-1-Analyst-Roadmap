# MITRE ATT&CK - Key Techniques for SOC Tier 1

MITRE ATT&CK is a knowledge base of cyber adversary behavior, reflecting real-world observations. It is organized into tactics (the "why") and techniques (the "how").

## Categories Overview

| Tactic               | Description                          | Example Techniques                          |
|----------------------|--------------------------------------|---------------------------------------------|
| Initial Access       | How attackers first gain entry       | Phishing, Exploiting Apps, Valid Accounts   |
| Execution            | Run malicious code                   | PowerShell, Scripting, Malicious Files      |
| Persistence          | Stay inside the system               | Startup Keys, Scheduled Tasks, User Creation|
| Privilege Escalation | Gain higher-level access             | Token Abuse, UAC Bypass, Setuid Exploits    |
| Defense Evasion      | Avoid detection                      | Obfuscation, Disabling Tools                |
| Credential Access    | Steal passwords/tokens               | Brute Force, Keylogging, Dumping Credentials|
| Discovery            | Learn about the environment          | Account Discovery, Port Scanning            |
| Lateral Movement     | Move across the network              | RDP, Pass-the-Hash, PSExec                  |
| Collection           | Gather sensitive data                | Screen Capture, Clipboard Data              |
| Command & Control    | Remote access/control                | C2 Channels via HTTP/DNS                    |
| Exfiltration         | Steal and transmit data              | Data Staging, Auto-Exfil, Upload            |
| Impact               | Damage or disrupt the target         | Data Wipe, Service Shutdown, Account Removal|