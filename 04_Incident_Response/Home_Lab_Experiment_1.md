# Home Lab – Recon and Log Visibility Test

## Date
July 25, 2025

## Objective
To simulate basic network reconnaissance from Kali Linux against an Ubuntu VM and test if any trace of that activity is visible on the target system. The goal was to better understand the limitations of log visibility and how to improve it.

## Lab Setup
- **Attacker**: Kali Linux (VirtualBox)
- **Target**: Ubuntu 22.04 (VirtualBox)
- **Network**: Host-only adapter (same subnet)

## Actions Taken

1. Started both VMs and confirmed IP addresses.
2. From Kali, ran:
   - `ping <Ubuntu_IP>`
   - `nmap -sS -Pn <Ubuntu_IP>` to perform a stealth TCP scan
3. On the Ubuntu machine, initially checked:
   - `/var/log/syslog`
   - `journalctl`
   - `/var/log/auth.log`

To my surprise — **nothing showed up**. No logs, no alerts, no signs of reconnaissance. It was a real eye-opener: without proper monitoring tools or logging configuration, even obvious attacks can pass completely unnoticed.

## Improvements Made

I enabled the default Ubuntu firewall and turned on logging:

```bash
sudo ufw enable
sudo ufw logging on

Then I reran the scan and monitored logs in real time:

sudo tail -f /var/log/ufw.log

Suddenly I could see traffic from my Kali box hitting the target.

[UFW BLOCK] IN=enp0s3 OUT= MAC=08:00:27:... SRC=192.168.56.101 DST=192.168.56.102 ...


Test Completed