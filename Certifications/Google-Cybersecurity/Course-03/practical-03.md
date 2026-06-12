# Security Risk Assessment: Post-Breach Network Hardening

Assessment Context: Scenario-Based Simulation (Google Cybersecurity Professional Certificate)  
Activity: Applying Network Hardening  
Role Assumed: Security Analyst, Network Operations  
Subject: Analysis of Recent PII Data Breach and Network Hardening Recommendations  

---


> *Note: This document is a practical activity for the Google Cybersecurity Professional Certificate. It represents a scenario-based simulation where I assume the role of a Security Analyst conducting a post-breach assessment and network hardening strategy for a fictional social media organization.*

---

## Executive Summary
Following the recent data breach that exposed our customers' personal information (names and addresses), I conducted a comprehensive review of our network infrastructure to understand how the compromise occurred and how we can prevent it from happening again. As a social media organization, we hold massive amounts of sensitive user data, making our network a high-value target. 

The assessment revealed that our current security controls are severely lacking. We identified four critical vulnerabilities that directly enabled the attackers to access and extract our customer data. If we do not implement the recommended hardening practices immediately, the organization remains at a very high risk of experiencing another catastrophic breach.

---

## Incident Analysis & Vulnerability Breakdown

### 1. Widespread Password Sharing Among Employees
The Risk: Currently, our team members are sharing login credentials to access internal tools and systems. This creates a massive blind spot for our security team. When multiple people use the same account, we lose all accountability. If an account is compromised, we have no way of knowing which employee's machine was actually infected. Furthermore, if one employee leaves the company or has their personal device stolen, every single person sharing that password is at risk.

Remediation: We need to issue unique, individual user accounts for every single employee immediately. To stop the habit of sharing passwords (which usually happens just to make workflows faster), we should deploy an enterprise password manager. This will allow teams to securely share access to specific tools without ever actually seeing or typing the raw credentials.

### 2. Default Administrator Password on the Database
The Risk: During the inspection, I found that the administrative account for our primary customer database is still running on its factory-default password. This is the most likely entry point for the recent breach. Attackers use automated scripts that constantly scan the internet for databases using default credentials. Because this password was never changed, gaining access to our entire customer PII database was trivial for the attackers.

Remediation: The database admin password must be changed immediately. Following that, we need to enforce a strict, OS-level password policy that requires long, complex passwords and prevents password recycling. We also need to restrict database admin access so it can only be accessed from specific, authorized management servers, not directly from the open internet.


### 3. Unrestricted Firewall Traffic (No Filtering Rules)
The Risk: Our firewalls are currently configured to pass all traffic without inspection. They are essentially acting as expensive routers rather than security controls. Because we have no rules filtering inbound traffic, attackers can easily reach any exposed port on our network. More importantly, because we have no outbound (egress) filtering, when the attackers stole the customer data, the firewall didn't stop the data from leaving our network. 

Remediation: We need to reconfigure our firewalls using a "default deny" posture. This means all traffic is blocked unless we explicitly create a rule allowing it. 
* Inbound: We will only open the specific ports required for the social media platform to function (e.g., 80, 443) and block everything else. 
* Outbound: We must implement egress filtering to ensure our internal servers can only communicate with known, trusted IP addresses. If an attacker gets in again, outbound filtering will prevent them from exfiltrating the database to their own servers.
* Perimeter Monitoring (IDPS): To provide an active layer of defense, I strongly recommend deploying an Intrusion Detection and Prevention System (IDPS) across our network perimeter. This system will continuously monitor all network traffic in real-time to instantly identify and block known attack signatures or suspicious behavioral anomalies. By actively dropping malicious packets before they reach our internal systems, the IDPS acts as a critical safety net to stop future exploits in their tracks.

### 4. Complete Lack of Multifactor Authentication (MFA)
The Risk: Right now, we are relying 100% on passwords to protect our most sensitive systems. Passwords can be guessed, phished, or stolen from an employee's browser. Without a second layer of verification, a stolen password is all an attacker needs to take over an account, access the database, and move laterally through our network.

Remediation: We need to roll out Multifactor Authentication (MFA) across the entire organization, starting immediately with all administrative accounts, database access, and remote network connections. We should use authenticator apps or hardware keys rather than SMS text codes, as they are much harder to intercept. Even if an attacker manages to steal an employee's password, MFA will stop them in their tracks because they won't have the physical second factor.

---

## My Final Submission
The recent breach was not the result of a highly sophisticated, zero-day exploit; it was the result of basic security hygiene failures. By addressing these four vulnerabilities including enforcing individual accounts, eliminating default passwords, properly configuring firewall rules, and mandating MFA, we can drastically reduce our attack surface. 

I recommend we treat these remediations as an emergency priority. I am ready to begin drafting the technical implementation plans for the firewall rules and MFA rollout as soon as this assessment is approved.

---

📄 [View Full Risk Assessment Document (PDF)](./security-risk-assessment-report.pdf)