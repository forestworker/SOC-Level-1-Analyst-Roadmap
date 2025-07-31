# Credential Guard – SOC Analyst Notes

## Overview

Credential Guard is a security feature in Windows that uses virtualization-based security (VBS) to isolate secrets such as NTLM hashes and Kerberos tickets from the operating system, preventing theft even by privileged malware.

## Key Concepts

- Runs LSASS in an isolated virtual container
- Blocks direct access to credential material in memory
- Reduces risk of Pass-the-Hash and Pass-the-Ticket attacks

## SOC Analyst Use Cases

- Confirm deployment across endpoints using PowerShell or WMI
- Monitor for attempts to disable or bypass Credential Guard
- Validate credential isolation during post-incident analysis

## Related MITRE ATT&CK Techniques

- T1003 – OS Credential Dumping
- T1550 – Use Alternate Authentication Material
- T1562 – Impair Defenses

## Validation

```powershell
Get-CimInstance -ClassName Win32_DeviceGuard
```

Ensure `CredentialGuard` is listed under `SecurityServicesConfigured`.
