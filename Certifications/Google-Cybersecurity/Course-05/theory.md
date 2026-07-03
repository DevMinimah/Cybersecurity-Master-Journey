# Course 05: Assets, Threats, and Vulnerabilities

## 📅 Date Started: 2026-06-29
## 📅 Date Completed: 2026-07-03

---

## 🎯 What I Learned

### 1. Security Risk Planning & Compliance
- Explored asset inventory management and learnt how to classify data based on sensitivity (Restricted, Confidential, Internal Only, Public).
- Learned to identify the three states of data protected by cybersecurity professionals: Data in use, Data in transit, and Data at rest.
- Studied risk categorization, understanding the differences between Damage, Disclosure, and Loss of information.
- Gained an understanding of how to apply the NIST Cybersecurity Framework (CSF), focusing on its core functions: Identify, Protect, Detect, Respond, Recover, and Govern.

### 2. Cloud Security & Shared Responsibility
- Explored cloud service models (SaaS, PaaS, IaaS) on platforms like Google Cloud Platform (GCP) and Microsoft Azure.
- Learnt how to navigate the Shared Responsibility Model: understanding that clients secure what they control (IAM, resource configuration, data handling), while providers secure the underlying infrastructure.
- Analyzed cloud security challenges, primarily focusing on misconfigurations, monitoring access difficulties, and meeting regulatory standards (HIPAA, PCI DSS, GDPR).

### 3. Security Plans, Privacy & Auditing
- Learned how to structure security plans using policies, standards, and procedures.
- Studied notable privacy regulations: General Data Protection Regulation (GDPR), Payment Card Industry Data Security Standard (PCI DSS), and Health Insurance Portability and Accountability Act (HIPAA).
- Understood the difference between security audits (reviewing controls against expectations) and security assessments (checking resilience against actual threats).

### 4. Cryptography & Access Control
- Explored cryptographic concepts including encryption, decryption, hashing, and Public Key Infrastructure (PKI).
- Learnt how to differentiate symmetric algorithms (3DES, AES) from asymmetric algorithms (RSA, DSA) and understood Kerckhoff’s principle.
- Studied how to secure passwords using hashing algorithms (MD5, SHA) and salting techniques.
- Understood the implementation of the AAA framework (Authentication, Authorization, Accounting), SSO, MFA, LDAP, SAML, and OAuth.
- Explored Identity and Access Management (IAM) through user provisioning/deprovisioning and authorization models (MAC, DAC, RBAC).
- Learned how to audit account privileges (usage, privilege, and account change audits) across guest, user, service, and privileged accounts.

### 5. Vulnerability Management & CI/CD Security
- Learned how to apply the Defense in Depth model across five layers: Perimeter, Network, Endpoint, Application, and Data.
- Explored the use of the CVE list, NIST National Vulnerability Database (NVD), and Common Vulnerability Scoring System (CVSS).
- Studied how to secure CI/CD pipelines by addressing vulnerabilities like insecure dependencies, misconfigured permissions, lack of automated security testing (SAST/DAST), exposed secrets, and unsecured build environments.

### 6. OSINT & Threat Intelligence
- Explored how to leverage Open Source Intelligence (OSINT) tools including VirusTotal, the OSINT Framework, MITRE ATT&CK, and Have I Been Pwned to gather intelligence and track threats.

### 7. Vulnerability Assessments & Penetration Testing
- Learned the 4-step vulnerability assessment process: Identification, Vulnerability analysis, Risk assessment, and Remediation.
- Explored pen testing perspectives: Red team (offense), Blue team (defense), and Purple team (collaborative).
- Understood the application of penetration testing strategies: Open-box/White-box (full knowledge), Closed-box/Black-box (zero knowledge), and Partial knowledge/Gray-box testing.

