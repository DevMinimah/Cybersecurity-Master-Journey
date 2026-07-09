# Course 06: Sound the Alarm: Detection and Response

## 📅 Date Started: 2026-07-04
## 📅 Date Completed: 2026-07-09

---

## 🎯 What I Learned

### 1. Incident Response (IR) Frameworks & Team Roles
- Explored the NIST Incident Response Lifecycle, studying its four critical phases: Preparation; Detection and Analysis; Containment, Eradication, and Recovery; and Post-incident activity.
- Learned how to apply the "5 W's" (Who, What, Where, When, Why) to effectively analyze and document security incidents.
- Studied the structure of Computer Security Incident Response Teams (CSIRT), understanding the distinct roles of the Security Analyst, Technical Lead, and Incident Coordinator.
- Understood the hierarchy of a Security Operations Center (SOC), exploring the progression and responsibilities of SOC Analyst Tier 1 (L1), Tier 2 (L2), Tier 3 (L3), and the SOC Manager.

### 2. IR Tools, Documentation & Playbooks
- Learned the critical importance of documentation in IR for ensuring transparency, standardization, and clarity.
- Studied the Chain of Custody form, understanding how accurate logging establishes proof of integrity, reliability, and accuracy for legal proceedings.
- Explored the different types of IR playbooks (non-automated, semi-automated, and automated) and how they guide standardized responses to specific threats.
- Understood the role of various documentation and investigative tools, including ticketing systems, word processors, and the incident handler's journal.

### 3. Detection Technologies: IDS, IPS & EDR
- Explored Intrusion Detection and Prevention Systems (IDS/IPS), studying tools like Snort, Zeek, Suricata, and Kismet.
- Learned the difference between Host-based (HIDS) and Network-based (NIDS) intrusion detection systems, as well as signature-based vs. anomaly-based detection techniques.
- Studied Endpoint Detection and Response (EDR) tools (e.g., Open EDR, Bitdefender, FortiEDR) for continuous endpoint monitoring.
- Understood the four detection categories used to evaluate alert accuracy: True Positive, True Negative, False Positive, and False Negative.

### 4. Network Monitoring & Packet Analysis
- Learned how to monitor network traffic by establishing baselines, performing flow analysis, and identifying temporal patterns and Indicators of Compromise (IoCs).
- Studied the anatomy of a network packet (Header, Payload, Footer) and explored packet capture libraries and formats (Libpcap, Npcap, PCAPng).
- Explored the detailed fields of IPv4 headers (13 fields, including TTL, Protocol, Source/Destination) and IPv6 headers (8 fields, including Traffic Class, Flow Label, Hop Limit).
- Practiced packet capture and analysis using protocol analyzers like Wireshark and command-line tools like tcpdump.

### 5. SIEM, SOAR & Log Management
- Understood the SIEM (Security Information and Event Management) process: collection/aggregation, data normalization, and analysis.
- Studied log management practices, including log types (network, system, application, security, authentication), retention policies driven by regulations (HIPAA, PCI DSS, FISMA), and log protection.
- Explored common log formats such as Syslog, JSON, XML, CSV, and Common Event Format (CEF).
- Learned how to query and analyze logs using Splunk's Search Processing Language (SPL) and Google SecOps (formerly Chronicle) using UDM and raw log searches.
- Understood Security Orchestration, Automation, and Response (SOAR) and its role in streamlining SOC workflows.

### 6. Threat Hunting, Intelligence & The Pyramid of Pain
- Explored proactive detection methods like Threat Hunting and Cyber Deception (Honeypots).
- Studied Threat Intelligence sources, including industry reports, government advisories, and threat data feeds for tracking Advanced Persistent Threats (APTs).
- Learned the "Pyramid of Pain" framework, understanding the difficulty for attackers to change different IoCs: Hash values, IP addresses, Domain names, Network/Host artifacts, Tools, and Tactics, Techniques, and Procedures (TTPs).
- Analyzed IoCs using OSINT and investigative tools like VirusTotal, Urlscan, Jotti's Malware Scan, and MalwareBazaar.

### 7. Securing CI/CD Pipelines
- Explored the ongoing monitoring of CI/CD pipelines to detect specific IoCs, such as unauthorized code changes, suspicious deployment patterns, compromised dependencies, and secrets exposure.
- Studied how to use automation, comprehensive logging, and SIEM integration to proactively find anomalies, trigger real-time alerts, and limit damage in the software delivery pipeline.

### 8. Triage, Business Continuity & Post-Incident Activity
- Learned the incident triage process: receiving/assessing the incident, assigning priority based on functional impact, information impact, and recoverability, and collecting/analyzing data.
- Understood Business Continuity Planning (BCP) and studied the three types of recovery sites for site resilience: Hot sites, Warm sites, and Cold sites.
- Explored the critical role of the post-incident review meeting to answer key questions (what happened, how it was contained, what could be improved) to strengthen future defenses.

---

## 💡 Key Takeaways

