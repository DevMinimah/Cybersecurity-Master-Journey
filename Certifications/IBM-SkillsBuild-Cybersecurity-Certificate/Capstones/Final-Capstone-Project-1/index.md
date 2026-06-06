# Final Capstone Project 1: Enhance Organizational Cybersecurity and Incidect Response 
## 🔍 Evaluate and Enhance Cybersecurity Posture of an Organization


>  Simulation-Based Capstone Project  
> *Completed as the culminating project of the IBM SkillsBuild Cybersecurity Certificate. This capstone integrates incident response, vulnerability management, infrastructure hardening, and digital forensics into a single investigative workflow.*

---

## 🎯 Challenge
Lead a comprehensive cybersecurity response for a professional services organization handling sensitive client data. The organization experienced network instability, unauthorized data transfers, and system crashes. Execute end-to-end incident response: analyze threat intelligence, contain active infections, harden host/network defenses, and conduct digital forensics to attribute the breach to an insider threat.

---

## 📋 Incident Context (Redacted)
- Organization Profile: Professional services firm with strict data privacy and PII protection requirements
- Incident Trigger: Unusual after-hours data transfers, frequent system crashes, and degraded network performance
- Threat Indicators: Post-exploitation framework usage, USB-propagating malware, credential-harvesting trojan activity
- Suspected Vector: Internal threat actor with prior privileged access
- Evidence Scope: Endpoint logs, network traffic anomalies, confiscated workstation, removable media artifacts

---

## 🛡️ Phase 1: Incident Response & Threat Intelligence
- Objective: Identify threat actors, understand malware behavior, and determine immediate containment tactics
- Analysis: Reviewed threat intelligence reports to differentiate between administrative tools and malicious post-exploitation activity
- Key Finding: Post-exploitation framework presence indicated active adversary lateral movement via SMB/WMI protocols
- Key Finding: USB-propagating malware indicated gaps in removable media security policies
- Containment Strategy: 
  - Isolate compromised endpoints to halt lateral movement
  - Disable AutoPlay and enforce Group Policy restrictions on USB execution
  - Disconnect infected systems and deploy commercial remediation tools after isolation

---

## 🔍 Phase 2: Vulnerability Assessment & Prioritization
- Objective: Categorize discovered vulnerabilities and prioritize remediation based on business impact
- Assessment: Identified active exploitation paths enabling unauthorized data exfiltration
- Prioritization: Classified as Critical due to severe impact on data confidentiality and active threat exploitation
- Control Implementation:
  - Immediate: Updated and executed antimalware scans to eradicate active infections
  - Secondary: Reviewed and corrected access control misconfigurations exposing network settings
  - Validation: Verified remediation effectiveness through post-scan verification and log review

---

## 🏗️ Phase 3: Infrastructure Hardening & Mitigation
- Objective: Secure host operating systems and network devices to prevent recurrence
- Host Security (Defense in Depth):
  - Configured host-based firewalls on individual workstations
  - Justification: Provides essential internal threat containment and lateral movement blocking beyond perimeter defenses
- Network Security:
  - Accessed router administrative interface via default gateway
  - Updated router firmware to patch known vulnerabilities and eliminate persistence vectors
  - Verified configuration backups and change documentation for audit compliance

---

## 🔎 Phase 4: Digital Forensics & Insider Threat Investigation
- Objective: Attribute the incident using preserved digital evidence
- Hypothesis: Activity logs indicated anomalous behavior from a former privileged staff member, suggesting dormant malware activation or logic-based trigger
- Evidence Preservation:
  - Confiscated suspect workstation following chain of custody protocols
  - Documented all handling, transfers, and storage conditions for legal admissibility
- Forensic Analysis:
  - Imaging: Created bit-for-bit forensic image using FTK Imager; verified integrity via cryptographic hashing
  - Investigation: Analyzed disk image with Autopsy to recover deleted artifacts, reconstruct timelines, and identify incriminating files
- Outcome: Confirmed insider threat attribution through recovered artifacts, metadata analysis, and access pattern correlation

