# Module 03: Endpoint Security & Physical Controls - Practical Activity

## 📅 Date Started: 2026-05-05
## 📅 Date Completed: 2026-05-05

## 🧪 Activity Type:
Scenario-based Cybersecurity professional simulation: Acting as an IT security specialist to triage malware incidents, analyze phishing attempts, and design a physical security layout for a high-compliance environment.

## 🎯 Lab Goal:
To identify, analyze, and mitigate endpoint threats (adware, spyware, malware) using specialized scanning tools, evaluate phishing indicators, and design physical security controls to prevent data exfiltration and unauthorized access in compliance with government contract requirements.

## 🛠 Tools Used:
- Adobe file editor
- AdwCleaner (adware/spyware detection & removal)
- Malwarebytes (antimalware scanning & remediation)
- Physical Security Simulation Interface
- Phishing analysis toolkit/email client simulation

## 📋 What I Did:
1. Triage two employee support tickets: analyzed Jade’s system for adware/browser hijacking and Martino’s system for unauthorized programs, performance degradation, and disabled security settings.
2. Deployed AdwCleaner to scan, detect, and remove adware and spyware from Jade’s workstation, restoring browser defaults and eliminating unwanted pop-ups.
3. Executed a Malwarebytes full-system scan on Martino’s device to identify and quarantine malware, including viruses and potentially disabled security components, restoring system stability.
4. Reviewed simulated phishing emails to identify social engineering tactics, suspicious links, and spoofed sender addresses, documenting red flags for employee awareness training.
5. Designed a physical security control plan for a first-floor layout, strategically placing biometric access, security cameras, guards, and desks to enforce a strict "no removable media" policy and secure the server room for a government contract bid.

## 🔍 What I Found:
- Adware/Spyware (Jade): The symptoms (pop-ups, automatic tab openings, changed search engine/homepage, redirects) are classic indicators of a browser hijacker bundled with adware. AdwCleaner successfully identified PUPs (Potentially Unwanted Programs) and registry modifications, restoring browser integrity after cleanup.
- Malware/Endpoint Threats (Martino): Slow performance, unexpected crashes, unauthorized software, and disabled security software point to active malware infection, likely a trojan or rootkit designed to evade detection. Malwarebytes detected malicious executables and restored disabled security services post-remediation.
- Phishing Indicators: Spoofed domains, urgent language, mismatched URLs, and requests for credentials/sensitive data were consistent across simulated phishing examples, reinforcing the need for employee verification protocols and email filtering.
- Physical Security Design: Replacing shared keys with biometric access for the server room eliminates credential sharing risks. Positioning security guards at the lobby enables active enforcement of the "no USB/removable media" contract requirement, while hallway cameras provide audit trails for accountability.

## 💡 What I Learned:
- Endpoint threats often manifest through behavioral symptoms (browser changes, system slowdowns, disabled security); systematic scanning with specialized tools is required for accurate identification and safe removal.
- Adware and malware serve different purposes but both compromise confidentiality and system integrity; using dedicated tools like AdwCleaner for PUPs and Malwarebytes for broader malware ensures comprehensive remediation.
- Physical and digital security are interdependent; enforcing technical policies (e.g., banning USB drives) requires physical controls (guards, biometrics, cameras) to prevent data exfiltration and meet compliance standards.
- Proactive threat identification—whether through phishing analysis, endpoint scanning, or physical access design—strengthens the organization’s defense-in-depth strategy and reduces response time during real incidents.

## 📸 Screenshot:
![Module 03 Malwarebytes Scan for malwares](<Malwarebytes Scan.jpg>)
![Module 03 adware/spyware detection & removal](<AdwCleaner Scan.jpg>)
![Module 03 Physical Security Layout](<Physical Security Control.png>)