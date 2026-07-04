# Practical Exercise: Identifying Attack Vectors of a USB Drive

Assessment Context: Scenario-Based Simulation (Google Cybersecurity Professional Certificate)  
Activity: Identify the attack vectors of a USB drive  
Case Study: Parking lot USB exercise  
Role Assumed: Security Analyst  

---

## Project Description
As part of the security team at a Hospital, I found a USB stick with the company logo in the parking lot one morning. Instead of plugging it directly into my workstation, I used virtualization software to safely investigate it in an isolated environment. This exercise walks through what I discovered on the drive and how I analyzed the potential attack vectors from both a defender's and an attacker's perspective.

---

## 1. Initial Discovery & Content Analysis
The drive contained Personally Identifiable Information (PII), including names, wedding dates, and financial details. However, what stood out was that it also contained work related documents mixed in with the personal data. Normally, personal details and professional documents are kept separate, but here they were sitting side by side.

Furthermore, since the USB appears to belong to someone in a resource management role, it likely contains sensitive information about colleagues as well. This makes the device a goldmine of personal and professional data, creating a severe confidentiality risk.

---

## 2. Threat Modeling: Thinking Like an Attacker
To properly assess the risk, I shifted my mindset. Instead of just cataloging what was on the drive, I asked myself: *"If I were a malicious threat actor, how could I use this?"*

* Social Engineering Toolkit: All this information provides an attacker with everything they need to craft highly convincing phishing emails or vishing (voice phishing) calls. They could reach out to a target saying, "Hey, I'm calling about your wedding gift registry," and the target would have no reason to doubt them because the details are real.
* The Bait Scenario: There is a strong possibility that the USB itself is a deliberate setup. The drive could be bait designed to get someone to plug it in, which then installs sophisticated malware or spyware on their system, giving the attacker a foothold in the hospital's network.

---

## 3. Identified Risk Vectors & Remediation
After analyzing the situation, I identified three major risk vectors and developed corresponding remediation strategies:

### A. Malicious Code Execution
* The Risk: This is the most immediate technical threat. Malicious code could be hidden on the device. When plugged into a computer, it could automatically execute, take over the system, and spread through the connected network. In a hospital environment, this is especially dangerous as it could compromise critical patient care systems.
* Remediation: We must disable auto-run features on all workstations and ensure robust endpoint protection is active. Most importantly, clear policies must forbid plugging in unknown drives, backed up by regular staff training.

### B. Identity Exploitation
* The Risk: If sensitive information like subscription details or financial data gets into the wrong hands, an attacker can use it to impersonate the owner or even incriminate them. An attacker could use financial details to make unauthorized transactions or access systems they shouldn't, making it look like the legitimate user did it.
* Remediation: Sensitive data should never be stored on unencrypted removable drives. We need to enforce strict data handling policies, encrypt files at rest, and monitor for any unusual access patterns to catch misuse early.

### C. Social Engineering Through Brand Trust
* The Risk: The USB has the hospital's logo on it, which immediately makes it look legitimate. An attacker could use this as a pretext to gain employees' trust, tricking them into plugging it into their workstations.
People see the company logo, assume the device belongs to a colleague, and lower their guard.
* Remediation: This comes down to training and culture. We need to run regular security awareness sessions that cover physical threats like USB drops, and establish a simple, unbreakable rule: If you find a drive, hand it to IT, do not plug it in.

---

## Summary
This parking lot USB exercise reinforced how physical security and cybersecurity are completely intertwined. Finding that USB wasn't just about curiosity; it was about recognizing a potential attack vector and handling it the right way. The biggest takeaway for me is that security isn't just about firewalls and antivirus software. It's about understanding human behavior, recognizing physical threats, and always asking questions before taking action.

---

📄 [View Full Strategy Document (PDF)](./parking-lot-USB-exercise.pdf)

---

*Note: This document outlines my hands-on practice in physical security assessment, threat modeling, and attack vector analysis required for comprehensive cybersecurity operations.*