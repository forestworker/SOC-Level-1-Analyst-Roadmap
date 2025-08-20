# Tcpdump: The Basics

## Overview
Tcpdump is a lightweight, command-line utility for packet capture and network troubleshooting.

## Key Commands
- Capture traffic on all interfaces: `tcpdump`
- Capture from a specific interface: `tcpdump -i eth0`
- Save traffic to a file: `tcpdump -w file.pcap`
- Read captured traffic: `tcpdump -r file.pcap`

## Filtering Examples
- `tcpdump host 192.168.1.1` – Capture all traffic to/from a host.
- `tcpdump port 443` – Capture HTTPS traffic.
- `tcpdump icmp` – Capture ping and ICMP messages.

## SOC Analyst Usage
- Capturing network traffic on servers for later analysis.
- Verifying suspicious connections in real-time.
- Exporting PCAP files for detailed review in Wireshark.
