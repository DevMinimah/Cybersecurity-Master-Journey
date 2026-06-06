# Final Capstone: From Breach to Resilience
## 🔍 End-to-End Cybersecurity Leadership: Incident Response → Forensic Attribution → Secure Architecture → Operational Resilience

>  Simulation-Based Capstone Project  
> *Completed as the culminating project of the IBM SkillsBuild Cybersecurity Certificate. This comprehensive capstone integrates incident response, digital forensics, security architecture design, SOC operations, risk management, and data resilience into a single investigative and strategic workflow.*

---

## 🎯 Executive Challenge
Lead a professional services organization through a complete cybersecurity transformation following a significant breach involving malware propagation and insider threat activity. Execute end-to-end leadership across two phases:

| Phase | Focus | Outcome |
|-------|-------|---------|
| Phase A: Reactive Response | Incident containment, forensic attribution, threat eradication | Identified insider threat, preserved evidence, halted active exploitation |
| Phase B: Proactive Rebuild | Security architecture redesign, SOC implementation, risk mitigation, data resilience | Established compliant, resilient, monitoring-ready operational state |

---

## 📋 Organizational Context (Redacted)
- Industry: Professional services with strict confidentiality, PII protection, and regulatory compliance requirements
- Pre-Incident Posture: Reactive security, limited monitoring, insufficient access controls, outdated infrastructure
- Incident Trigger: Unusual after-hours data transfers, system instability, credential anomalies
- Threat Profile: Post-exploitation framework usage, USB-propagating malware, credential-harvesting trojan activity
- Suspected Vector: Internal threat actor with prior privileged access
- Business Impact Risk: Client data exposure, reputational damage, regulatory non-compliance, operational disruption

---

## 🛡️ PHASE A: Incident Response & Forensic Attribution

### Objective
Contain active threats, preserve evidence, attribute the breach, and eradicate malicious artifacts.

### 1. Threat Intelligence & Initial Containment
- Reviewed threat intelligence feeds to differentiate administrative tools from malicious post-exploitation activity
- Identified lateral movement indicators via SMB/WMI protocols
- Isolated compromised endpoints to halt propagation
- Disabled AutoPlay and enforced Group Policy restrictions on USB execution
- Deployed commercial remediation tools post-isolation for malware eradication

### 2. Vulnerability Assessment & Prioritization
- Mapped active exploitation paths enabling unauthorized data exfiltration
- Classified vulnerabilities as Critical based on confidentiality impact and active exploitation status
- Implemented immediate antimalware scans and corrected access control misconfigurations
- Validated remediation through post-scan verification and log correlation

### 3. Infrastructure Hardening (Immediate)
- Configured host-based firewalls on individual workstations to contain lateral movement
- Updated router firmware to patch known persistence vectors
- Documented configuration changes for audit compliance and change management

### 4. Digital Forensics & Insider Threat Attribution
- Confiscated suspect workstation following strict chain of custody protocols
- Created bit-for-bit forensic image using FTK Imager; verified integrity via cryptographic hashing
- Analyzed disk image with Autopsy to recover deleted artifacts, reconstruct timelines, and correlate access patterns
- Outcome: Confirmed insider threat attribution through recovered artifacts and behavioral anomaly correlation

---

## 🏗️ PHASE B: Secure Architecture & Operational Resilience

### Objective
Transition the organization from reactive recovery to proactive, compliant, and resilient security operations.
### 1. Infrastructure & Cloud Strategy
- Conducted network reconnaissance to map topology, assets, and monitoring baselines
- Recommended and implemented a Private Cloud architecture
- Rationale: High-compliance environment required absolute data control, isolation capabilities, and customized security controls unavailable in public/hybrid models
- Outcome: Secure, compliant infrastructure foundation aligned with business continuity and regulatory obligations

