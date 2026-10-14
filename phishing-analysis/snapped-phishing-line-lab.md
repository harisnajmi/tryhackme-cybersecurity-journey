
## Snapped Phishing Line Lab

## Overview

As a member of the IT department at SwiftSpend Financial, you are responsible for assisting employees with technical concerns. What initially appeared to be a routine day quickly escalated when multiple employees across different departments reported receiving a suspicious email. Several users noted unusual characteristics in the message, and unfortunately, some had already submitted their credentials and were no longer able to access their accounts. With the potential for a wider compromise, the incident has been escalated for investigation. Your task is to analyze the available evidence, determine the scope of the attack, and uncover how the adversary operated.

### Objective

- Analyze the provided email samples to identify key artifacts
- Investigate phishing URLs to understand redirection
- Retrieve and examine the phishing kit used in the attack
- Use CTI tools to gather intelligence on the adversary
- Analyze the phishing kit to uncover additional indicators

## Tools Used

| Tool | Purpose |
|---|---|
| CLI | Navigating directory and downloading files using CLI, hash generation |

---

## Tasks

### Task 1 — Begin reviewing the emails in the phish-emails folder on your desktop.
### Which individual received the email regarding a Quote for Services Rendered?
![](screenshots/43email-recepient.png)

- Identified the recipient of the email from observation.

### Task 2 — What email address was used by the adversary to send the phishing emails?
![](screenshots/44sender-email-address.png)

- Identified the email address through observation.

### Task 3 — Investigate the attachment in the email addressed to Zoe Duncan.
### What is the root domain of the redirection URL found within the file?
![](screenshots/45redirection-root-domain.png)

- Downloaded the attachment in a dedicated email attachment folder. Hovering over the button reveals the redirection url.

### Task 4 — Open the attachment in your VM web browser.
### Which company is the login page impersonating?

![](screenshots/46microsoft-impersonation.png)

- Based on observation, key product names such as Office365 and One Drive indicate that the threat actor is impersonating Microsoft.

### Task 5 — Let’s check if the attacker left any files exposed on the same website. Navigate to the /data directory.
### What is the name of the archive file?

![](screenshots/47cli-directory-curl.png)
![](screenshots/48download-wget.png)

- Used CLI and curl commands to navigate the directory and identify the archived file. Used wget to download the archive file into my directory.

### Task 6 — Download the phishing kit archive to your virtual environment.
### Using the sha256sum command, what is the SHA256 hash of the file?

![](screenshots/49zip-hash.png)

- Used sha256sum to generate the hash of the file and for analysis on VirusTotal.

### Task 7 — Investigate the file hash from the previous question using VirusTotal.
### Aside from phishing, what other threat category is assigned to the ZIP archive?

![](screenshots/50other-threat-category.png)

- Identified the other threat category in VirusTotal in the threat category section.

### Task 8 — Review the VirusTotal Details page for the phishing kit.
### How many files are contained within the archive?

![](screenshots/51total-files-in-zip.png)

- VirusTotal indicates that they are 49 total files within the zip.

### Task 9 — Let’s see if the attacker has exposed any captured credentials. Navigate to the /data/Update365/ directory and investigate the log file.
### What is the email address of the user who submitted their credentials more than once?

![](screenshots/52download-move-log-file.png)
![](screenshots/53email-login.png)

- Downloaded the log.txt file and used cat and grep to identify the credentials that were submitted. Notice one email has been submitted more than once.

### Task 10 — Extract the phishing kit archive and locate the submit.php file.
### What email address is used by the adversary to collect compromised credentials?
![](screenshots/55cat-submit-php.png)
![](screenshots/54credentials-recipient.png)

- Navigated to the directory that contains the submit.php file, identified the email that is receiving the credentials.

### Task 11 — Return to the phishing URL and locate the flag.txt file.
### Using CyberChef to decode the flag, what is the secret value?

![](screenshots/56curl-flag.png)
![](screenshots/57flag-decoded.png)

- Acquired the flag of this lab and decode using base64 and reverse recipe.

---

## Key Takeaways

- **Takeaway 1** — This lab requires me to use commands that I am not familiar with such as curl and wget, these commands are powerful and useful for investigation and threat hunting in safe manner. I am interested how other or perhaps how these commands can be further utilize for other applications.
- **Takeaway 2** — This lab also establishes the general mindset one would require in investigating phishing emails, ultimately all the tasks assigned is building context, threat vector and IOC enrichment that is sufficient for a smooth remediation plan or escalation to L2. 

### Practical Application
In live SOC environment, getting all necessary context and information to fully understand the situation and severity is highly important. Mastering these will add value to one's skillset and will allow them to conduct an independent investigation beyond surface level L1 workflow. CLI is a skill that offers flexibility and powerful tool to hone.

---
