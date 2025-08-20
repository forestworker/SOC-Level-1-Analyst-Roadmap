# Wireshark: The Basics

## Overview
Wireshark is a graphical packet analysis tool widely used by network administrators and security analysts.

## Key Features
- Captures live network traffic.
- Supports protocol dissection for hundreds of protocols.
- Allows filtering and searching to isolate relevant traffic.
- Provides visualization of conversations and streams.

## Example Filters
- `ip.addr == 192.168.1.10` – Show traffic involving a specific host.
- `tcp.port == 80` – Show HTTP traffic.
- `http.request` – Show HTTP requests.

## SOC Analyst Usage
- Investigating malware communication patterns.
- Analyzing suspicious PCAP files from incidents.
- Identifying exfiltration attempts or unusual connections.
