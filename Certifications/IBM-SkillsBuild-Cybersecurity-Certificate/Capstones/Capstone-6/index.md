# Capstone 6: Investigate an Incident Using Digital Forensics
## 🔍 Digital Forensics Investigation: Intellectual Property Theft via Physical Media


> 🎓 Simulation-Based Capstone Project  
> *Completed as part of the IBM SkillsBuild Cybersecurity Certificate program. This project demonstrates applied learning in incident response lifecycle management, forensic evidence preservation, and hands-on artifact recovery using industry-standard digital forensics platforms.*

---

## 🎯 Challenge
Execute a comprehensive digital forensics investigation into a simulated data breach involving physical media exfiltration from isolated systems, applying NIST Incident Response frameworks to contain the threat, preserve evidence integrity, and utilize forensic tools to recover artifacts and establish investigative conclusions.

---

## 🛡️ Phase 1: Incident Response & Containment (NIST Framework)
- Detection & Analysis: Identified breach of isolated systems indicating physical data exfiltration via removable media
- Containment: Secured devices from authorized personnel to prevent further data loss and preserve evidence chain
- Eradication & Recovery: Coordinated threat response and monitoring protocols
- Outcome: Established controlled incident environment with preserved evidence integrity

---

## 🔒 Phase 2: Evidence Acquisition & Chain of Custody
- Action: Secured physical media as primary evidence
- Process: Maintained strict chain of custody documentation tracking every transfer, handler, timestamp, and storage location
- Principle Applied: Legal admissibility standards and evidence preservation protocols
- Outcome: Unbroken custody trail ensuring forensic validity

---

## 💾 Phase 3: Forensic Imaging & Integrity Verification
- Tool Used: AccessData FTK Imager
- Action: Created bit-for-bit forensic image of target physical media
- Verification: Validated image integrity using cryptographic hash comparison (MD5/SHA-1) between original and forensic copy
- Principle Applied: Never analyze original evidence, work exclusively on verified forensic replicas
- Outcome: Exact replica created with verified integrity, ready for analysis

---

## 🔎 Phase 4: Forensic Analysis & Artifact Recovery
- Tool Used: Autopsy (Digital Forensics Platform)
- Analysis Steps:
  - File system examination and directory structure mapping
  - Deleted file recovery and slack space analysis
  - Metadata timeline reconstruction (creation, modification, access timestamps)
  - Keyword and content-based artifact search
- Outcome: Recovered hidden/deleted artifacts and established factual evidence trail supporting investigative conclusions

---

## 📊 Theory-to-Practice Application

| Practical Activity | Theory Applied | Real-World Skill |
|--------------------|----------------|------------------|
| NIST IR Lifecycle Execution | Incident detection, containment, eradication, recovery phases | Managing security incidents from alert to resolution |
| Chain of Custody Documentation | Legal evidence handling, admissibility standards, compliance | Preparing forensic evidence for legal/audit review |
| FTK Imager Forensic Imaging | Bit-stream copying, hash verification, write-blocking concepts | Creating court-admissible forensic disk images |
| Autopsy Artifact Analysis | File system structures, metadata analysis, deleted data recovery | Conducting deep-dive digital forensics investigations |

---

## 🛡️ Security & Forensic Principles Demonstrated

| Principle | Implementation | Business Impact |
|-----------|----------------|-----------------|
| Evidence Integrity | Hash verification before/after imaging; write-protected analysis | Ensures findings are legally defensible and audit-ready |
| Chain of Custody | Documented every evidence transfer, handler, and timestamp | Prevents evidence tampering claims; maintains investigative validity |
| Incident Containment | Isolated affected systems; secured removable media immediately | Limits data exposure; preserves attack artifacts for analysis |
| Forensic Methodology | Systematic acquisition → verification → analysis → reporting | Produces repeatable, standardized investigations aligned with industry best practices |

---

## 💼 Employer-Ready Competencies

### Technical Skills
✅ Digital forensic imaging using FTK Imager (bit-stream copies, hash verification)  
✅ Deep-dive artifact analysis with Autopsy (file recovery, metadata, keyword search)  
✅ NIST Incident Response lifecycle execution (detection → containment → recovery)  
✅ Chain of custody documentation and evidence handling protocols  
✅ Timeline reconstruction and deleted data recovery techniques  

### Professional Skills
✅ Investigative reporting and factual conclusion drafting  
✅ Critical analysis of evidence and conflicting claims  
✅ Cross-functional coordination with threat intelligence and recovery teams  
✅ Compliance awareness and legal standards adherence  

---

## 🛠️ Tools & Technologies
- AccessData FTK Imager: Forensic disk imaging, hash validation, write-blocker simulation
- Autopsy 4.x: File system analysis, deleted artifact recovery, metadata timeline mapping, keyword searching
- Cryptographic Hash Utilities: MD5/SHA-1 integrity verification for evidence validation
- NIST SP 800-61 Framework: Structured incident response lifecycle and containment strategies

---

## 🎓 Learning Outcomes Verified
Upon completion, I can confidently:
- ✅ Execute forensic imaging with verified integrity using industry-standard tools
- ✅ Maintain strict chain of custody documentation to ensure evidence admissibility
- ✅ Recover and analyze deleted artifacts to reconstruct incident timelines and establish facts
- ✅ Apply NIST IR frameworks to contain breaches, preserve evidence, and coordinate recovery
- ✅ Document investigative findings professionally for technical and legal stakeholders

---

## 🏆 Official Microcredential

| Field | Details |
|-------|---------|
| Credential | IBM SkillsBuild: Incident Response and Systems Forensics |
| Issued | May 29, 2026 |
| Credential ID | 47d7fe68-14e9-4186-899b-6f85cf576c1e |
| Verify | [🔗 View Badge](https://www.credly.com/badges/47d7fe68-14e9-4186-899b-6f85cf576c1e/public_url) |

### Badge Display
![IBM SkillsBuild Badge](../../Assets/badges/incident-response-and-systems-forensics.png)

> ℹ️ *Completed in a controlled simulation environment. Badge issued via IBM SkillsBuild platform. Verification link confirms authenticity.*

---
*🔙 [Back to IBM SkillsBuild Dashboard](../../index.md)*