- Detection is a Layered Discipline: Effective detection requires a combination of network monitoring (NIDS/pcap), endpoint visibility (EDR), and centralized log analysis (SIEM). No single tool can catch every threat.
- The Pyramid of Pain is a Strategic Mindset: While it's easy to block a malicious IP or hash, true security maturity comes from detecting the attacker's TTPs (Tactics, Techniques, and Procedures), which forces them to completely change their behavior.
- Logs are the Lifeblood of the SOC: Without proper log ingestion, normalization, and retention (complying with frameworks like Syslog or JSON), a SIEM is useless. Knowing how to query these logs (via SPL or UDM) is a core analyst skill.
- CI/CD is a Critical Attack Surface: As development accelerates, so do the risks. Monitoring pipelines for anomalous code changes, unauthorized deployments, and exposed secrets is just as important as monitoring the production network.
- Incident Response is Cyclical, Not Linear: The NIST lifecycle emphasizes that "Post-incident activity" is just as crucial as containment. Learning from the breach via thorough documentation and post-incident reviews is how organizations actually improve their security posture.

---

## 🔗 Links/Resources:

Core Certification & SOC Operations:
- [Google Cybersecurity Professional Certificate](https://www.coursera.org/professional-certificates/google-cybersecurity)
- [CISA Cyber Career Pathways Tool](https://niccs.cisa.gov/workforce-development/cyber-career-pathways-tool)
- [Chronicle SOC Ecosystem Infographic](https://chronicle.security/blog/posts/soc-ecosystem-infographic/)
- [YouTube: The SOC Ecosystem Explained](https://www.youtube.com/watch?v=QZ0cpBocl3c)

OSINT & Investigative Tools:
- [VirusTotal](https://www.virustotal.com/gui/home)
- [Urlscan](https://urlscan.io/)
- [Jotti's Malware Scan](https://virusscan.jotti.org/)
- [MalwareBazaar](https://bazaar.abuse.ch/browse/)

Network Monitoring & Packet Analysis:
- [tcpdump Official Manual & Examples](https://www.tcpdump.org/)
- [Daniel Miessler: tcpdump Guide](https://danielmiessler.com/p/tcpdump/)
- [Infosec Institute: Packet Crafting](https://www.infosecinstitute.com/resources/hacking/packet-crafting-a-serious-crime/)
- [MITRE ATT&CK Datasources](https://attack.mitre.org/datasources/DS0029/)
- [MITRE ATT&CK Tactics](https://attack.mitre.org/tactics/TA0010/)

Threat Hunting & Intelligence:
- [ThreatHunting.net](https://www.threathunting.net/)
- [Google Threat Analysis Group (TAG) Blog](https://blog.google/threat-analysis-group/)
CI/CD & DevSecOps Security:
- [Splunk: CI/CD & DevOps Pipelines Introduction](https://www.splunk.com/en_us/blog/learn/ci-cd-devops-pipeline.html)
- [What is CI/CD? - Threat Intelligence Blog](https://www.threatintelligence.com/blog/continuous-integration-continuous-delivery)
- [Coralogix: Optimizing logs for a more effective CI/CD pipeline](https://coralogix.com/blog/optimizing-logs-for-a-more-effective-ci-cd-pipeline/)
- [Axiom.io: Implementing AI in CI/CD Pipelines](https://blog.axiomio.com/implementing-ai-in-ci-cd-pipelines-a-practical-guide-83466035e3c7)

Intrusion Detection (Suricata):
- [Suricata Official Documentation](https://suricata.readthedocs.io/en/latest/index.html#)
- [Suricata Features Overview](https://suricata.io/features/)
- [Suricata Update & Rule Management](https://suricata.readthedocs.io/en/latest/rule-management/suricata-update.html)
- [Suricata YAML Configuration & Profiling](https://suricata.readthedocs.io/en/latest/configuration/suricata-yaml.html#engine-analysis-and-profiling)
- [Suricata EVE JSON Output Examples](https://suricata.readthedocs.io/en/latest/output/eve/eve-json-examplesjq.html)
- [YouTube: Suricata Tutorial Part 1](https://youtu.be/kaDGolhTu94)
- [YouTube: Suricata Tutorial Part 2](https://youtu.be/tvoqFBVSShA)

SIEM Tools (Splunk & Google SecOps/Chronicle):
- [Splunk: How to Add Data](https://docs.splunk.com/Documentation/SplunkCloud/9.0.2303/Data/Howdoyouwanttoadddata)
- [Splunk: Getting Started with Search](https://docs.splunk.com/Documentation/Splunk/9.0.1/Search/GetstartedwithSearch)
- [Splunk: Understanding SPL Syntax](https://docs.splunk.com/Documentation/Splunk/9.0.2/SearchReference/UnderstandingSPLsyntax)
- [Google SecOps (Chronicle): Data Ingestion Flow](https://cloud.google.com/chronicle/docs/data-ingestion-flow)
- [Google SecOps (Chronicle): UDM Field List](https://cloud.google.com/chronicle/docs/reference/udm-field-list)
- [Google SecOps (Chronicle): Review Security Alerts](https://cloud.google.com/chronicle/docs/review-security-alert)

Protocols & Standards:
- [Syslog Protocol RFC 5424](https://www.rfc-editor.org/rfc/rfc5424)

---

🎓 Google Cybersecurity Professional Certificate | Course 6 of 8
