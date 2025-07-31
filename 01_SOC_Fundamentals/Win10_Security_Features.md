# Key Windows 10 Security Features – SOC Analyst Notes

## 1. Windows Defender Antivirus

A built-in antivirus solution with real-time protection, cloud-based analysis, and integration with AMSI for dynamic threat detection.

## 2. Windows Defender Application Control (WDAC)

Allows administrators to enforce application allowlists using code integrity policies, reducing the risk of malware execution.

## 3. Credential Guard

Utilizes virtualization-based security to protect login credentials from credential theft attacks.

## 4. Controlled Folder Access

Prevents unauthorized applications from modifying protected folders, helping mitigate ransomware threats.

## 5. Exploit Protection

Includes exploit mitigation techniques such as DEP, ASLR, and CFG. These can be configured on a per-process basis.

## 6. Windows Sandbox

Provides a disposable virtual environment for safely executing untrusted code or investigating suspicious files.

## 7. Defender for Endpoint (ATP/EDR)

Enterprise-level endpoint detection and response platform with threat hunting, alert correlation, and incident response features.

## SOC Analyst Takeaways

| Feature                  | Use Case                                       |
|--------------------------|------------------------------------------------|
| AMSI + Defender          | Detect and block malicious scripts dynamically |
| Credential Guard         | Prevent credential dumping and lateral movement|
| Controlled Folder Access | Mitigate unauthorized encryption or exfiltration |
| WDAC                     | Block unauthorized or unsigned applications    |
| Windows Sandbox          | Safe detonation of unknown executables         |
