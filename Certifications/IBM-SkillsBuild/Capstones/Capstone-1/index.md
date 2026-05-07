# Capstone 1: Evaluate an Organization's Data Security Posture
## 🏥 Cedarville Family Health Clinic

> 🎓 Simulation-Based Capstone Project  
> *This evaluation was completed as part of the IBM SkillsBuild Cybersecurity Certificate program. Cedarville Family Health Clinic is a simulated healthcare scenario created for educational purposes. All findings, recommendations, and artifacts are based on the simulated environment and demonstrate applied learning of HIPAA compliance, risk assessment, and data security principles.*

---

## 🎯 Challenge
Evaluating an Organization's Data Security Posture against:
- ✅ HIPAA Compliance
- ✅ Risk Assessment Frameworks
- ✅ General Compliance Requirements
- ✅ Data Encryption Standards

---

## 🔍 Evaluation Areas

### 1. HIPAA Compliance Assessment

| Area | Status | Findings |
| Privacy Rule | ⚠️ Partial | Policies exist, but delayed paper-to-digital entry creates windows for unauthorized access or loss of PHI. No documented patient authorization or minimum necessary access procedures. |
| Security Rule | ❌ Non-compliant | Fails across all three safeguard categories: <br>• *Administrative*: Policies lack enforcement, formal risk analysis, contingency planning <br>• *Physical*: Single workstation on open desk; backup media carried personally without secure storage <br>• *Technical*: No access controls, audit logs, encryption, or network security |
| Breach Notification | ❌ Not documented | Current practices create high breach probability with no defined 60-day notification workflow or mitigation steps |

### 2. Risk Assessment

Threats Identified:
- 🔴 External: Malware/ransomware via internet-connected workstation, unauthorized network access
- 🔴 Internal: Human error (missed backups), physical loss/theft of media, insider mishandling of paper records
- 🟠 Environmental: Single point of failure (1 PC, 1 backup drive), drive corruption, fire/flood at single location

Vulnerabilities Discovered:
Risk Levels Assigned:
| Level | Issue | Impact |
| 🔴 Critical | Unencrypted backup drive carried offsite | PHI exposure, HIPAA violation |
| 🔴 Critical | Single computer dependency | Total data loss if hardware fails |
| 🟠 High | Delayed paper-to-digital entry | Data loss window, compliance gap |
| 🟠 High | No access controls or audit trails | Unauthorized access undetected |
| 🟡 Medium | Policy existence without training verification | False sense of compliance |

Mitigation Recommendations:
1. Immediately encrypt all devices storing PHI (AES-256)
2. Replace manual backup with automated, encrypted, cloud-based HIPAA-compliant solution
3. Implement firewall, endpoint protection, and unique user logins
4. Establish tested contingency & disaster recovery plans
5. Conduct formal HIPAA security awareness training with attendance tracking

### 3. Compliance Review

Regulatory Requirements Checked:
- HIPAA Security Rule (45 CFR §164.308-312)
- HIPAA Privacy Rule
- HITECH Act breach notification requirements
- State medical record retention laws

Gaps Identified:
Remediation Roadmap:
| Priority | Action | Timeline |
| 1 | Conduct formal Security Risk Analysis (SRA) | Week 1 |
| 2 | Deploy full-disk encryption on all workstations & removable media | Week 2 |
| 3 | Implement automated 3-2-1 backup strategy with quarterly restore testing | Week 3 |
| 4 | Draft & enforce Access Control, Audit Control, and Incident Response policies | Week 4 |
| 5 | Train all staff; document completion; schedule annual refreshers | Ongoing |

### 4. Data Encryption Analysis

| Category | Status | Details |
| Encryption at Rest | ❌ None | Main workstation and portable backup drive store unencrypted PHI. No full-disk or file-level encryption implemented. |
| Encryption in Transit | ⚠️ Unverified | Internet connection used for supply ordering, but no TLS/SSL configuration or secure clinic-to-vendor PHI transmission documented. |
| Key Management | ❌ Non-existent | No encryption keys deployed, stored, or rotated. No separation of duties for cryptographic controls. |

Recommendations for Improvement:
- Enable BitLocker (Windows) or FileVault (macOS) on all clinic devices
- Use hardware-encrypted or software-encrypted (AES-256) USB/portable drives
- Enforce TLS 1.2+ for any external communications or cloud backup transfers
- Establish a documented key management policy (secure storage, rotation, backup, revocation)
- Consider HIPAA-compliant backup vendors that manage encryption keys under BAA

---

## 📤 Key Deliverables
✅ Compliance gap analysis report (mapped to HIPAA Security/Privacy Rules)  
✅ Risk matrix (Critical/High/Medium threats with mitigation timelines)  
✅ Encryption recommendations (At-rest, in-transit, key management, vendor criteria)  
✅ Executive summary (Leadership-ready overview of posture, liabilities, and 90-day remediation roadmap)

---

## 💡 What I Learned
Evaluating Cedarville Family Health Clinic highlighted the critical gap between *having policies* and *implementing technical safeguards*. In healthcare, even well-intentioned manual processes (like carrying a backup drive in a purse) can violate HIPAA and expose clinics to severe financial, legal, and reputational risk. 

I learned that true security posture requires defense-in-depth: encryption everywhere, automated tested backups, strict access controls, and continuous staff training. Most importantly, compliance isn't a checklist, it's an operational culture that must be validated through regular testing and documentation.

---

## 🏆 Official Microcredential Earned

| Field | Details |
| Credential | IBM SkillsBuild: Governance, Risk, Compliance, and Data Privacy |
| Issued | May 04, 2026 |
| Credential ID | 09aa3a71-c2da-40f2-b9b7-ff11b0137c7d |
| Verify | [🔗 View on Credly](https://www.credly.com/badges/09aa3a71-c2da-40f2-b9b7-ff11b0137c7d) |

### Badge Display
![IBM SkillsBuild Microcredential Badge](../../Assets/badges/governance-risk-compliance-and-data-privacy.png)

> ℹ️ *This capstone was completed in a controlled simulation environment. Proprietary simulation materials are not shared publicly per IBM SkillsBuild policy. This report and the official microcredential serve as verified proof of competency.*

---
*🔙 [Back to IBM SkillsBuild Dashboard](../../index.md)*
* 