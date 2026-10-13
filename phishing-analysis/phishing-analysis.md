## 1. Phishing Analysis Fundamentals

## Overview
Explore the anatomy of an email, starting with the structure of an email address and the path a message takes from sender to recipient. Developed the technical skills needed to investigate suspicious emails by extracting and analyzing both the header and body source code. Examine common phishing techniques and applied knowledge to analyze real-world examples, identifying attacker intent.

### Objective

- Understand how email delivery works and its processes.
- How to read the message source and identifying key components.
- Identify basic phishing attempts and conduct simple analysis.
- Apply defang to prevent accidental clicks.

## Tools Used

| Tool | Purpose |
|---|---|
| Tryhackme Lab Room | Identification and analysis of phishing attempts|

---

## Tasks

### Task 1 — Reputable organization that is being spoofed
![Spoofed Organization](screenshots/01spoofed-organization.png)

- Email sender identifies as "Home Depot" however the email domain is "teckbe.com". This mismatch indicates spoofing of a reputable organization.

### Task 2 — Sender's email address
![Sender Email Address](screenshots/02sender-email-address.png)

- Identify the email address of the sender that is attempting to spoof.

### Task 3 — Defanged X-Originating-IP
![X-Orignating-IP](screenshots/03x-originating-ip.png)
![Defang X-Originating-IP](screenshots/04defang-x-originating-ip.png)

- Identified x-originating-ip from message source and use Cyberchef "Defang IP addresses" recipe to defang the IP.

### Task 4 — Mail server generated the Authentication-Results header

![Mal Server](screenshots/05mail-server-generated.png)

- Identified the mail server that authenticated the email. ("Authentication-Results:")

---

## Key Takeaways

- **[Takeaway 1]** — Understanding the anatomy of an email and the path of a message goes from sender to receipient.
- **[Takeaway 2]** — It is important to remember that a message source contains more useful and hidden information than what is being rendered and shown on the front end.
- **[Takeaway 3]** — Analysis of possible phishing attempts must be handled accordingly and in a safe manner to prevent accidental breaches.

### Practical Application

In an SOC live environment, it is important to know where to get these hidden information that may provide additional context and assist in identifying IOCs. A wealth of information is available to further strengthen verdict formation for L1 and context for escalation to L2 which will ensure a smooth and quick investigation. 

---
## 2. Phishing Analysis Tools

## Overview
Build on that foundation by learning about the tools that enable deeper analysis, then apply skills by investigating three real-world phishing cases.
### Objective

- Understand what information should be collected during an email analysis
- Learn about the tools that enable effective email investigation
- Explore IP and URL analysis, including reputation lookups
- Investigate phishing cases to apply your understanding and strengthen your analysis skills

## Tools Highlighted

| Tool | Purpose |
|---|---|
| Messageheader | Analyze email headers |
| IPinfo | Gathering information about an IP address |
| URLScan.io | Safely investigate websites without visiting them directly |
| Talos | Tool from Cisco that enables analysts to assess the reputation of IP |
| URL extraction tool | Automatically parse all embedded links |
| sha256sum | Generate a hash value for further analysis and reputation checks |
| VirusTotal | Check the reputation of files, URLs, IP addresses, and domains |
| ANY.RUN | Interactive malware sandbox |
| JOESandbox | Advanced malware analysis |
| PhishTool | Centralized view of phishing activity, automates much of the manual work involved in analyzing suspicious emails |

---

## Phishing Case 1: Account On Hold Email Analysis

### Task 1 — The reputable brand the email is impersonating
![](screenshots/06spoofed-organization.png)

### Task 2 — The intended recipient
![](screenshots/07recepient.png)

### Task 3 — The IP address "Received: from"
![](screenshots/08received-from-ip.png)

### Task 4 — Domain of interest from Return-Path
![](screenshots/10domain-of-interest.png)

### Task 5 — Shortened URL of "Update Account Now"
![](screenshots/09copy-shortened-url.png)

## Phishing Case 2: Update Payment Details Analysis

### Task 1 — ANYRUN classify this suspected phishing email as 
![](screenshots/11anyrun-classification.png)

