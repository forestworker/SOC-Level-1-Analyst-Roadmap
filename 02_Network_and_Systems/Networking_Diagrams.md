# Networking Diagrams

This document contains simplified ASCII diagrams to visualize key networking concepts. 
These diagrams are designed to be displayed directly in Markdown repositories such as GitHub.

---

## OSI vs TCP/IP Model

```
OSI Model              TCP/IP Model
-----------            --------------
Application            Application
Presentation           
Session                
Transport              Transport
Network                Internet
Data Link              Link
Physical
```

---

## Basic Network Flow

```
[ Client ] ---> [ Router ] ---> [ Server ]
       Source IP        Destination IP
```

Explanation:
- **Client** sends a request with its Source IP.
- **Router** forwards packets based on routing tables.
- **Server** receives the request at its Destination IP.

---

## TCP Three-Way Handshake

```
Client                       Server
  | -------- SYN -------->     |
  | <------- SYN-ACK ------    |
  | -------- ACK -------->     |
```

Explanation:
- **SYN**: Client asks to start a connection.
- **SYN-ACK**: Server acknowledges and agrees.
- **ACK**: Client confirms, and the connection is established.

---

## Encrypted vs Unencrypted Communication

```
Unencrypted (HTTP):   Client ----> Server (Plaintext)
Encrypted   (HTTPS):  Client ==TLS==> Server (Encrypted)
```

---

## Packet Capture Flow

```
[ NIC ] --> [ tcpdump ] --> capture.pcap --> [ Wireshark Analysis ]
```

Explanation:
- **NIC** (Network Interface Card) receives traffic.
- **tcpdump** captures raw packets.
- **capture.pcap** is the saved file.
- **Wireshark** is used to analyze the captured traffic.

---

## Example Network Scan with Nmap

```
[ Analyst ] --Nmap Scan--> [ Target Host ]
              (Open Ports, Services, OS Fingerprinting)
```

---

