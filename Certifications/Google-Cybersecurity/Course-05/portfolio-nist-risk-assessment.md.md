# Portfolio Project: NIST SP 800-30 Rev. 1 Risk Assessment for Public-Facing Database

Assessment Context: Scenario-Based Simulation (Google Cybersecurity Professional Certificate)  
Activity: Vulnerability and Risk Assessment (NIST SP 800-30 Rev. 1)  
Environment: E-commerce Company / Remote Database Infrastructure  
Role Assumed: Cybersecurity Analyst  
Tools/Framework: NIST SP 800-30 Rev. 1, Risk Assessment Matrix, Network Segmentation Principles  

---

## Executive Summary
As a newly hired cybersecurity analyst for a global e-commerce company, I identified a critical architectural flaw: the core MySQL database server had been publicly accessible via IPv4 for three years. To communicate this risk to executive decision-makers, I conducted a formal risk assessment aligned with the NIST SP 800-30 Rev. 1 framework. By evaluating threat sources, likelihood, and business impact, I quantified the severe risks of data exfiltration and service disruption. I ultimately delivered a strategic remediation plan to secure the infrastructure, enforce least-privilege access, and maintain seamless business continuity.

---

## 1. System Description and Scope
To establish the baseline for the risk assessment, I first documented the system architecture and defined the boundaries of the evaluation.

* System Description: The target system is a high-performance remote database server (128GB RAM, latest Linux OS) hosting a MySQL database management system. It utilizes IPv4 addressing for network interactions and currently relies on SSL/TLS for encrypted connections.
* Scope: The assessment focused strictly on the current access controls and network exposure of the system. The evaluation period covered a three-month window (April 2026 to June 2026) to analyze potential threat vectors against the publicly exposed server.

---

## 2. Purpose and Business Impact
The primary purpose of this assessment was to evaluate the risks associated with the database's public-facing posture. The server houses the main operational data for the business, including highly sensitive information belonging to customers and business partners. 

I identified three critical business impacts if the server remains unprotected:
1. Confidentiality Loss: A breach could lead to the leakage of sensitive customer and partner data.
2. Integrity Loss: Unauthorized actors could alter or destroy critical business records.
3. Availability Loss: If the server is attacked or disabled, it would disrupt the services rendered to users and partners, causing them to seek alternative solutions and resulting in direct revenue loss.

---

## 3. Risk Assessment (NIST SP 800-30 Rev. 1)
Following the NIST SP 800-30 Rev. 1 methodology, I identified threat sources, determined the likelihood of threat events occurring, and assessed the severity of their impact on the organization's operations and assets. 

*Note: Likelihood and Severity are rated on a qualitative scale of 1 (Low) to 3 (High).*

| Threat Source | Threat Event Description | Likelihood (1-3) | Severity (1-3) | Risk Level |
| :--- | :--- | :---: | :---: | :---: |
| Malicious Insider (Employee) | Exfiltration of sensitive company data or altering records, potentially masking the attack to look like an external breach due to the server's public access. | 2 | 3 | High |
| External Threat Actor (Hacker) | Conducting reconnaissance and surveillance on business operations and data movements to identify vulnerabilities for exploitation. | 3 | 3 | High |
| Competitor | Directly connecting to the public IP address to query the database and silently scrape or download proprietary information (client lists, pricing models, strategies). | 2 | 3 | High |

Approach: This evaluation analyzed the organization's data handling and storage architecture. By measuring both the likelihood and severity of potential threats, I ensured that security considerations were balanced with the necessity of maintaining seamless daily business continuity.

---

## 4. Remediation Strategy and Risk Treatment
To mitigate the identified risks to an acceptable level, I developed a comprehensive remediation strategy divided into immediate network controls and long-term defense-in-depth measures.

### Immediate Network Remediation
* Block Public Access: Reconfigure the network firewall and cloud security groups to deny all inbound internet traffic to the database port.
* Network Segmentation: Relocate the database server to a private, internal network segment, completely isolating it from the public internet.
* Secure Remote Administration: If remote access is required for administration, route it strictly through a secure Virtual Private Network (VPN) or a dedicated Bastion host. The database must never possess a direct public-facing IP address.

### Long-Term Defense-in-Depth
* Strict Access Controls: Enforce the principle of least privilege by implementing Role-Based Access Control (RBAC) and disabling all default administrative accounts.
* Identity Verification: Enforce Multi-Factor Authentication (MFA) for all database access to prevent credential compromise.
* Continuous Monitoring: Enable comprehensive audit logging and integrate it with a Security Information and Event Management (SIEM) system. This will allow the security team to detect and respond to unauthorized connection attempts or anomalous queries in real time.

---

## Summary
Through this risk assessment, I successfully translated a critical technical vulnerability of a publicly exposed database a into clear, actionable business risks for executive decision-makers. By applying the NIST SP 800-30 Rev. 1 framework, I was able to systematically identified insider and external threats, quantified their likelihood and severity, and provided a robust, multi-layered remediation strategy. This exercise demonstrates my ability to conduct formal risk assessments, align technical security controls with business objectives, and protect critical organizational assets from catastrophic data breaches.

---

📄 [View Full Strategy Document (PDF)](./vulnerability-assessment-report.pdf)


*Note: This document outlines my hands-on practice and learning proficiency in risk assessment frameworks, vulnerability analysis, security governance, and business-aligned security controls required for cybersecurity operations.*