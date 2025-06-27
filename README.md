# Task 4: Setup and Use a Firewall on Linux (UFW)

## Objective  
Configure basic firewall rules using UFW to block/allow traffic, understand how firewalls filter network activity, and test their effectiveness.

## Tools Used  
- Linux OS (Kali Linux)  
- UFW (Uncomplicated Firewall) – Lightweight and simple command-line firewall tool

## Steps Performed

1. Checked current firewall status:
   bash
   sudo ufw status
   
2. Enabled the firewall:
   bash
   sudo ufw enable
   
3. Listed current rules (before configuration):
   bash
   sudo ufw status numbered
   
4. Blocked inbound traffic on port 23 (Telnet):
   bash
   sudo ufw deny 23

5. Tested the Telnet block rule using:
   bash
   telnet localhost 23
   - Connection was refused, confirming the rule was active.

6. Allowed SSH (port 22) to ensure remote access:
   bash
   sudo ufw allow 22
   
7. Removed the test rule for Telnet after verification:
   bash
   sudo ufw delete deny 23
   
8. Took screenshots of the command execution and firewall status.

## How Firewall Filters Traffic (Summary)
   - UFW filters incoming and outgoing network traffic based on defined rules.

   - Default policies:
     - Deny incoming connections (unless allowed)
     - Allow outgoing by default

   - Each rule either allows or blocks traffic on a specific port or protocol (TCP/UDP).

   - Rules can be tailored to specific IP addresses, ports, or services.

## Output Files
   screenshots/ – Contains terminal screenshots showing UFW rules and testing

## Outcome
   Successfully configured a firewall using UFW, tested traffic blocking for Telnet, ensured SSH access remained available, and gained practical experience with Linux firewall management.
