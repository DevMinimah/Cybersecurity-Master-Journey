# TS Academy Cybersecurity: Module 04 - Offensive Security & Vulnerability Management

## 📅 Date Started: 2026-09-03
## 📅 Date Completed: 2026-09-26

---

## 🎯 What I Learned

### 1. Foundations of Ethical Hacking & Pre-Engagement
- Explored the critical distinction between ethical hacking (the broad craft of thinking like an attacker to find weaknesses) and penetration testing (a specific, time-boxed, authorized project with a defined scope and report).
- Studied the absolute necessity of written authorization, defining strict scope, and establishing Rules of Engagement (RoE) to ensure all activities remain lawful, safe, and professionally bounded.
- Learned to build secure, isolated virtual machine labs (e.g., Kali Linux as the attacker, DevGuru/Metasploitable as the target) using NAT networking and VM snapshots to safely experiment without risking production environments.
- Practiced essential Linux command-line operations for navigation (`cd`, `pwd`, `ls`), file management (`cp`, `mv`, `rm`), permissions (`chmod`, `sudo`), and network verification (`ip a`, `ping`).

### 2. Reconnaissance & OSINT (Open-Source Intelligence)
- Studied the difference between passive reconnaissance (gathering public data without touching the target, leaving no trace) and active reconnaissance (interacting with the target, which requires explicit permission).
- Learned footprinting techniques to map the attack surface, including analyzing DNS records (A, MX, NS, TXT), WHOIS registration data, IP ranges/ASNs, and technology stack fingerprinting.
- Explored advanced search techniques like Google Dorking (using operators like `site:`, `filetype:`, `inurl:`) to uncover exposed directories, configuration files, and forgotten login portals.
- Understood how to leverage Shodan to identify internet-exposed devices, services, and open ports by querying its database rather than scanning the target directly.
- Practiced core OSINT disciplines: email intelligence (predicting naming patterns), SOCMINT (social media intelligence), breach data analysis, and username enumeration using tools like `theHarvester`, `Sherlock`, and `Holehe`.

### 3. Active Scanning, Enumeration & Vulnerability Management
- Studied the continuous vulnerability management lifecycle: Discover, Assess, Prioritize, Remediate, and Verify.
- Learned to perform active network scanning using tools like Nmap to identify live hosts, determine port states (open, closed, filtered), and perform version detection and OS fingerprinting.
- Explored automated vulnerability scanners (e.g., OpenVAS, Nessus, Qualys) and understood the critical difference between unauthenticated scans (outside attacker view, higher false positives) and authenticated scans (inside view, deeper visibility, fewer false positives).
- Understood how to triage scanner results by identifying false positives, merging duplicates, and prioritizing genuine findings using CVE (Common Vulnerabilities and Exposures) identifiers and CVSS (Common Vulnerability Scoring System) severity scores (0.0 to 10.0).

### 4. Exploitation & Post-Exploitation
- Learned the core mechanics of exploitation: utilizing an exploit (the technique) to deliver a payload (the code) and gain a shell (interactive command-line access).
- Studied the difference between bind shells (target listens for incoming connection, often blocked by firewalls) and reverse shells (target connects back to the attacker, bypassing inbound firewall restrictions).
- Explored post-exploitation techniques, including privilege escalation (moving from a low-privileged user to root/admin), lateral movement (spreading to other machines), pivoting (using a compromised host as a bridge), and establishing persistence.
- Understood password security concepts, including how systems store one-way cryptographic hashes and the methodologies behind password cracking (e.g., brute force, dictionary attacks).

### 5. Web Application Security & The OWASP Top 10
- Studied fundamental web architecture (Browser ↔ Server ↔ Database) and the critical role of an intercepting proxy (e.g., Burp Suite) in viewing, intercepting, and modifying HTTP requests and responses.
- Explored the OWASP Top 10 critical web vulnerabilities, including:
  - *Injection (e.g., SQLi):* When untrusted user input is executed as a database command rather than treated as data.
  - *Broken Access Control (e.g., IDOR):* When users can access or modify data belonging to other users by manipulating object identifiers.
  - *Cross-Site Scripting (XSS):* When malicious scripts are injected into a webpage and executed in a victim's browser.
  - *Sensitive Data Exposure & Security Misconfiguration:* Unprotected files, default credentials, or missing security headers.

