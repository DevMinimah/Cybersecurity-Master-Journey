# TS Academy Cybersecurity: Module 03 - Defensive Security Operations (SOC & Incident Response)

## 📅 Date Started: 2026-07-01
## 📅 Date Completed: 2026-08-29

---

## 🎯 What I Learned

### 1. Security Operations Center (SOC) Fundamentals
- Explored the core purpose of a SOC: a centralized team responsible for continuous monitoring, detection, investigation, and response to cybersecurity threats to protect digital assets and ensure business continuity.
- Studied the three core components of a SOC:
  - *People:* Analysts (monitoring/detection), Engineers (infrastructure maintenance), and Incident Responders (containment/eradication).
  - *Process:* Policies (high-level rules), SOPs (step-by-step routine tasks), and Playbooks (scenario-based response guides).
  - *Technology:* The foundational tools enabling detection and response.
- Learned about different SOC structures (In-house, Outsourced/MSSP, Hybrid) and modern challenges like alert fatigue, the skills gap, and cloud complexity.
- Understood the evolution of modern SOCs from reactive, event-based monitoring to proactive, investigation-based operations utilizing AI clustering and exposure management.

### 2. The Incident Response (IR) Lifecycle
- Studied the structured, six-phase approach to handling cybersecurity incidents: Preparation, Detection & Analysis, Containment, Eradication & Recovery, and Lessons Learned.
- Learned the critical importance of evidence collection (logs, network data, malware samples) and maintaining clear internal/external communication and escalation protocols during an active incident.
- Practiced mapping real-world scenarios (e.g., phishing emails, malware detections) to the IR lifecycle to understand containment, eradication, and recovery workflows.

### 3. Alerts, IOCs, and Triage
- Explored the classification of incident alerts: True Positives (TP), False Positives (FP), True Negatives (TN), and False Negatives (FN), understanding how FP rates impact analyst efficiency.
- Studied the difference between Default (out-of-the-box) alerts and Custom (user-defined) alerts, and how alert severity (Critical, High, Medium, Low, Info) is calculated based on threat confidence, asset criticality, and attack stage.
- Learned to identify and categorize Indicators of Compromise (IOCs) across five domains: File-based, Network-based, Host-based, Email-based, and Behavioral.
- Understood the concept of IOC aging and the necessity of using online analysis tools (e.g., VirusTotal, AbuseIPDB, URLScan, Shodan, HaveIBeenPwned) to enrich and validate suspicious data points with external context.

### 4. The SOC Technology Stack
- Studied the roles of core defensive technologies:
  - *SIEM:* Centralizes, normalizes, and correlates logs to generate alerts (e.g., Microsoft Sentinel, Splunk, Elastic).
  - *EDR vs. XDR:* Understood how EDR monitors endpoint behavior, while XDR extends this visibility across endpoints, email, identity, network, and cloud workloads to correlate advanced attacks (e.g., Microsoft Defender XDR, CrowdStrike).
  - *SOAR:* Automates repetitive tasks and executes response playbooks via integrations (e.g., Azure Logic Apps, Cortex XSOAR).
  - *IDS/IPS:* Detects and blocks suspicious network traffic (e.g., Snort, Suricata, Zeek).
- Explored Vulnerability Management tools (e.g., Qualys, Nessus) and Ticketing systems (e.g., Jira, ServiceNow, TheHive) for tracking investigations and ensuring compliance.

### 5. Threat Intelligence & Frameworks
- Explored the sources of Threat Intelligence (OSINT, commercial feeds, internal telemetry, sharing communities) and the role of Threat Intelligence Platforms (TIPs) like MISP and OpenCTI in automating enrichment.
- Studied industry standards for sharing intelligence: STIX (structured language for describing threats) and TAXII (protocol for exchanging STIX data).
- Learned to map adversary behavior using foundational frameworks:
  - *MITRE ATT&CK:* A comprehensive knowledge base of attacker tactics and techniques.
  - *Cyber Kill Chain:* Describes the stages of an attack from reconnaissance to actions on objectives.
  - *Diamond Model of Intrusion Analysis:* Links the four core elements of an intrusion: Adversary, Infrastructure, Capability, and Victim.

---

## 💡 Key Takeaways

- **SOC is a Triad, Not Just Tools:** A successful SOC relies equally on skilled People, defined Processes (Playbooks/SOPs), and integrated Technology. Upgrading tools without tuning processes or training analysts only leads to alert fatigue.
- **Context is the Antidote to Alert Fatigue:** An IOC or alert is just a data point. Its true value is unlocked only when enriched with threat intelligence, asset criticality, and behavioral context to distinguish a True Positive from a False Positive.
- **XDR is the Natural Evolution of EDR:** Modern attacks rarely stay confined to a single endpoint. XDR's ability to correlate telemetry across identity, email, network, and cloud is essential for reducing investigation time and spotting multi-stage attacks.
- **Intelligence Drives Proactive Defense:** Frameworks like MITRE ATT&CK and the Diamond Model shift the analyst's mindset from merely reacting to alerts to proactively hunting for adversary TTPs and understanding the "who, what, and how" of an intrusion.

---

## 🔗 Links/Resources

- [MITRE ATT&CK Framework](https://attack.mitre.org/)
- [Lockheed Martin Cyber Kill Chain](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html)
- [The Diamond Model of Intrusion Analysis (PDF)](https://www.threatintel.com/diamond-model)
- [MISP (Open Source Threat Intelligence Platform)](https://www.misp-project.org/)
- [NIST Computer Security Incident Handling Guide (SP 800-61 Rev. 2)](https://csrc.nist.gov/publications/detail/sp/800-61/rev-2/final)
- [VirusTotal](https://www.virustotal.com/)
- [AbuseIPDB](https://www.abuseipdb.com/)
- [Have I Been Pwned](https://haveibeenpwned.com/)

---

*Note: This document represents knowledge consolidation, personal realization, and a mindset shift from passive user to active defender — foundational to my growth in cybersecurity operations.*

*🔙 [Back to TS Academy Cybersecurity](../README.md)*
