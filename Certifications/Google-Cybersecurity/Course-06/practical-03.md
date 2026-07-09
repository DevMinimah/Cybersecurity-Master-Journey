# Practical Activity: Phishing Incident Investigation and SOC Escalation

Activity: Malicious File Hash Investigation and Incident Triage  
Case Study: Financial Services Company Phishing & Malware Execution  
Environment: Simulated Security Operations Center (SOC)  
Role Assumed: Level 1 SOC Analyst  
Tools/Frameworks: VirusTotal, Pyramid of Pain, OSINT, Incident Response Playbook  

## Project Description
In a Security Operations Center, the first few minutes of an incident dictate the outcome. In this simulation, I acted as a Level 1 SOC analyst at a financial services company responding to a malware execution alert. An employee opened a password-protected spreadsheet from a phishing email, triggering a malicious payload. Following our standard incident response playbook, I analyzed the file hash using VirusTotal, mapped the threat actor's Tactics, Techniques, and Procedures (TTPs) using the Pyramid of Pain, and prepared a comprehensive escalation report for the Level 2 team. This exercise represents the critical bridge between initial detection and deep-dive incident response.

---

## Stage 1: Initial Triage and Alert Analysis
Before investigating the malware, I followed the playbook's initial triage steps to understand how the payload bypassed our defenses and what occurred on the endpoint. 

*   The Attack Vector: The employee received a phishing email containing a password-protected spreadsheet. The password was included in the email body.
*   The Bypass: By using a password-protected file, the attacker successfully bypassed automated email security filters, which cannot inspect the contents of encrypted attachments.
*   The Execution: The employee downloaded the file, entered the password, and opened it, immediately executing the malicious payload on their workstation.

---

## Stage 2: OSINT Investigation using VirusTotal
With the malicious file secured, I followed the investigation playbook to extract its cryptographic hashes and query global threat intelligence.

*   Hash Extraction: I generated the primary SHA256 hash (54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b) and noted the associated MD5 hash (287d612e29b71c90aa54947313810a25).
*   Threat Identification: A VirusTotal search revealed the file is known as Flagpro. 
*   Vendor Consensus: It was flagged by over 50 security vendors as a backdoor and trojan, heavily associated with Advanced Persistent Threat (APT) actors.

---

## Stage 3: Mapping to the Pyramid of Pain
As outlined in the playbook for threat classification, I mapped the discovered Indicators of Compromise (IoCs) to the Pyramid of Pain to understand the attacker's methodology and determine how difficult it would be for them to adapt if we blocked their tools.

*   Hash Values (Low Pain): The SHA256 and MD5 hashes are easy for the attacker to change by slightly modifying the malware code. Blocking these is a quick win but offers only temporary protection.
*   Network/Host Artifacts & IP/Domain (Moderate Pain): I identified the C2 Protocol, the malicious domain (http://org.misecure.com), and the IP address (108.77.126.100). Blocking these forces the attacker to acquire new infrastructure, which takes time and resources.
*   TTPs (High Pain): The malware's core behavior involves Command and Control (C2) and stealing web session cookies. Detecting and blocking these specific behaviors forces the attacker to fundamentally change their methodology.

---

## Stage 4: Incident Escalation to Level 2 SOC
Following the escalation procedures in the playbook, I prepared to hand off the incident. Because Flagpro is linked to APT actors and exhibits active C2 behavior, this required Level 2 intervention.

*   Contextualized Handoff: I provided the Level 2 team with the complete IoC list, the Pyramid of Pain mapping, and the APT classification.
*   Requested Actions: I specifically asked them to perform deep-dive endpoint forensics, hunt network logs for the C2 IP and domain to check for lateral movement, and analyze if web session cookies were successfully exfiltrated.

---

## Investigation Artifacts
Below are the detailed documents, logs, and reports generated during this investigation:

*   [File Hash Investigation & Pyramid of Pain](file-hash-investigation-pyramid-of-pain.pdf)
*   [Malicious Email Alert Ticket](malicious-email-alert-ticket.pdf)
*   [Incident Handler's Journal](class-incident-handler's-journal.pdf)

---

## Summary
This phishing investigation reinforced several core principles of SOC operations that I carry forward in my career. First, it highlighted how attackers continuously evolve to bypass automated filters by shifting the vulnerability to the human element through social engineering. Second, it proved that shared threat intelligence is a massive force multiplier; I didn't have to reverse-engineer the binary from scratch because the global community had already fingerprinted it. Third, mapping IoCs to the Pyramid of Pain taught me that not all indicators are created equal understanding an attacker's TTPs allows us to build behavioral detections that inflict long-term pain on the threat actor, rather than just playing whack-a-mole with easily changed hashes. Finally, this exercise reinforced that a Level 1 analyst's job isn't just to close tickets, but to enrich them. A well-documented, thoroughly investigated escalation saves the Level 2 team hours of repetitive triage.

What excites me most about this work is the continuous learning it demands. Every new hash, C2 domain, and TTP adds to my mental library of how adversaries operate. I am continually refining my ability to not just spot anomalies, but to understand the "who, what, and why" behind them. The organizations that survive modern cyber threats rely on analysts who can seamlessly connect the initial dots and empower the broader team to finish the picture. That is the standard of work I am committed to delivering.


---

*Note: This document outlines my hands-on practice and learning proficiency in phishing incident triage, OSINT investigation, threat intelligence mapping using the Pyramid of Pain, and SOC escalation procedures required for cybersecurity operations.*