### Task 2 — Name of malicious PDF attachment
![](screenshots/12paymentid-pdf.png)

### Task 3 — MD5 hash of the PDF
![](screenshots/13md5-hash.png)

### Task 4 — PDF's malicious URL
![](screenshots/14malicious-url.png)

### Task 5 — DNS of malicious domain.
![](screenshots/15malicious-dns.png)

## Phishing Case 3: Executable File Analysis

### Task 1 — Name of malicious Excel attachment
![](screenshots/16malicious-file-name.png)

### Task 2 — Suspicious process after attachment launch
![](screenshots/17suspicious-process.png)

### Task 3 — The full path to the malicious binary
![](screenshots/18full-path.png)

### Task 4 — CVE the file attempt to exploit
![](screenshots/19cve-exploit.png)

### Task 5 — Domain the malware was downloaded from
![](screenshots/20malicious-domain-source.png)

### Task 6 — Network threat associated with the download
![](screenshots/21network-threat.png)

---

## Key Takeaways

- **[Takeaway 1]** — 

### Practical Application

---

## Reusable Template 1
## x. Title/Room

## Overview

### Objective

## Tools Used

| Tool | Purpose |
|---|---|
| Tool | Used for |

---

## Tasks

### Task 1 — 
![](screenshots/insertname.png)

### Task 2 — 
![](screenshots/insertname.png)

### Task 3 — 
![](screenshots/insertname.png)

### Task 4 — 

![](screenshots/insertname.png)

---

## Key Takeaways

- **[Takeaway 1]** — The use of external tools automates IOC enrichment and quickens triage by substantial amount, however the fundamentals is still required to fully utilize such tools to its maximum effectiveness.

### Practical Application
In a live SOC environment, 3rd party tools and services significantly reduces the time to execute a triage and also increase the quality of triage. Utilizing these tools will assist in fatigue, improve workflow and internal processes through automated and enrichment of IOCs.
---




## Reusable Template 2.

[Room / Topic Name]

## Overview

### Objective

-

### Key Concepts

- [Concept 1]
- [Concept 2]
- [Concept 3]

---

## Tools Used

| Tool | Purpose |
|---|---|
| [Tool 1] | [What it was used for] |
| [Tool 2] | [What it was used for] |
| [Tool 3] | [What it was used for] |

---

## Methodology

### Step 1 — [Investigation / Analysis Step]

[Describe what you did and why.]

### Step 2 — [Investigation / Analysis Step]

[Describe what you did and why.]

### Step 3 — [Investigation / Analysis Step]

[Describe what you did and why.]

### Step 4 — [Investigation / Analysis Step]

[Describe what you did and why.]

---

## Evidence

### [Evidence / Finding Name]

**Observation:**

[Describe what the evidence shows.]

**Analysis:**

[Explain why the evidence is significant.]

**Screenshot:**

![Description of screenshot](screenshots/example.png)

---

### [Evidence / Finding Name]

**Observation:**

[Describe what the evidence shows.]

**Analysis:**

[Explain why the evidence is significant.]

**Screenshot:**

![Description of screenshot](screenshots/example-2.png)

---

## Findings

### Finding 1 — [Finding Name]

**Observation:**  
[What was discovered.]

**Impact / Significance:**  
[Why this matters from a security perspective.]

**Evidence:**  
[Reference the relevant evidence or screenshot.]

---

### Finding 2 — [Finding Name]

**Observation:**  
[What was discovered.]

**Impact / Significance:**  
[Why this matters from a security perspective.]

**Evidence:**  
[Reference the relevant evidence or screenshot.]

---

## Key Takeaways

- **[Takeaway 1]** — [What you learned.]
- **[Takeaway 2]** — [What you learned.]
- **[Takeaway 3]** — [What you learned.]

### Practical Application

[Briefly explain how this knowledge could be applied in a real SOC, incident response, threat hunting, detection engineering, or defensive security environment.]

---

## References

- [TryHackMe Room](https://tryhackme.com/)
- [Additional Reference](https://example.com/)
