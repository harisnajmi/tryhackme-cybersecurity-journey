
## Wireshark: Packet Operations

## Overview

Cover the fundamentals of packet analysis with Wireshark and investigate the event of interest at the packet-level.

### Objective

Investigate network traffic captures
View statistics including summary and protocol details
Uncover and apply packet filtering principles
Apply protocol filters
Apply advanced filtering

## Tools Used

| Tool | Purpose |
|---|---|
| Wireshark | Used for packet analysis |

---

## Tasks

### Task 1 — What is the IP address of the hostname starts with "bbc"?
![](screenshots/01bbc-ip.png)

### Task 2 — What is the number of IPv4 conversations?
![](screenshots/02total-ipv4.png)

### Task 3 — How many bytes (k) were transferred from the "Micro-St" MAC address?

![](screenshots/03micro-st-mac-address.png)
![](screenshots/04microst-bytes.png)

### Task 4 — What is the number of IP addresses linked with "Kansas City"?

![](screenshots/05ip-from-kansas-city.png)

### Task 5 — Which IP address is linked with "Blicnet" AS Organisation?

![](screenshots/06blicnet-ip-address.png)

---

## Key Takeaways

- **Takeaway 1** — Resolved Addresses (identify IP addresses and DNS names available in the capture file.)
- **Takeaway 2** — Protocol Hierarchy (breaks down all available protocols from the capture file and helps analysts view the protocols in a tree view based on packet counters and percentages.)
- **Takeaway 3** — Conversations (provides the list of the conversations in five base formats; ethernet, IPv4, IPv6, TCP and UDP.)
- **Takeaway 4** — Endpoints (provides unique information for a single information field such as Ethernet, IPv4, IPv6, TCP and UDP ).

---

## Statistics Protocol Details

### Objective
- Extends learning statistic feature to IPv4, IPv6, DNS and HTTP
- The statistics menu has two options for narrowing the statistics on packets containing a specific IP version. Thus, analysts can identify and list all events linked to specific IP versions in a single window and use it for the event of interest.

---

## Tasks

### Task 1 — What is the most used IPv4 destination address?
![](screenshots/07most-used-ip4.png)

### Task 2 — What is the max service request-response time of the DNS packets?
![](screenshots/08max-request-response-time.png)

### Task 3 — What is the number of HTTP Requests accomplished by "rad[.]msn[.]com?
![](screenshots/09radmsn-total-http-request.png)

---

## Key Takeaways

- **Takeaway 1** — Specific statistics feature for IPs, DNS and HTTP provides detail insights on the data capture summarized and organized to analysis. It is one of many useful tool in analyst's toolbox to investigate and identify anomalies.
