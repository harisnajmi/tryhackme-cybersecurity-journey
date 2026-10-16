
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

---

## Wireshark Protocol Filters

## Overview

Wireshark supports 3000 protocols and allows packet-level investigation by filtering the protocol fields. This task shows the creation and usage of filters against different protocol fields.

### Objective

- Utilize the protocol filters to help analysts filter the traffic according to the IP level information from the packets (Network layer of the OSI model).
- These filters filter network-level information like IP addresses, version, time to live, type of service, flags, and checksum values.
---

### Useful and Commonly Used Filters

### Filters

1. ip — show all IP packets.
2. ip.addr — show packets for a specific IP
3. ip.src — show packets from a specific IP
4. ip.dst — show packets to a specific IP
5. tcp.port/udp.port — show packets for a specific TCP/UDP port
6. tcp.srcport/udp.srcport — show packets from a specific TCP/UDP port
7. tcp.dstport/udp.dstport — show packets to a specific TCP/UDP port
8. http — show all HTTP packets
9. http.response.code — show all packets with a specific response code (200 for successful)
10. http.request.method — show all packets with a specific request method (GET, POST)
11. dns — show all DNS packets
12. dns.flags.response — show packets for a specific DNS response (0 for request, 1 for response)
13. dns.qry.type — show packets for a specific DNS type (eg. 1 for "A")

---

## Tasks

### Task 1 — What is the number of IP packets?
![](screenshots/10total-ip-packets.png)

### Task 2 — What is the number of packets with a "TTL value less than 10"?
![](screenshots/11ttl-less-than-10.png)

### Task 3 — What is the number of packets which uses "TCP port 4444"?
![](screenshots/12tcp-4444-packets.png)

### Task 4 — What is the number of "HTTP GET" requests sent to port "80"?

![](screenshots/13get-request-tcpudp-80.png)

### Task 5 — What is the number of type A DNS Queries?

![](screenshots/14total-dns-type-a.png)

- Therefore, filters like dns.flags.response == 1 && dns.qry.type == 1 are used because the requested data points (Type A records) are delivered and parsed within the response packets.

---

## Key Takeaways

- **Takeaway 1** — 

### Practical Application
