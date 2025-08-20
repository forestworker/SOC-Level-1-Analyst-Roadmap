# Networking Essentials

## Overview
Networking essentials cover the **basic protocols and mechanisms** required for network communication.

## Fundamental Protocols
- **DHCP (Dynamic Host Configuration Protocol)**: Automatically assigns IP addresses, subnet masks, and gateways to clients.
- **DNS (Domain Name System)**: Translates domain names into IP addresses (e.g., `example.com` → `93.184.216.34`).
- **Routing Protocols**: Decide the path packets take across networks (e.g., RIP, OSPF, BGP).

## Packet Structure
- **Source IP**: The address of the sending device.
- **Destination IP**: The address of the receiving device.
- **Payload**: The actual data being transmitted.
- **Headers**: Metadata used for delivery and error checking.

## SOC Analyst Relevance
- DNS abuse (DNS tunneling, exfiltration).
- DHCP spoofing can redirect traffic to malicious servers.
- Routing attacks can lead to man-in-the-middle interception.
