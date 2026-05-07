# Module 04: Vulnerability Management - Practical Activity

## 📅 Date Started: 2026-05-06
## 📅 Date Completed: 2026-05-07

## 🧪 Activity Type:
Scenario-based professional simulation: Acting as a security analyst to analyze threat intelligence using STIX and perform penetration testing on a web application using OWASP ZAP for an online retail organization.

## 🎯 Lab Goal:
To analyze threat intelligence data using STIX (Structured Threat Information Expression) for standardized threat sharing, and conduct vulnerability assessments on a web application using OWASP ZAP to identify, categorize, and report security risks by severity level.

## 🛠 Tools Used:
- STIX threat intelligence framework
- OWASP ZAP (Zed Attack Proxy) v2
- Web application vulnerability scanner
- Risk categorization matrix (High/Medium/Low/Informational)

## 📋 What I Did:
1. Analyzed threat intelligence from a case study to understand threat actor tactics, techniques, and procedures (TTPs) using structured data formats.
2. Explored STIX (Structured Threat Information Expression) as a standardized language for representing, storing, and sharing cyber threat intelligence across organizations.
3. Analyzed STIX expressions to identify indicators of compromise (IOCs), attack patterns, and threat actor relationships in machine-readable format.
4. Performed simulated penetration testing on an online retail organization's web application using OWASP ZAP v2 to identify security vulnerabilities.
5. Explored the OWASP ZAP interface, configured scan policies, and executed automated vulnerability scans against the target web application.
6. Analyzed scan results to identify vulnerabilities, categorize them by risk level (High, Medium, Low, Informational), and document findings in a penetration testing report format.

## 🔍 What I Found:
- Threat Intelligence & STIX: STIX provides a standardized, machine-readable format for sharing threat intelligence, enabling automated detection and response. It structures information about threat actors, campaigns, indicators, and attack patterns, making it easier for organizations to collaborate and defend against common threats.
- STIX Expressions: STIX objects (Indicators, Observables, Malware, Attack Patterns) can be linked together to create comprehensive threat narratives. Analyzing these expressions revealed relationships between IOCs (IP addresses, domains, file hashes) and specific threat actor behaviors.
- OWASP ZAP Capabilities: As an open-source DAST (Dynamic Application Security Testing) tool, OWASP ZAP successfully identified common web vulnerabilities including SQL injection, XSS (Cross-Site Scripting), security misconfigurations, and information disclosure issues in the retail web application.
- Risk Categorization: Vulnerabilities must be prioritized by severity:
  - High: Critical flaws requiring immediate remediation (e.g., SQL injection, authentication bypass)
  - Medium: Significant risks needing prompt attention (e.g., weak encryption, missing security headers)
  - Low: Minor issues with limited impact (e.g., verbose error messages, cookie flags)
  - Informational: Best practice recommendations for hardening (e.g., server version disclosure)
- Penetration Testing Value: Automated scanning with OWASP ZAP provides rapid vulnerability identification, but results require manual verification to eliminate false positives and assess business impact accurately.

## 💡 What I Learned:
- Threat intelligence standardization (STIX) is critical for effective information sharing between organizations, security vendors, and CERTs, enabling faster detection and response to emerging threats.
- Structured threat data allows for automation—security tools can ingest STIX feeds to automatically update detection rules, block malicious IPs, and identify compromised systems.
- Penetration testing is a proactive security control that identifies vulnerabilities before attackers exploit them; regular testing is essential for maintaining security posture.
- OWASP ZAP is an essential tool for web application security testing, providing both automated scanning and manual testing capabilities aligned with OWASP Top 10 vulnerabilities.
- Risk categorization and clear reporting are as important as finding vulnerabilities—stakeholders need prioritized, actionable findings to allocate remediation resources effectively.
- The penetration testing lifecycle (reconnaissance, scanning, exploitation, reporting) mirrors real attacker behavior, helping organizations understand their exposure from an adversary's perspective.

## 📸 Screenshot: