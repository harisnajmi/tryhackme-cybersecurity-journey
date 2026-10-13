## The Greenholt Phish

## Overview

A sales executive at Greenholt PLC has reported a suspicious email received from a known customer. The message raised several red flags: a generic greeting, an unexpected request for a money transfer, and an unsolicited attachment. According to the employee, this behavior does not align with the customer’s usual communication style. Concerned that the email may be malicious, the message has been escalated to the SOC (Security Operations Center) for further investigation. Your goal is to analyze the provided email sample and determine whether it is legitimate or part of a phishing attempt.

### Objective

- Analyze the provided email to identify and extract key artifacts
- Investigate the message source to determine its origin and authenticity
- Use analysis tools to assess the potential maliciousness of the email

## Tools Used

| Tool | Purpose |
|---|---|
| Tool | Used for |

---

## Tasks

### Task 1 — What is the Transfer Reference Number listed in the email's Subject line?
![](screenshots/insertname.png)

-

### Task 2 — What is the display name of the sender?
![](screenshots/insertname.png)

-

### Task 3 — Continue investigating the email headers.
What is the sender's email address?
![](screenshots/insertname.png)

-

### Task 4 — What email address will receive a reply to this email?

![](screenshots/insertname.png)

-

### Task 5 — Begin analyzing the message source.
What is the originating IP address of this email?

![](screenshots/insertname.png)

-

### Task 6 — Investigate the IP address from the previous question.
Who is the owner of the originating IP?

![](screenshots/insertname.png)

-

### Task 7 — Run an SPF record check on the Return-Path domain identified in the email headers.
What is the full SPF record for this domain?

![](screenshots/insertname.png)

-

### Task 8 — Perform a DMARC lookup for the Return-Path domain found in the email headers.
What is the complete DMARC record for this domain?

![](screenshots/insertname.png)

-

### Task 9 — What is the file name of the attachment found in the email?

![](screenshots/insertname.png)

-

### Task 10 — Download the attachment to your virtual environment.
Using the sha256sum command, what is the SHA256 hash of the file?

![](screenshots/insertname.png)

-

### Task 11 — Investigate the file hash from the previous question using VirusTotal.
What is the attachment's file size in KB (e.g., 122.31 KB)?

![](screenshots/insertname.png)

-

### Task 12 — Continue your research on the file.
What is the actual file type of the attachment?

![](screenshots/insertname.png)

-

---

## Key Takeaways

- **Takeaway 1** — 

### Practical Application

---
