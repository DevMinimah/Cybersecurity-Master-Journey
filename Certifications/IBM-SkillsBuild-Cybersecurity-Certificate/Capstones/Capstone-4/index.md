# Capstone 4: Propose Cloud Services and Security Measures
## ☁️ Cloud Migration & Security Architecture for A Manufacturing Company

> 🎓 Simulation-Based Capstone Project  
> *Completed as part of the IBM SkillsBuild Cybersecurity Certificate program. The Manufacturing company is a simulated small manufacturing scenario created for educational purposes. All architecture designs, threat models, and security recommendations demonstrate applied learning in cloud strategy, risk assessment, and defense-in-depth implementation.*

---

## 🎯 Challenge
Propose a secure, cost-effective cloud migration strategy for a small manufacturing company, balancing legacy system integration, proprietary data protection, and operational scalability while implementing targeted threat mitigation controls.

---

## 🏗️ Strategic Cloud Architecture Decisions

### 1. Deployment Model: Hybrid Cloud
- Decision: Recommended a Hybrid Cloud architecture
- Justification:
  - Legacy Integration: Existing on-premise legacy systems remain on a Private Cloud while new workloads migrate to Public Cloud
  - Data Sensitivity: Proprietary manufacturing data & employee records stay under strict Private Cloud control; non-sensitive web services leverage Public Cloud scalability
  - Cost Efficiency: Shifts from CapEx to OpEx by scaling public resources based on manufacturing demand

### 2. Service Model: Infrastructure as a Service (IaaS)
- Decision: Selected IaaS as the primary service model
- Justification:
  - Control & Customization: Full OS/middleware configuration required for legacy app compatibility (unlike PaaS/SaaS)
  - Skill Alignment: Leverages existing IT team's infrastructure expertise, minimizing retraining
  - Scalability: Dynamic resource scaling without physical hardware procurement

---

## 📊 Threat Modeling & Risk Assessment

| Threat Category | Specific Risk Identified | Potential Business Impact |
|-----------------|--------------------------|---------------------------|
| Identity Management | Improper identity management → unauthorized access | Data breaches exposing proprietary IP; compliance violations |
| Configuration | Cloud misconfiguration (incorrect settings) | Sensitive data exposure to public internet; reputational damage |
| Network Security | DDoS attacks overwhelming traffic | Manufacturing operation disruption; revenue/productivity loss |
| Insider Threats | Malicious activities by authorized users | Production system sabotage; trade secret theft |
| API Security | Insecure APIs allowing data manipulation | Data leaks; compromised system integrity & customer trust |

---

## ️ Security Posture & Mitigation Strategy

| Control Area | Implementation | Security Principle |
|--------------|----------------|-------------------|
| Access Control | MFA + Role-Based Access Control (RBAC) | Principle of Least Privilege |
| Data Protection | Encryption for Data at Rest & in Transit | Confidentiality & Integrity |
| Network Defense | DDoS Protection & Traffic Filtering | Availability & Business Continuity |
| Application Security | Regular API Security Audits & Patch Management | Vulnerability Management |
| Compliance & Governance | Scheduled Compliance Audits + Security Awareness Training | Risk Reduction & Human Firewall |

---

## 💼 Employer-Ready Competencies

### Technical Skills
✅ Cloud architecture design (Hybrid deployment, IaaS model selection)  
✅ Cloud-specific threat modeling & risk assessment  
✅ Implementation of MFA, RBAC, encryption, and DDoS mitigation  
✅ API security auditing & configuration management  
✅ Legacy-to-cloud migration planning  

### Professional Skills
✅ Translating business constraints (budget, legacy systems, compliance) into technical architecture  
✅ Risk-based decision making & control justification  
✅ Security posture management & continuous monitoring strategy  
✅ Cross-functional communication (IT team alignment, executive reporting)  

---

## 🎓 Learning Outcomes Verified
Upon completion, I can confidently:
- ✅ Evaluate business requirements and map them to optimal cloud deployment & service models
- ✅ Identify cloud-specific threats (misconfiguration, insecure APIs, identity gaps) and assess business impact
- ✅ Design defense-in-depth strategies using technical, administrative, and operational controls
- ✅ Justify security investments by linking threats → risks → business impacts → mitigation tactics

---

## 🏆 Official Microcredential

| Field | Details |
|-------|---------|
| Credential | IBM SkillsBuild: Cloud Security |
| Issued | May 23, 2026 |
| Credential ID | 960774b1-b037-4f92-ac1d-e31d0828dd81 |
| Verify | [🔗 View on Credly](https://www.credly.com/badges/960774b1-b037-4f92-ac1d-e31d0828dd81/public_url) |

### Badge Display
![IBM SkillsBuild Badge](../../Assets/badges/cloud-security.png)

> ℹ️ *Completed in a controlled simulation environment. Badge issued via IBM SkillsBuild platform. Verification link confirms authenticity.*

---
*🔙 [Back to IBM SkillsBuild Dashboard](../../index.md)*