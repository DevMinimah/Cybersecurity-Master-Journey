# Module 06: Network Security Design - Practical Activity

## 📅 Date Started: 2026-05-09
## 📅 Date Completed: 2026-05-10

## ⚠️ Disclaimer:
Every scenario is a simulation for practical educational purposes only. All activities are conducted in controlled learning environments to develop cybersecurity skills and knowledge. No real systems, networks, or data were accessed or modified.

## 🧪 Activity Type:
Scenario-based professional simulation: Evaluating and designing secure network architectures for distinct business and compliance requirements (public-facing web services vs. air-gapped classified data).

## 🎯 Lab Goal:
To evaluate proposed network architectures against specific organizational security requirements, applying principles of network segmentation, DMZ deployment, and air-gapping to protect data based on sensitivity, access needs, and regulatory mandates.

## 🛠 Tools Used:
- Network architecture simulation/design interface
- Network segmentation & zoning evaluation framework

## 📋 What I Did:
1. Analyzed Scenario 1 (Yummy In My Tummy) requirements for a public-facing recipe web server and customer-accessible database.
2. Evaluated four proposed network designs to identify the architecture that properly isolates the web server in a DMZ while restricting direct internet-to-database access.
3. Analyzed Scenario 2 (Top Secret Emporium) requirements for maintaining an air gap to protect classified government contract data.
4. Evaluated four proposed network designs to identify the architecture that enforces complete physical and logical isolation between the classified network and all corporate/external networks.
5. Documented the security rationale for each selected design, aligning network topology choices with data classification, threat modeling, and compliance requirements.

## 🔍 What I Found:
- Scenario 1 (Public Web & Database): The secure design places the web server in a DMZ, with the database in a protected internal zone. Internet traffic is allowed to the web server only, while database access is restricted to authenticated internal/application traffic. This prevents direct external exploitation of sensitive data while enabling customer functionality.
- Scenario 2 (Air-Gapped Classified Network): The compliant design shows absolute physical and logical separation. No routing, bridging, or firewall rules connect the classified segment to the corporate or internet networks. This eliminates network-based attack vectors, meeting strict government contract requirements.
- Segmentation & Risk Alignment: Network architecture must match data sensitivity. Public services require controlled exposure (DMZ + stateful firewalls), while classified assets demand total isolation (air gap). Flat or overly permissive designs introduce unnecessary attack surface and compliance violations.
- Common Design Flaws: Several proposed options featured missing firewalls, direct database exposure, or improper zone placement, demonstrating how architectural oversights can bypass technical controls and violate security baselines.

## 💡 What I Learned:
- Secure network design is driven by data classification and access requirements; controls must be layered, proportionate, and explicitly mapped to business needs.
- DMZs act as critical buffer zones, enabling public service delivery while preventing direct internet access to internal assets like databases and application servers.
- Air gaps provide the highest assurance for classified or highly regulated data by removing network connectivity entirely, though they require strict procedural controls for any authorized data transfer.
- Evaluating network architectures requires verifying proper segmentation, firewall placement, default-deny policies, and compliance alignment before deployment.
- Network security is a foundational control that directly reduces attack surface, limits lateral movement, and supports both technical defense and regulatory audit requirements.

## 📸 Screenshot:
🔒 Screenshot Restriction Notice

Screenshots from IBM SkillsBuild simulated lab environments are proprietary content and cannot be shared externally per IBM's academic integrity policy and terms of use.
Lab Completion Verified:
- ✅ Platform: IBM SkillsBuild
- ✅ Module Status: 100% COMPLETE
- ✅ Activities Completed: Network security design (DMZ architecture & air-gapped network)
- ✅ Completion Date: 2026-05-10

Alternative Evidence: Comprehensive written documentation provided in sections above.