### 8. Threat Actors, Hackers & Attack Vectors
- Learned how to categorize threat actors by motivation: Competitors, State actors, Criminal syndicates, Insider threats, and Shadow IT.
- Explored the classification of hackers by intent: Unauthorized, Authorized (ethical), and Semi-authorized.
- Analyzed Advanced Persistent Threats (APTs) and mapped common access points (direct access, removable media, email, cloud services, supply chains).
- Developed an understanding of the attacker mindset: Identify target, determine reach, evaluate vectors, and find appropriate tools.

### 9. Social Engineering & Phishing
- Learnt how to map the stages of social engineering: Prepare, Establish trust, Use persuasive tactics, Disconnect.
- Explored how to recognize attack signs: Baiting, Tailgating, Phishing, Quid pro quo, and Watering hole.
- Analyzed phishing kits (malicious attachments, fake forms, fraudulent links) and variants (Email, Smishing, Vishing, Spear phishing, Whaling).

### 10. Malicious Software & Web-Based Exploits
- Learned to identify malware types: Viruses, Worms, Trojans, Ransomware, Spyware, Botnets, Rootkits, Adware, Fileless malware, and Scareware.
- Explored how to detect signs of Cryptojacking (slowdowns, high CPU usage, sudden crashes, fast draining batteries).
- Studied how to mitigate web exploits including Cross-Site Scripting (Reflected, Stored, DOM-based) and SQL Injection (In-band, Out-of-band, Inferential) using prepared statements, input sanitization, and validation.

### 11. Threat Modeling
- Learned the threat modeling process: Define scope, identify threats, characterize environment, analyze threats, mitigate risks, evaluate findings.
- Explored the application of the PASTA framework (Process for Attack Simulation and Threat Analysis) and studied other common frameworks like STRIDE, Trike, and VAST.

---

## 💡 Key Takeaways

- **Security is Layered and Shared:** Whether defending on-premises infrastructure using the Defense in Depth model or securing cloud environments via the Shared Responsibility Model, security requires multiple overlapping controls and clear delineation of duties.
- **CI/CD Pipelines are Prime Targets:** Automating software delivery increases speed but also scales vulnerabilities if not secured. Integrating DevSecOps practices (like automated SAST/DAST and secrets management) is non-negotiable for modern application security.
- **The Human Element Remains the Weakest Link:** Despite advanced cryptographic and network defenses, social engineering and phishing remain highly effective. Technical controls must be paired with continuous user awareness training.
- **Proactive vs. Reactive Security:** Moving from simply reacting to incidents to proactively modeling threats (using PASTA/STRIDE), conducting penetration tests, and performing continuous vulnerability assessments is what matures an organization's security posture.
- **Access Control is the New Perimeter:** With the rise of cloud and remote work, identity and access management (IAM, RBAC, MFA) and strict privilege auditing are the most critical defenses against unauthorized data access.

---

## 🔗 Links/Resources

- [Google Cybersecurity Professional Certificate](https://www.coursera.org/professional-certificates/google-cybersecurity)
- [Kerckhoff’s Principle (Wikipedia)](https://en.wikipedia.org/wiki/Kerckhoffs%27s_principle)
- [OSINT Framework](https://osintframework.com/)
- [MITRE ATT&CK](https://attack.mitre.org/)
- [Have I Been Pwned](https://haveibeenpwned.com/)
- [SANS OUCH! Newsletter](https://www.sans.org/newsletters/ouch/)
- [Google Phishing Quiz](https://phishingquiz.withgoogle.com/)
- [OWASP SQL Injection Testing Guide](https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/07-Input_Validation_Testing/05-Testing_for_SQL_Injection)
- [DevSecOps Using GitHub Actions (Medium)](https://medium.com/@rahulsharan512/devsecops-using-github-actions-building-secure-ci-cd-pipelines-5b6d59acab32)
- [GitLab CI/CD Hands-On Lab: Securing Scanning](https://handbook.gitlab.com/handbook/customer-success/professional-services-engineering/education-services/gitlabcicdhandsonlab9/)


---

**🎓 Google Cybersecurity Professional Certificate | Course 5 of 8**