### 6. Threat Intelligence & Incident Response Context
- Explored the sources of Threat Intelligence (OSINT, commercial feeds, internal telemetry, sharing communities) and the role of Threat Intelligence Platforms (TIPs) like MISP and OpenCTI in automating enrichment.
- Studied industry standards for sharing intelligence: STIX (structured language for describing threats) and TAXII (protocol for exchanging STIX data).
- Learned to map adversary behavior using foundational frameworks:
  - *MITRE ATT&CK:* A comprehensive knowledge base of attacker tactics and techniques.
  - *Cyber Kill Chain:* Describes the stages of an attack from reconnaissance to actions on objectives.
  - *Diamond Model of Intrusion Analysis:* Links the four core elements of an intrusion: Adversary, Infrastructure, Capability, and Victim.
- Understood the Incident Response lifecycle (Preparation, Detection & Analysis, Containment, Eradication & Recovery, Lessons Learned) and how to classify and analyze Indicators of Compromise (IOCs) across file, network, host, email, and behavioral domains using tools like VirusTotal and AbuseIPDB.

### 7. Professional Reporting & Documentation
- Learned that the penetration test report is the ultimate deliverable, serving two distinct audiences: leadership (executive summary focusing on business risk and high-level recommendations) and technical teams (detailed findings with reproduction steps and specific fixes).
- Studied how to structure a single, professional finding: Title, Severity (calculated via Likelihood × Impact), Description, Evidence (screenshots/steps), Business Impact, and actionable Remediation.
- Understood the importance of maintaining an objective, factual, and constructive tone to ensure findings are trusted, understood, and acted upon by the client.

---

## 💡 Key Takeaways

- **Permission is the Absolute Boundary:** The exact same technical action is a highly paid, lawful profession on an authorized network, and a serious crime on an unauthorized one. Written authorization and strict scope are non-negotiable.
- **Triage is the Analyst's Superpower:** Automated scanners generate noise. The true value of a security professional lies in their ability to filter out false positives, validate genuine risks, and prioritize remediation based on real-world exploitability and business context, not just raw CVSS scores.
- **Obscurity is Not Security:** Hiding a URL (like an admin panel or score board) does not protect it. True security requires server-side authorization checks for every request, regardless of whether the endpoint is publicly advertised.
- **The Report is the Product:** A brilliant technical exploit is worthless to a business if it cannot be clearly communicated. The ability to translate technical findings into business risk and actionable remediation is what builds long-term trust and career success.
- **Never Trust User Input:** The underlying pattern behind almost all web vulnerabilities (SQLi, XSS, Command Injection) is the application trusting and executing unvalidated data from the user. Input validation and output encoding are the foundational defenses.

---

## 🔗 Links/Resources

- [OWASP Top 10 Web Application Security Risks](https://owasp.org/www-project-top-ten/)
- [MITRE ATT&CK Framework](https://attack.mitre.org/)
- [NIST Vulnerability Management Guidelines (SP 800-40)](https://csrc.nist.gov/publications/detail/sp/800-40/rev-4/final)
- [Common Vulnerabilities and Exposures (CVE) Search](https://cve.mitre.org/)
- [National Vulnerability Database (NVD) & CVSS](https://nvd.nist.gov/)
- [Shodan: The Search Engine for the Internet of Things](https://www.shodan.io/)
- [Google Hacking Database (GHDB) by Exploit-DB](https://www.exploit-db.com/google-hacking-database)
- [TryHackMe: Vulnerability Scanning Tools](https://tryhackme.com/room/vulnerabilityscanningtools)
- [Have I Been Pwned (Breach Data)](https://haveibeenpwned.com/)
- [VirusTotal (IOC Analysis)](https://www.virustotal.com/)
- [AbuseIPDB (IP Reputation)](https://www.abuseipdb.com/)

---

**🎓 TS Academy Cybersecurity Program | Module 04: Offensive Security & Vulnerability Management**

---

*Note: This document represents knowledge consolidation, personal realization, and a mindset shift from passive user to active defender — foundational to my growth in cybersecurity operations.*

*🔙 [Back to TS Academy Cybersecurity](../README.md)*
