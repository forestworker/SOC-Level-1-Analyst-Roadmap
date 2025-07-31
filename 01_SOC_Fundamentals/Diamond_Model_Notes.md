# The Diamond Model of Intrusion Analysis

## Overview

The Diamond Model is a cybersecurity framework developed to help analysts understand, categorize, and investigate cyber intrusions. It is especially useful in SOC (Security Operations Center) environments for tracking and analyzing threat actor behaviors and patterns.

The model represents intrusions as relationships between four core features: **Adversary**, **Infrastructure**, **Capability**, and **Victim**. These four features form the vertices of a diamond shape, with each vertex connected to the others.

## The Four Core Features

### 1. Adversary
The actor or group responsible for the intrusion. This could be a named APT group, a cybercriminal organization, or an unknown individual.

**Examples:**
- APT29 (nation-state group)
- Lone ransomware operator
- Insider threat

### 2. Capability
The tools and methods used by the adversary to achieve their goals. This includes malware, exploits, techniques, scripts, and procedures.

**Examples:**
- Remote Access Trojan (RAT)
- Mimikatz for credential dumping
- Exploits for known vulnerabilities

### 3. Infrastructure
The physical or logical communication channels used by the adversary to deliver their capability or maintain access to the target.

**Examples:**
- C2 servers
- Phishing domains
- Compromised VPN connections

### 4. Victim
The target of the intrusion. This includes the organization, network, or specific assets or users being attacked.

**Examples:**
- Government network
- Energy company SCADA system
- Finance department employee

## Use in SOC Level 1

For SOC1 analysts, the Diamond Model is a valuable mental tool for:

- Structuring alerts and incidents: Helps categorize observed artifacts and events.
- Supporting correlation: Links infrastructure (e.g., IPs/domains) to capabilities (e.g., malware) and known adversaries.
- Enabling threat hunting: Assists in formulating hypotheses by exploring relationships across the diamond.
- Informing reporting: Provides context that helps escalate or de-escalate alerts.
- Feeding threat intelligence platforms and enrichment tools.

## Practical Example

**Alert:** Employee received a spearphishing email with a malicious Excel attachment that connects to a suspicious IP.

**Mapped in Diamond Model:**
- Adversary: Unknown (potential phishing campaign actor)
- Capability: Excel doc with macro and payload
- Infrastructure: IP address used for callback / C2
- Victim: Employee email system / endpoint

This allows SOC1 to log relationships, enrich threat intel, and monitor for reuse of infrastructure or TTPs.

## Additional Notes

- The Diamond Model supports pivoting from one known point (e.g., IP) to others (e.g., tool, victim).
- It is complementary to frameworks like MITRE ATT&CK and Cyber Kill Chain.
- Analysts can use it to support visual mapping in SIEMs and threat intel platforms.

## References

- Original Paper: "The Diamond Model of Intrusion Analysis" by Caltagirone, Pendergast, and Betz (2013)
- MITRE ATT&CK Framework: https://attack.mitre.org/
- SANS Reading Room: https://www.sans.org/reading-room/
