# Networking Core Protocols

## Overview
Core protocols form the backbone of TCP/IP networking and are critical for communication across networks.

## Protocols
1. **IP (Internet Protocol)** – Provides unique addressing and packet routing across networks.
2. **TCP (Transmission Control Protocol)** – Offers reliable, connection-oriented communication with flow control and retransmission.
3. **UDP (User Datagram Protocol)** – Provides fast, connectionless communication, used in streaming and DNS.
4. **ICMP (Internet Control Message Protocol)** – Used for diagnostics (ping, traceroute) and error reporting.

## Security Implications
- **TCP SYN Floods**: Exploit TCP handshake to exhaust resources.
- **UDP Floods**: Overwhelm services using amplification attacks.
- **ICMP Misuse**: Attackers may tunnel data or map networks.

## SOC Analyst Focus
- Understand the difference between legitimate and abnormal traffic patterns.
- Detect DoS/DDoS attempts and reconnaissance activities.