### 2. Security Operations Center (SOC) Design & Implementation
- Evaluated Virtual, Hybrid, SOCaaS, and In-house models against operational requirements
- Selected Model: In-House SOC
- Strategic Justification: Maintains maximum control, enables direct oversight of private infrastructure, ensures fastest response without third-party latency
- Team Assembly:
  - Prioritized experienced personnel for immediate impact
  - Aligned skills to critical functions: threat hunting, incident response, security engineering
  - Integrated compliance-specific training (confidentiality protocols, privilege handling) into continuous improvement cycles

### 3. Comprehensive Risk Assessment & Mitigation
- Objective: Identify threats, analyze business impact, and design targeted controls
- Threat Categorization & Control Mapping:

| Threat Category | Specific Risk | Mitigation Control Implemented |
|----------------|---------------|--------------------------------|
| External | Phishing targeting personnel | Security awareness training + advanced email filtering |
| External | Physical breach of infrastructure | Enhanced facility security + access control protocols |
| Internal | Insider threat activity | Least privilege access + continuous behavioral monitoring |
| Internal | Weak credential management | Strong password policies + mandatory MFA enforcement |

- Business Impact Analysis: Prioritized investments based on potential data loss, operational disruption, and reputational damage
- Outcome: Risk-driven control implementation aligned with organizational tolerance and compliance obligations



### 4. Data Resilience Strategy (Backup, Recovery & Encryption)
- Backup Plan:
  - Assigned dedicated ownership to IT Lead for execution and verification
  - Scope: Full coverage of electronic organizational data
  - Methodology: Differential backups balancing resource efficiency with recovery speed
  - Storage Strategy: 3-2-1 Rule implemented (3 copies, 2 media types, 1 offsite)
- Recovery Plan:
  - Immediate: Restore from verified clean backups
  - Hardening: Apply patches to address exploited vulnerabilities
  - Review: Conduct structured lessons-learned sessions with stakeholders
  - Prevention: Tighten network rules and close identified gaps
- Encryption Strategy (Layered Approach):
  - Data at Rest (Endpoints): Full-disk encryption on all workstations
  - Data in Transit (External): Asymmetric encryption for sensitive external communications
  - Data in Transit (Internal): Public key encryption for internal network data sharing
  - Backup Data: Symmetric encryption for efficient large-volume protection
- Outcome: Comprehensive data resilience framework ensuring confidentiality, integrity, and availability across all states

---

## 📊 Theory-to-Practice Application

| Practical Activity | Theory Applied | Real-World Skill |
|--------------------|----------------|------------------|
| End-to-End Incident Response | NIST/SANS IR lifecycle: Detection → Containment → Eradication → Recovery | Managing multi-stage breaches from alert to resolution |
| Forensic Attribution | Write-blocking, hash verification, artifact recovery, timeline reconstruction | Court-admissible evidence handling and insider threat investigation |
| Cloud Architecture Design | Private vs. Public vs. Hybrid deployment models, compliance alignment | Aligning infrastructure choices with regulatory and risk requirements |
| SOC Model Evaluation | In-house vs. outsourced monitoring trade-offs, team structuring | Building scalable, controlled detection and response capabilities |
| Risk Assessment & Control Mapping | Threat categorization, impact analysis, control selection frameworks | Translating risk findings into prioritized, actionable security investments |
| Data Resilience Planning | 3-2-1 backups, differential strategies, encryption layering by data state | Designing resilient data protection and business continuity workflows |

---

## 🛡️ Security Principles Demonstrated

| Principle | Implementation | Business Impact |
|-----------|----------------|-----------------|
| Defense in Depth | Host firewalls + network controls + GPO restrictions + SOC monitoring + encryption layering | Limits blast radius and ensures multi-layered threat containment |
| Evidence Integrity | Cryptographic hashing, write-protected analysis, documented chain of custody | Ensures findings are legally defensible and audit-ready |
| Risk-Based Security | Impact analysis driving control prioritization and investment decisions | Maximizes ROI on security spend while addressing highest-value threats |
| Compliance Alignment | Tailored controls for confidentiality, access logging, privilege management | Reduces regulatory exposure and maintains client trust in high-stakes industries |
| Operational Resilience | 3-2-1 backups + differential strategy + phased recovery sequencing + lessons-learned cycles | Ensures business continuity and continuous security improvement post-incident |