---

##  Theory-to-Practice Application

| Practical Activity | Theory Applied | Real-World Skill |
|--------------------|----------------|------------------|
| NIST/SANS IR Execution | Detection, containment, eradication, recovery phases | Managing multi-stage breaches from alert to resolution |
| Threat Intelligence Analysis | Differentiating admin tools from post-exploitation frameworks | Actionable intel translation into containment decisions |
| Vulnerability Prioritization | CVSS scoring + business impact mapping | Risk-based remediation planning for executive stakeholders |
| Host/Network Hardening | Defense-in-depth, least privilege, firmware lifecycle | Reducing attack surface across layered infrastructure |
| Forensic Imaging & Analysis | Write-blocking, hash verification, artifact recovery | Court-admissible evidence handling and insider threat attribution |

---

## ️ Security Principles Demonstrated

| Principle | Implementation | Business Impact |
|-----------|----------------|-----------------|
| Evidence Integrity | Cryptographic hashing, write-protected analysis, chain of custody | Ensures findings are legally defensible and audit-ready |
| Defense in Depth | Host firewalls + network controls + GPO restrictions | Limits blast radius even if perimeter defenses are bypassed |
| Risk-Based Prioritization | CVSS + business impact + active exploitation status | Directs limited resources to highest-value remediation efforts |
| Insider Threat Attribution | Forensic timeline reconstruction + access pattern analysis | Enables precise HR/legal action and prevents false accusations |

---

## 💼 Employer-Ready Competencies

### Technical Skills
✅ End-to-end incident response execution (NIST/SANS frameworks)  
✅ Threat intelligence interpretation and containment strategy design  
✅ Vulnerability assessment, CVSS mapping, and remediation prioritization  
✅ Host-based firewall configuration and Group Policy enforcement  
✅ Router firmware management and network device hardening  
✅ Forensic disk imaging, hash verification, and artifact recovery FTK Imager, Autopsy
✅ Chain of custody documentation and evidence preservation protocols  

### Professional Skills
✅ Cross-functional incident coordination and executive reporting  
✅ Risk communication translating technical findings to business impact  
✅ Analytical reasoning connecting logs, artifacts, and user behavior  
✅ Compliance-aware documentation for legal and audit stakeholders  

---

## 🛠️ Tools & Technologies
- FTK Imager: Forensic disk imaging, hash validation, write-blocker simulation
- Autopsy: File system analysis, deleted artifact recovery, metadata timeline mapping
- Windows Defender Firewall / GPO: Host-based segmentation and policy enforcement
- Router Admin Interface: Firmware patching, configuration backup, port/service analysis
- Threat Intelligence Feeds: Malware behavior analysis, IOC validation, containment planning

---

## 🎓 Learning Outcomes Verified
Upon completion, I can confidently:
- ✅ Execute full-lifecycle incident response for active breaches
- ✅ Prioritize vulnerabilities using technical severity + business impact
- ✅ Harden endpoints and network devices to prevent recurrence
- ✅ Conduct legally defensible digital forensics investigations
- ✅ Attribute insider threats through artifact correlation and timeline analysis
- ✅ Document findings for technical, legal, and executive audiences

---

## 🏆 Official Microcredential

| Field | Details |
|-------|---------|
| Credential | IBM SkillsBuild: IBM SkillsBuild Cybersecurity Certificate |
| Issued | June 05, 2026 |
| Credential ID | f201e203-2861-4678-bc32-664e4f285ba7 |
| Verify | [🔗 View Badge](https://www.credly.com/badges/f201e203-2861-4678-bc32-664e4f285ba7/public_url) |
| Progress | Final Capstone 1/2 Completed |



### Badge Display
![IBM SkillsBuild Badge](../../../../Assets/badges/ibm-skillsbuild-cybersecurity-certificate.png)

> ️ *Completed in a controlled simulation environment. Badge issued via IBM SkillsBuild platform. Verification link confirms authenticity.*

---
*🔙 [Back to IBM SkillsBuild Dashboard](../../index.md)*