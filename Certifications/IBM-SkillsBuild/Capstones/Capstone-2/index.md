# Capstone 2: Perform an Impact Analysis to Address Vulnerabilities
## 🏢 Capital Ink Publishing - Cybersecurity Risk Assessment

> 🎓 Simulation-Based Capstone Project  
> *This assessment was completed as part of the IBM SkillsBuild Cybersecurity Certificate program. Capital Ink Publishing is a simulated digital publishing scenario created for educational purposes. All findings, recommendations, and artifacts demonstrate applied learning of vulnerability analysis, impact assessment, and risk mitigation.*

---

## 🎯 Challenge
Conduct a comprehensive cybersecurity risk assessment for a digital publishing company, identifying vulnerabilities, analyzing threats, assessing business impacts, and prioritizing mitigation strategies using industry frameworks.

---

## 🛠️ Tools & Frameworks Used
- OWASP ZAP (Vulnerability Scanning)
- CVSS 3.0 (Vulnerability Scoring)
- IBM X-Force Exchange (Threat Intelligence)
- NIST Cybersecurity Framework
- Industry Best Practices

---

## 🔍 Key Vulnerabilities Identified

| Vulnerability | Type | CVSS Score | Risk Level |
| Active Malware Infection | Data Exfiltration | 9.8 | 🔴 Critical |
| Unauthorized Database Access | Access Control | 7.5 | 🔴 High |
| Cross-Site Scripting (XSS) | Injection | 6.1 | 🟠 High |
| Cross-Site Request Forgery (CSRF) | Session Management | 6.5 | 🟠 High |
| Cloud Metadata Exposure | Misconfiguration | 5.3 | 🟡 Moderate |
| Missing Security Headers | Configuration | 4.3 | 🟡 Moderate |

---

## 📊 Impact Analysis

### Network Integrity Impact
- Malware: Compromised workstations spreading laterally, corrupting network integrity
- Unauthorized Access: Attackers mapping network topology, bypassing segmentation

### Business Continuity Impact
- Operational: Potential system downtime, extended recovery time
- Financial: Lost productivity, incident response costs, revenue loss
- Reputation: Loss of customer trust from credential theft

### Data Security Impact
- Confidentiality: CRITICAL - Active theft of unpublished manuscripts, customer PII, financial records
- Compliance: Potential GDPR/CCPA violations, legal notification requirements
- Integrity: Attackers performing unauthorized actions via session hijacking

---

## 🎯 Skills Demonstrated

✅ Evaluate Organizational Security
- Assessed current security posture across web applications, databases, and cloud infrastructure
- Identified gaps in technical, administrative, and operational controls

✅ Analyze Cybersecurity Threat Impact
- Evaluated effects on network integrity, business continuity, and data security
- Assessed confidentiality, integrity, and availability (CIA) impacts

✅ Categorize Vulnerabilities by Severity
- Applied CVSS 3.0 scoring framework
- Prioritized using risk-based approach (Critical → High → Moderate → Low)

✅ Justify Threat Mitigation Tactics
- Recommended technical, administrative, and operational controls
- Provided implementation timelines (24h, 1 week, 1 month, 3 months)
- Explained effectiveness and business rationale for each control

---

## 📤 Key Deliverables

✅ Comprehensive Risk Assessment Report
- Executive summary with critical findings
- Vulnerability identification using OWASP ZAP
- Threat intelligence analysis (IBM X-Force)

✅ Prioritized Mitigation Plan
- Immediate actions (24 hours): Malware containment, access control updates
- Short-term (1 week): MFA deployment, XSS remediation
- Medium-term (1 month): Security headers, employee training
- Long-term (3 months): Secure backups, architecture review

✅ Security Controls Framework
- Technical controls (Antivirus, WAF, Encryption)
- Administrative controls (Policies, Training, Audits)
- Operational controls (Monitoring, Patch Management)

✅ Implementation Roadmap
- Prioritized timeline with clear rationales
- Resource requirements and success metrics
- KPIs for ongoing measurement

---

## 💡 What I Learned
This capstone reinforced that vulnerability management is about risk-based prioritization, not just finding bugs. 

Key insights:
- Active threats demand immediate response: Malware with data exfiltration capabilities requires containment within 24 hours, not weeks
- Business context matters: A "moderate" CVSS score can be critical if it affects core revenue systems or customer trust
- Defense-in-depth is essential: No single control is sufficient; technical, administrative, and operational controls must work together
- Communication is critical: Executive summaries and clear timelines help leadership allocate resources effectively

Most importantly, I learned that security assessments aren't just technical exercises they're business continuity tools that protect customer data, intellectual property, and organizational reputation.

---

## 🏆 Official Microcredential

| Field | Details |
| Credential | IBM SkillsBuild: Vulnerability Management |
| Issued | May 08, 2026 |
| Credential ID | 173b0ebb-a010-4f62-8c83-54e8def38ffb |
| Verify | [🔗 View on Credly](https://www.credly.com/badges/173b0ebb-a010-4f62-8c83-54e8def38ffb/public_url) |

### Badge Display
![IBM SkillsBuild Badge](../../Assets/badges/vulnerability-management.png)

> ℹ️ *This capstone was completed in a controlled simulation environment. Proprietary simulation materials are not shared publicly per IBM SkillsBuild policy. This report and the official microcredential serve as verified proof of competency.*

---
*🔙 [Back to IBM SkillsBuild Dashboard](../../index.md)*