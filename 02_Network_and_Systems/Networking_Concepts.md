# Networking Concepts

## Overview
Networking concepts explain how devices interact within local and global networks. 
Two major frameworks describe this communication process: the **OSI Model** and the **TCP/IP Model**.

## OSI Model
The OSI (Open Systems Interconnection) model divides communication into **seven layers**, each responsible for a specific function:

1. **Physical Layer** – Transmission of raw data over physical media (cables, radio signals).
2. **Data Link Layer** – Provides node-to-node delivery using MAC addresses (Ethernet, Wi-Fi).
3. **Network Layer** – Responsible for logical addressing and routing (IP addresses).
4. **Transport Layer** – Ensures reliable communication through TCP (connection-oriented) or UDP (connectionless).
5. **Session Layer** – Establishes and manages sessions between applications.
6. **Presentation Layer** – Handles encryption, compression, and data formatting.
7. **Application Layer** – Interfaces with user applications (HTTP, FTP, DNS).

## TCP/IP Model
The TCP/IP model is a simplified four-layer model widely used in practice:

1. **Link Layer** – Hardware addressing and physical data transfer.
2. **Internet Layer** – Provides logical addressing and routing (IP).
3. **Transport Layer** – Offers reliable and unreliable transport (TCP/UDP).
4. **Application Layer** – Includes protocols like HTTP, DNS, SMTP.

## Importance for SOC Analysts
- Enables mapping of attacks to the correct network layer.
- Helps understand which layer to investigate when anomalies occur.
- Guides in selecting appropriate monitoring tools and controls.
