### Man-In-The-Middle Attacks

## Overview

Man-in-the-middle (MITM) attacks represent one of the most insidious threats in network security. In these attacks, attackers position themselves between legitimate communication endpoints to intercept, modify, or redirect traffic. From a blue team perspective, detecting these attacks requires a multi-layered approach combining network monitoring, certificate validation, and behavioral analysis. 
In this room, we'll learn the fundamentals of Man-in-the-Middle (MITM) attacks and how to spot the signs in network traffic.

### Objective

- Understand common MITM attack vectors and techniques
- Learn to identify indicators of compromise related to MITM attacks
- Master network monitoring tools for detecting suspicious traffic patterns
- Practice incident response procedures for MITM scenarios
- Cover three chained MITM techiques. ARP Spoofing, DNS Spoofing and SSL Stripping

## Tools Used
| Tool | Purpose |
|---|---|
| Wireshark | Deep packet analysis |

## Notes

1. Interception: The attacker inserts themselves into a communication stream, often by exploiting weaknesses in network protocols or by using techniques like ARP, DNS, or IP spoofing.
2. Manipulation/Decryption: The attacker tries to access or modify the communication, decrypting encoded data or injecting harmful content, such as altered website responses or fake login forms.
3. Packet sniffing: Capturing unencrypted data packets exchanged over a network, often on open Wi-Fi.
4. Session hijacking: Stealing and using session tokens to impersonate users.
5. SSL stripping: Downgrading HTTPS connections to insecure HTTP to steal or alter data transferred.
6. DNS spoofing: Redirecting legitimate website traffic to fraudulent domains by manipulating DNS responses.
7. IP spoofing: Crafting malicious IP packets that appear to come from trusted systems.
8. Rogue Wi-Fi access point: Creating fake networks to intercept user traffic.

### ARP Spoofing

### IoCs

1. Duplicate MAC-to-IP Mappings: Multiple MAC addresses claiming the same IP address. Indicates impersonation.
2. Unsolicited ARP Replies: High number of ARP replies without matching requests ("gratuitous ARP").
3. Abnormal ARP Traffic Volume: A Large number of ARP packets in short intervals.
4. Unusual Traffic Routing: Traffic rerouted through the attacker’s MAC.
5. Gateway Redirection Patterns: Multiple destination MACs for the same gateway IP.
6. ARP Probe / Reply Loops: Many ARP requests with Who has 192.168.1.x? Tell 192.168.1.y patterns.

### Task 1 — How many ARP packets from the gateway MAC Address were observed?
![](screenshots/12arp-packets-gateway.png)

- Filtered ARP and the initial source mac address in the packet capture. 

### Task 2 — What MAC address was used by the attacker to impersonate the gateway?
![](screenshots/13attacker-mac-addr.png)

- Search arp.opcode == 2 for the gateway address, identify "alternatives" mac address for the gateway.

### Task 3 — How many Gratuitous ARP replies were observed for 192.168.10.1?
![](screenshots/14gateway-gratuitous-reply.png)

- Filter for arp.isgratuitous and gateway address, only 2 packets were found.

### Task 4 — How many unique MAC addresses claimed the same IP (192.168.10.1)?
![](screenshots/15total-unique-mac-for-gateway.png)

- Search arp.opcode == 2 for the gateway address, count total unique mac address for the gateway.

### Task 5 — How many ARP spoofing packets were observed in total from the attacker?
![](screenshots/16total-arp-spoofing-packets.png)

- filtered for arp.opcode == 2, gateway ip address and the mac address of the attacker. Total 14 counts of packet

---

## Key Takeaways

- **Takeaway 1** — 

### Practical Application

---
