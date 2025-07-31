# BitLocker Drive Encryption – SOC Analyst Notes

## Overview

BitLocker is a full-disk encryption feature in Windows designed to protect data at rest. It encrypts entire volumes using the XTS-AES algorithm and integrates with hardware security components like the TPM (Trusted Platform Module).

## Key Concepts

- Encrypts data using XTS-AES 128-bit or 256-bit encryption
- Uses TPM, USB key, PIN, or password for unlocking
- Activation occurs at system boot
- Prevents unauthorized offline data access

## Threat Mitigation

| Threat Type             | BitLocker Protection Mechanism           |
|-------------------------|-------------------------------------------|
| Stolen or lost devices  | Prevents unauthorized data access         |
| Disk removal attacks    | Disk is unreadable without the proper key |
| Boot from external media| Bootloader is protected by encryption     |

## SOC Analyst Use Cases

- Verify encryption status using `manage-bde -status`
- Monitor for attempts to disable BitLocker
- Ensure recovery keys are securely stored (e.g., AD, Azure AD)
- Validate encryption during incident response for lost/stolen devices

## Related MITRE ATT&CK Techniques

- T1555.003 – Credentials from Password Stores
- T1003 – OS Credential Dumping

## Commands

```bash
manage-bde -status C:
manage-bde -on C: -tpm
manage-bde -on C: -pw
```
