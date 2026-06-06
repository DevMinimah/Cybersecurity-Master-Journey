# Security Compliance & Controls Audit | Toy Manufacturing & Retail Sector

## 🎯 Executive Summary
Conducted a comprehensive enterprise security audit for a mid-size toy production and retail organization. Evaluated technical controls, administrative policies, and regulatory compliance across PCI-DSS, GDPR, and SOC frameworks. Identified a high-risk posture (8/10) driven by critical gaps in access control, data encryption, disaster recovery, and security monitoring. Delivered a prioritized remediation roadmap addressing 9 control deficiencies and 7 compliance gaps to strengthen security posture, ensure regulatory alignment, and protect sensitive customer/employee data.

## 📋 Audit Scope & Objectives
- Scope: Full security program assessment covering on-premises infrastructure, employee endpoints, retail/warehouse assets, internal networks, data storage, legacy systems, and compliance frameworks.
- Objectives: 
  - Inventory and classify critical assets
  - Evaluate existing security controls against industry best practices
  - Assess compliance with PCI-DSS, GDPR, and SOC standards
  - Identify gaps and develop actionable remediation strategies

  ## 🔍 Methodology & Framework
- Framework Applied: NIST Cybersecurity Framework (CSF) - *Identify* Function
- Assessment Approach: Structured compliance checklist (YES/NO format) with risk scoring (1-10 scale)
- Evaluation Criteria: Technical, physical controls, administrative controls and policies, data protection standards, incident response readiness, and business continuity planning

## 🔍 Risk Assessment Overview
- Overall Risk Score: 8/10 (High)
- Primary Risk Drivers: Inadequate asset management, absence of critical security controls, non-compliance with data protection regulations, and lack of disaster recovery/backups.
- Business Impact: Medium-to-high potential for operational disruption, regulatory fines, and reputational damage due to unprotected PII/SPII and cardholder data.

## 📊 Complete Controls & Compliance Checklist
*(Translated from the YES/NO checklist with all items included exactly as assessed. Status indicates current compliance posture.)* 

###  Technical, Administrative & Physical Controls Assessment

| Control Area | Status | Context & Observations |
|---|---|---|
| Least Privilege |  No | All employees have unrestricted access to internal data, including cardholder data & PII/SPII. |
| Disaster Recovery Plans | ❌ No | No DR strategy or business continuity planning in place. |
| Password Policies | ✅ Yes (Weak) | Policy exists but requirements are nominal; lacks modern complexity standards. |
| Separation of Duties | ❌ No | Not implemented; creates risk of insider threat & unauthorized privileged access. |
| Firewall | ✅ Yes | Properly configured with defined security rules; actively monitored by IT. |
| Intrusion Detection System (IDS) | ❌ No | Not deployed; limits visibility into network-based threats & lateral movement. |
| Backups | ❌ No | No backup strategy for critical data or systems. |
| Antivirus Software | ✅ Yes | Installed, actively monitored, and maintained by IT department. |
| Legacy System Monitoring/Maintenance | ❌ No | End-of-life systems monitored but lack scheduled maintenance & clear intervention protocols. |
| Encryption |  No | Not used for customer credit card data stored/processed locally. |
| Password Management System | ❌ No | No centralized enforcement; causes productivity loss via manual IT ticket resets. |
| Physical Locks (Offices/Store/Warehouse) | ✅ Yes | Adequate locking mechanisms in place. |
| CCTV Surveillance | ✅ Yes | Up-to-date closed-circuit television operational across premises. |
| Fire Detection/Prevention Systems | ✅ Yes | Fire alarms & sprinkler systems functional and maintained. |

### 💳 PCI-DSS Compliance Assessment

| Requirement | Status | Context & Observations |
|---|---|---|
| Only authorized users have access to customers’ credit card information | ❌ No | Unrestricted employee access violates least privilege & PCI requirement 7. |
| Credit card information is stored, accepted, processed, and transmitted internally in a secure environment | ❌ No | Lacks encryption, access controls, and secure processing segmentation. |
| Implement data encryption procedures to secure credit card transaction touch points & data | ❌ No | No AES/TLS encryption applied to cardholder data at rest or in transit. |
| Adopt secure password management policies |  No | Existing policy is weak; no centralized management or enforcement mechanism. |

### 🇪🇺 GDPR Compliance Assessment

| Requirement | Status | Context & Observations |
|---|---|---|
| E.U. customers’ data is kept private/secured | ❌ No | Lacks encryption, access restrictions, and data classification. |
| Plan in place to notify E.U. customers within 72 hours of a breach | ✅ Yes | Breach notification protocol established & documented. |
| Ensure data is properly classified and inventoried |  No | Inadequate asset management; no formal data classification or inventory process. |
| Enforce privacy policies, procedures, and processes to document & maintain data | ✅ Yes | Policies developed, documented, and enforced among IT & staff. |