---

## 💼 Employer-Ready Competencies

### Technical Skills
✅ End-to-end incident response execution (NIST/SANS frameworks)  
✅ Digital forensics: disk imaging, hash verification, artifact recovery, insider threat attribution (FTK Imager, Autopsy)  
✅ Threat intelligence interpretation and containment strategy design  
✅ Vulnerability assessment, CVSS mapping, and remediation prioritization  
✅ Security architecture design: private cloud, network segmentation, encryption layering  
✅ SOC model evaluation and in-house team structuring  
✅ Risk assessment, threat categorization, and control mapping  
✅ Backup strategy design (3-2-1 rule, differential backups, verification workflows)  
✅ Recovery sequencing and post-incident hardening procedures  
✅ Cryptographic control application (symmetric, asymmetric, full-disk encryption)  

### Professional Skills
✅ Cross-functional incident coordination and executive reporting  
✅ Strategic alignment of security initiatives with business and compliance requirements  
✅ Analytical reasoning connecting logs, artifacts, user behavior, and business impact  
✅ Risk communication translating technical findings to non-technical stakeholders  
✅ Documentation and reporting for technical, legal, and executive audiences  
✅ Continuous improvement mindset: lessons-learned integration into security operations  

---

## 🛠️ Tools & Technologies
- Forensics: FTK Imager, Autopsy
- Threat Intelligence: Commercial feeds (Red Canary, Malwarebytes), IOC validation
- OS Security: Windows Defender Firewall, Group Policy Object (GPO) management
- Network Security: Router firmware management, port/service analysis (SMB/WMI)
- Cloud Infrastructure: Private cloud deployment, isolation controls, compliance configuration
- SOC Operations: Monitoring frameworks, alerting workflows, incident ticketing systems
- Encryption Utilities: Full-disk encryption, asymmetric/symmetric key management, PKI concepts
- Backup & Recovery: Differential backup scheduling, offsite replication, integrity verification
- Risk Management: Threat modeling, control mapping, business impact analysis methodologies

---

## 🎓 Learning Outcomes Verified
Upon completion, I can confidently:
- ✅ Execute full-lifecycle incident response for active breaches
- ✅ Conduct legally defensible digital forensics investigations and attribute insider threats
- ✅ Design secure cloud and network architectures aligned with compliance requirements
- ✅ Evaluate and implement SOC models optimized for organizational scale and control
- ✅ Conduct risk assessments and map targeted controls to mitigate identified threats
- ✅ Architect data resilience strategies using industry-standard backup and recovery practices
- ✅ Apply layered encryption controls based on data state, transmission, and storage context
- ✅ Lead end-to-end security strategy from incident recovery to proactive operational maturity
- ✅ Document findings for technical, legal, and executive audiences with compliance awareness

---

## 🏆 Official Microcredential

| Field | Details |
|-------|---------|
| Credential | IBM SkillsBuild: IBM SkillsBuild Cybersecurity Certificate |
| Issued | June 05, 2026 |
| Credential ID | f201e203-2861-4678-bc32-664e4f285ba7 |
| Verify | [🔗 View Badge](https://www.credly.com/badges/f201e203-2861-4678-bc32-664e4f285ba7/public_url) |
| Progress | Final Capstone (Comprehensive) — 2/2 Components Completed |


### Badge Display
![IBM SkillsBuild Badge](../../../../Assets/badges/[your-badge-filename].png)

> ℹ️ *Completed in a controlled simulation environment. Badge issued via IBM SkillsBuild platform. Verification link confirms authenticity.*

---
*🔙 [Back to IBM SkillsBuild Dashboard](../../index.md)*