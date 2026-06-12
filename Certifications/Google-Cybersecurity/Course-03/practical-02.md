# Incident Response : Web Server Compromise & Malware Distribution

Assessment Context: Scenario-Based Simulation (Google Cybersecurity Professional Certificate)  
Activity: Applying OS Hardening 
Role Assumed: Cybersecurity Analyst 
Incident Type: Web Defacement, Malware Distribution, Brute Force Attack  

> *Note: This document is a practical activity for the Google Cybersecurity Professional Certificate. It represents a scenario-based simulation where I assume the role of a Cybersecurity Analyst / Incident Responder investigating a web server compromise and developing a strategic remediation plan. Proprietary details have been redacted for confidentiality.*

---

## Executive Summary
This report details the investigation and remediation of a security incident involving the compromise of the corporate website (official Website). An unauthorized actor gained administrative access via a brute force attack, leveraging default credentials. The attacker injected malicious JavaScript into the site’s source code, forcing visitors to download an executable file that redirected them to a fraudulent, malware-hosting domain (Fake Webiste). 

Through sandbox analysis and network traffic inspection using tcpdump, the attack chain was fully mapped and confirmed. The incident was resolved by isolating the server, restoring clean backups, and implementing comprehensive OS hardening and Identity and Access Management (IAM) controls to prevent recurrence.

---

## Incident Timeline & Execution
1. Initial Access: The attacker targeted the website's administrative portal. Due to the account relying on default credentials and lacking brute-force mitigation (e.g., account lockouts), the attacker successfully guessed the password.
2. Persistence & Payload Delivery: Once inside the admin panel, the attacker modified the website's source code. They injected a JavaScript function designed to prompt visitors to download an executable file disguised as a mandatory browser update or "free recipe" access. 
3. Lockout: To maintain control and delay detection, the attacker changed the administrative password, locking out the legitimate website owner.
4. Detection: The breach was identified when the IT helpdesk received a surge of customer complaints regarding unexpected download prompts, sudden URL redirects, and degraded PC performance. The incident was formally escalated when the owners of the website discovered they were locked out of the admin panel.
5. Analyst Confirmation & Code Review: A senior analyst confirmed the website was compromised by inspecting the site's source code. They discovered that malicious JavaScript code had been injected to prompt visitors into downloading an executable file. Analysis of the downloaded file revealed a redirect script designed to bounce visitors' browsers from the official Website to the Fake Webiste.

---

## Investigation & Technical Analysis
Upon escalation, I was tasked to carry out an investigation to determine the scope and mechanics of the breach. 

### 1. Safe Replication (Sandboxing)  
To avoid infecting production machines, I set up an isolated sandbox environment. Navigating to the compromised site immediately triggered the malicious download prompt. I allowed the executable to run within the controlled environment to observe its behavior.

### 2. Network Traffic Analysis (tcpdump)
I captured the network traffic during the sandbox execution to map the attack chain. The packet logs clearly outlined the malicious workflow:
* Step 1: Browser initiates a DNS request for the Official Website and receives the legitimate IP.
* Step 2: Browser sends an HTTP GET request to load the webpage.
* Step 3: The injected JavaScript forces the browser to download the malicious executable.
* Step 4: Upon execution, the browser initiates a new DNS request for the Fake Webiste.
* Step 5: The browser sends an HTTP request to the attacker's IP, loading the fraudulent, malware-laden site.

### 3. Code Analysis  
Collaborating with a senior analyst, we reviewed the website’s source code and confirmed the presence of the injected JavaScript. Static analysis of the downloaded executable confirmed it contained a simple but effective redirect script designed to bounce the user to the attacker's domain.

---

## Root Cause Analysis
The root cause of this breach was a failure in basic Identity and Access Management (IAM) hygiene. Specifically:
* The administrative account was left configured with factory-default credentials.
* The Operating System and web application lacked rate-limiting or account lockout policies, allowing the brute force attack to proceed indefinitely until successful.

---

## Remediation
To ensure this does not happen again, I developed and presented a remediation plan focusing on OS hardening and robust password management.

### Identity & Access Management (IAM) Overhaul
* Implement Account Lockout Policies and Rate Limiting: To directly neutralize brute force attacks, the Operating System and web application must be configured to automatically lock user accounts after a maximum of 3 to 5 consecutive failed login attempts. Because brute force attacks rely on making thousands of rapid password guesses, an account lockout instantly halts the attack by cutting off access at the source. This should be paired with a mandatory cooldown period or requiring administrator intervention to unlock the account, ensuring the attacker cannot simply resume guessing.

---

## Lessons Learned & Professional Reflection
This incident reinforced several critical cybersecurity principles that I now apply to all my work:

1. Defaults are a Silent Killer: The most sophisticated attacks often start with the simplest oversights. Assuming a system is secure out-of-the-box is a dangerous fallacy. Hardening must be the first step of any deployment.
2. The Helpdesk is a Vital Sensor: While technical alerts are important, user reports are often the fastest indicator of a breach. Fostering a strong relationship between the security team and the helpdesk is crucial for rapid detection.
3. Defense in Depth is Non-Negotiable: If the password policy had failed, file permissions should have stopped the code injection. If that failed, FIM should have alerted us. Relying on a single security control is a recipe for disaster.
4. Proactive > Reactive: Investigating the breach was valuable, but the real win was using the incident to justify and implement a company-wide password management strategy and OS hardening baseline, shifting our security posture from reactive firefighting to proactive defense.

---

*Note: This case study has been anonymized and adapted for portfolio purposes to demonstrate incident response methodology, technical analysis, and strategic remediation planning. Proprietary details and specific domain names have been redacted for confidentiality.*


📄 [View Full Risk Assessment Document (PDF)](./security-incident-report.pdf)