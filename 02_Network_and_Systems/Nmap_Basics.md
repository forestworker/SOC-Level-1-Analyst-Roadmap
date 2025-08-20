# Nmap: The Basics

## Overview
Nmap (Network Mapper) is a versatile tool for network discovery, scanning, and auditing.

## Key Capabilities
- **Host Discovery**: Identify live hosts on a network.
- **Port Scanning**: Determine which ports are open or closed.
- **Service Detection**: Identify the service and version running on open ports.
- **OS Fingerprinting**: Guess the operating system of a target device.

## Example Commands
- `nmap -sn 192.168.1.0/24` – Discover live hosts in a subnet.
- `nmap -p 1-1000 192.168.1.1` – Scan the first 1000 ports on a host.
- `nmap -sV 192.168.1.1` – Detect service versions.
- `nmap -O 192.168.1.1` – Perform OS detection.

## SOC Analyst Usage
- Validating network inventory against expected configurations.
- Detecting unauthorized services exposed to the internet.
- Identifying signs of reconnaissance activity by attackers.
