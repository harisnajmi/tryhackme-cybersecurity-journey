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
(screenshots/01spoofed-organization.png)
Email sender identifies as "Home Depot" however the email domain is "teckbe.com". This mismatch indicates spoofing of a reputable organization.

### Task 2 — Sender's email address
(screenshots/02sender-email-address.png)
Identify the email address of the sender that is attempting to spoof.

### Task 3 — Defanged X-Originating-IP
(screenshots/03x-originating-ip.png)
(screenshots/04defang-x-originating-ip)

Identified x-originating-ip from message source and use Cyberchef "Defang IP addresses" recipe to defang the IP.

### Task 4 — Mail server generated the Authentication-Results header

(screenshots/05mail-server-generated.png)
Identified the mail server that authenticated the email. ("Authentication-Results:")

---

## Key Takeaways

- **[Takeaway 1]** — Understanding the anatomy of an email and the path of a message goes from sender to receipient.
- **[Takeaway 2]** — It is important to remember that a message source contains more useful and hidden information than what is being rendered and shown on the front end.
- **[Takeaway 3]** — Analysis of possible phishing attempts must be handled accordingly and in a safe manner to prevent accidental breaches.

### Practical Application

In an SOC live environment, it is important to know where to get these hidden information that may provide additional context and assist in identifying IOCs. A wealth of information is available to further strengthen verdict formation for L1 and context for escalation to L2 which will ensure a smooth and quick investigation. 

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
[(screenshots/insertname.png)]

### Task 2 — 
[(screenshots/insertname.png)]

### Task 3 — 
[(screenshots/insertname.png)]

### Task 4 — 

[(screenshots/insertname.png)]

---

## Key Takeaways

- **[Takeaway 1]** — 

### Practical Application

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