### 🏢 SOC (Type 1 & Type 2) Compliance Assessment

| Requirement | Status | Context & Observations |
|---|---|---|
| User access policies are established |  No | Lacks formal RBAC, least privilege, and separation of duties. |
| Sensitive data (PII/SPII) is confidential/private |  No | Unrestricted internal access compromises confidentiality. |
| Data integrity ensures data is consistent, complete, accurate, and validated | ✅ Yes | IT has implemented controls to maintain data accuracy & validation. |
| Data is available to individuals authorized to access it | ✅ Yes | Availability controls are functioning for authorized personnel. |

---

## 🛠️ Gap Analysis & Prioritized Remediation Roadmap
*(Mapped directly to checklist deficiencies with actionable, framework-aligned recommendations)*

### 🔴 Critical (0-30 Days)
| Gap | Recommendation | Framework Alignment |
|---|---|---|
| ❌ Least Privilege / Separation of Duties | Implement Role-Based Access Control (RBAC); enforce least privilege; deploy Privileged Access Management (PAM). | NIST AC-6, SOC CC6.1 |
| ❌ Encryption / PCI-DSS Data Protection | Deploy AES-256 encryption for data at rest; enforce TLS 1.2+ for data in transit; implement payment tokenization. | PCI-DSS Req 3 & 4, GDPR Art 32 |
|  Backups / Disaster Recovery | Implement 3-2-1 backup strategy; define RTO/RPO; test DR runbooks quarterly. | NIST CP-9, SOC CC9.1 |
| ❌ IDS Deployment | Deploy network-based IDS/IPS; integrate with existing monitoring for real-time threat detection. | NIST SI-3, PCI-DSS Req 11 |

###  High Priority (30-90 Days)

| Gap | Recommendation | Framework Alignment |
|---|---|---|
| ❌ Password Policy & Management System | Enforce 12+ character complexity + MFA; deploy enterprise password manager; automate self-service resets. | NIST IA-5, PCI-DSS Req 8 |
| ❌ Asset Inventory & Data Classification | Deploy automated asset discovery; classify data by sensitivity; map to business impact analysis (BIA). | NIST ID.A, GDPR Art 30 |
| ❌ Legacy System Controls | Isolate legacy systems via network segmentation; create decommissioning roadmap; apply compensating controls. | NIST CM-7, SOC CC6.8 |

### 🔵 Strategic (90-180 Days)

| Gap | Recommendation | Framework Alignment |
|---|---|---|
| ✅ Password Policy (Strengthen) | Upgrade to NIST 800-63B standards; remove arbitrary expiration; focus on breach-password screening. | NIST IA-5, PCI-DSS Req 8.3 |
| ✅ CCTV/Physical Security | Integrate physical access logs with SIEM; implement badge/biometric server room access. | NIST PE-3, SOC CC6.8 |
| 🔄 Continuous Compliance | Establish quarterly access reviews; automate compliance monitoring; conduct annual PCI-DSS/GDPR audits. | NIST RA-5, SOC CC7.2 |

## 💼 Business Impact & Strategic Value
- Risk Reduction: Projected risk score decrease from 8/10 to ≤3/10 upon roadmap completion
- Regulatory Alignment: Resolves critical PCI-DSS, GDPR, and SOC non-compliance findings
- Operational Resilience: Establishes backup/DR capabilities, structured access controls, and threat visibility
- Cost Efficiency: Centralized password management & automated monitoring reduce IT helpdesk overhead & manual ticket volume
- Security Maturity: Advances organization from reactive to proactive security posture using NIST CSF & industry frameworks

##  Skills Demonstrated
- Security Compliance Auditing & Gap Analysis
- NIST CSF, PCI-DSS, GDPR, & SOC Framework Application
- Risk Assessment & Prioritization (1-10 Scoring)
- Technical Control Evaluation (Firewall, IDS, Encryption, EDR, Backups)
- Access Control & Zero Trust Principles (Least Privilege, Separation of Duties)
- Disaster Recovery & Business Continuity Planning
- Remediation Roadmap Development & Stakeholder Reporting
- Regulatory Compliance Mapping & Audit Documentation

## ️ Disclaimer
*This audit was conducted as part of a scenario-based educational simulation. All organizational names, data, and scenarios are fictional and created for practical learning purposes. No real systems, networks, or live environments were accessed or modified. The methodology, frameworks, and remediation strategies reflect industry-standard cybersecurity practices.*