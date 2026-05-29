# Module 12: Digital System Forensics - Practical   Activity

## 📅 Date Started: 2026-05-27
## 📅 Date Completed: 2026-05-28

## ⚠️ Disclaimer:
Every scenario is a simulation for practical educational purposes only. All activities are conducted in controlled learning environments to develop cybersecurity skills and knowledge. No real systems, networks, or data were accessed or modified.

## 🧪 Activity Type:
Scenario-based professional simulation: Acting as a digital forensics investigator to preserve digital evidence using FTK Imager, analyze multi-source attack artifacts with Autopsy, apply chain of custody procedures, and develop remediation recommendations based on forensic findings.

## 🎯 Lab Goal:
To apply industry-standard digital forensics methodologies by creating forensically sound disk images, analyzing digital evidence across email, system, and network data sources, maintaining proper chain of custody documentation, recovering deleted artifacts, and translating technical findings into actionable security improvements.

## 🛠 Tools Used:
- FTK Imager (forensic disk imaging and verification)
- Autopsy (digital forensics platform and data carving)
- Chain of custody documentation
- System file integrity and process monitoring utilities
- Network traffic and log analysis interfaces
- Encrypted storage devices (evidence preservation)

##  What I Did:

### Task 1: Create a Forensic Disk Image with FTK Imager
1. Scenario Setup: Assumed role as digital forensics investigator responding to an internal incident where a suspended employee was suspected of exfiltrating sensitive organizational data using a personal USB storage device.
2. Evidence Preservation Protocol:
   - Recognized the need to create a bit-for-bit forensic copy before any analysis to maintain original evidence integrity
   - Ensured write-blocking procedures were conceptually applied to prevent evidence contamination
   - Prepared chain of custody documentation to track evidence handling from acquisition onward
3. Forensic Imaging Execution:
   - Launched FTK Imager and selected the target USB storage device as the source
   - Configured forensic image parameters including destination path, naming convention, and case metadata
   - Enabled cryptographic hash calculation (MD5/SHA-1) for post-imaging integrity verification
   - Initiated the imaging process and monitored completion status
4. Image Verification:
   - Verified hash values matched between original media and forensic image
   - Documented verification results in chain of custody records
   - Secured the forensic image on encrypted storage for subsequent analysis

### Task 2: Analyze a Cyberattack Using Digital Forensics
1. Investigation Scoping & Data Source Prioritization:
   - Reviewed case background: Organization experienced a network-impacting cyberattack with no mobile/personal device involvement
   - Evaluated four potential data sources (Network Logs, System Files, Email Accounts, Mobile Data)
   - Selected three applicable sources based on incident scope and prioritized examination sequence
2. Email Account Forensic Analysis:
   - Examined employee mailboxes for social engineering and credential compromise indicators
   - Identified phishing emails and analyzed headers to trace malicious origin
   - Documented indicators of compromise (IoCs) including embedded malicious links clicked by users
   - Analyzed follow-up emails using spoofed/typo-squatted domains and identified malware attachments
3. System File & Process Forensics:
   - Examined system directories for unauthorized modifications or replacements of critical files
   - Identified anomalous running processes and potential process injection techniques
   - Correlated file modification timestamps with attack timeline to establish persistence mechanisms
   - Documented evidence of malware installation and unauthorized system access
4. Network Log Forensic Analysis:
   - Analyzed traffic logs for anomalous communication patterns
   - Identified compromised accounts sending outbound messages to suspicious external addresses
   - Detected unusual inbound traffic indicating command-and-control (C2) communication and bot-like behavior
   - Mapped network artifacts to lateral movement and potential data exfiltration attempts
5. Autopsy Evidence Analysis:
   - Loaded the FTK Imager forensic image into Autopsy for deep artifact examination
   - Analyzed disk volumes, identifying formatted partitions (FAT32) and unallocated space
   - Utilized data carving capabilities to recover deleted files from unallocated clusters
   - Examined carved file metadata including timestamps, MIME types, file sizes, and hash values
   - Documented recovered artifacts supporting investigation conclusions
6. Chain of Custody Review & Correction:
   - Evaluated the organization's chain of custody procedures for legal admissibility
   - Identified critical documentation gaps:
     - Overly permissive access controls allowing unrestricted evidence access
     - Incomplete handling logs missing date/time stamps for evidence interactions
   - Documented correct practices: encrypted storage, restricted authorized access, comprehensive handling logs
7. Investigation Reporting & Recommendations:
   - Compiled forensic findings into a structured incident report
   - Mapped technical artifacts to attack phases and root cause determination
   - Developed actionable recommendations: enhanced phishing awareness training, simulated phishing exercises, email filtering improvements, and multi-factor authentication enforcement

## 🔍 What I Found:

### Forensic Imaging & Preservation Findings:
- Bit-for-Bit Integrity: FTK Imager successfully created a forensically sound copy preserving original file system structures, deleted data remnants, and metadata
- Hash Verification: Cryptographic hashing provided mathematical proof that the forensic image remained unaltered from acquisition through analysis
- Write-Blocking Necessity: Hardware or software write-protection is non-negotiable; direct analysis of original media risks evidence contamination and legal inadmissibility
- Case Metadata: Embedding examiner information, case numbers, and descriptions within the image file maintains organizational integrity and audit readiness

### Email Forensic Findings:
- Social Engineering Vector: Initial compromise originated from phishing emails leveraging psychological manipulation and trusted domain impersonation
- Header Analysis Value: Email headers revealed true routing paths and sender origins despite spoofed display names and reply-to addresses
- IoC Extraction: Malicious URLs, attachment hashes, and sender domains provided actionable indicators for blocking and threat intelligence sharing
- Escalation Pattern: Attackers used follow-up emails with misspelled domains to maintain engagement and deliver additional malware payloads

### System & Process Forensic Findings:
- Persistence Mechanisms: Attackers modified or replaced legitimate system files to maintain access across reboots and evade basic detection
- Process Anomalies: Suspicious running processes indicated malware execution, potential privilege escalation, and unauthorized background activity
- Timeline Correlation: File creation/modification timestamps aligned with network and email artifacts, enabling precise attack phase reconstruction
- Defense Evasion: Malware utilized legitimate system processes and file modifications to blend with normal operations and bypass signature-based controls
### Network Forensic Findings:
- C2 Communication: Unusual inbound traffic patterns indicated compromised hosts communicating with attacker-controlled infrastructure
- Account Compromise: Outbound email traffic from legitimate accounts to suspicious destinations confirmed credential theft and active exploitation
- Bot Activity: Compromised systems exhibited automated communication patterns consistent with remotely controlled botnet behavior
- Lateral Movement: Network artifacts revealed attackers using compromised credentials and systems to expand access within the organization

### Autopsy Analysis Findings:
- Data Carving Effectiveness: Autopsy successfully recovered deleted files from unallocated disk space, demonstrating that deletion does not equal destruction
- Volume Analysis: Differentiated between allocated, formatted volumes and unallocated space, guiding focused investigation efforts
- Metadata Extraction: Recovered file metadata provided insights into file creation, modification, access, and deletion timelines
- Artifact Correlation: Carved files, registry entries, and browser artifacts created a comprehensive view of user activity and malware behavior

### Chain of Custody & Legal Admissibility Findings:
- Documentation Gaps: Missing timestamps and overly permissive access controls violated forensic best practices and could render evidence inadmissible
- Access Control Principles: Evidence access must follow least-privilege principles with documented justification for every interaction
- Complete Logging: Every evidence handler must record date, time, location, person's name, reason for handling, and actions taken
- Secure Storage: Encrypted, access-controlled storage prevents unauthorized tampering and maintains evidence confidentiality

### Root Cause & Attack Reconstruction:
1. Initial Access: Phishing email delivered to employee inbox
2. Execution: User interaction with malicious link/attachment triggered compromise
3. Persistence: Malware installed and system files modified for long-term access
4. Privilege Escalation: Attackers gained elevated system and account privileges
5. Defense Evasion: Malware blended with legitimate processes and modified system files
6. Credential Access: User credentials and email accounts compromised
7. Discovery: Attackers mapped internal network and identified additional targets
8. Lateral Movement: Compromised accounts used to expand access and distribute malware
9. Command & Control: Established persistent remote communication channels
10. Exfiltration/Impact: Network disruption and potential data theft through outbound communications

## 💡 What I Learned:

### Digital Forensics Fundamentals:
- Evidence Preservation First: Creating forensically sound images before analysis is the cornerstone of digital forensics; original media must never be directly examined
- Chain of Custody is Critical: Meticulous documentation of every evidence interaction determines legal admissibility; even minor gaps can destroy an investigation's credibility
- Multi-Source Correlation: No single data source tells the complete story; correlating email, system, and network artifacts enables accurate attack reconstruction
- Deletion ≠ Destruction: Deleted files remain recoverable from unallocated disk space until overwritten, making data carving a powerful forensic technique

### FTK Imager Proficiency:
- Forensic Imaging Standards: Industry-standard tools create court-admissible copies with embedded verification hashes
- Hash Algorithm Importance: MD5 and SHA-1/SHA-256 provide mathematical proof of integrity and chain of custody continuity
- Case Management: Proper case metadata and naming conventions maintain organizational integrity across complex investigations
- Image Format Selection: E01 format offers compression, error checking, and embedded metadata advantages over RAW format for most investigations
### Autopsy Analysis Capabilities:
- Timeline Reconstruction: Autopsy's timeline analysis correlates file system events, registry changes, and network artifacts into coherent attack narratives
- Data Carving Techniques: File carving recovers deleted evidence based on file signatures and headers, essential for investigating evidence destruction attempts
- Artifact Extraction: Automated parsing of browser history, email artifacts, and system logs accelerates evidence identification
- Volume & Partition Analysis: Understanding file system structures (FAT32, NTFS, exFAT) guides targeted investigation of allocated vs. unallocated space

### Attack Lifecycle & Framework Mapping:
- MITRE ATT&CK Alignment: Forensic artifacts map directly to ATT&CK techniques (T1566 Phishing, T1059 Command Execution, T1070 Indicator Removal, T1071 Application Layer Protocol)
- Cyber Kill Chain Application: Forensic findings validate attack phases from delivery and exploitation to installation, command & control, and actions on objectives
- IoC Lifecycle: Indicators of compromise have limited shelf life; rapid extraction, sharing, and blocking are essential for effective threat mitigation
- Behavioral vs. Signature Analysis: Modern forensics emphasizes behavioral anomalies and system modifications over static signature matching

### Email & Social Engineering Forensics:
- Header Analysis Skills: Email headers reveal routing paths, authentication results, and true sender origins despite spoofing
- Typosquatting Recognition: Attackers register domains resembling legitimate organizations; forensic analysis identifies subtle character substitutions
- Attachment Analysis: Malicious attachments leverage macro execution, exploit kits, and dropper techniques requiring sandboxed forensic examination
- User Behavior Insights: Forensic email analysis reveals susceptibility patterns, informing targeted security awareness training

### System & Network Forensic Techniques:
- File Integrity Monitoring: Comparing current system state against known-good baselines reveals unauthorized modifications and persistence mechanisms
- Process Forensics: Analyzing running processes, parent-child relationships, and memory artifacts identifies malware execution and privilege escalation
- Network Traffic Analysis: Baseline establishment enables anomaly detection; C2 communication, DNS tunneling, and unusual port usage indicate compromise
- Timeline Analysis: Correlating timestamps across file system, registry, event logs, and network captures creates precise attack chronologies

### Chain of Custody & Legal Considerations:
- Documentation Standards: Every evidence interaction requires date, time, location, handler name, justification, and actions taken
- Access Control Principles: Least-privilege access with audit trails prevents evidence tampering and maintains investigation integrity
- Legal Admissibility: Proper chain of custody, write-blocking, hash verification, and expert testimony ensure evidence survives judicial scrutiny
- Ethical Responsibilities: Forensic investigators must remain objective, follow evidence without bias, and maintain strict confidentiality

### Incident Response Integration:
- Forensics-Informed Remediation: Technical findings directly guide containment, eradication, and recovery actions
- Root Cause Analysis: Forensic investigation reveals how attacks occurred, enabling targeted security improvements rather than generic patches
- Recommendation Development: Evidence-based recommendations address specific vulnerabilities, user behaviors, and control gaps identified during investigation
- Continuous Improvement: Post-incident forensic analysis updates detection rules, monitoring thresholds, and security policies
### Professional Competencies:
- Tool Mastery: Proficiency with FTK Imager and Autopsy requires understanding underlying forensic principles, not just button-clicking
- Analytical Thinking: Connecting disparate artifacts into coherent narratives requires systematic analysis and hypothesis testing
- Communication Skills: Translating technical forensic findings into clear, actionable reports for technical and non-technical stakeholders
- Continuous Learning: Attack techniques, encryption methods, and anti-forensic tools evolve constantly; investigators must maintain current skills and certifications

### Defense & Prevention Strategies:
- Security Awareness Training: Phishing simulations and regular training reduce user susceptibility to social engineering
- Email Security Controls: Advanced filtering, attachment sandboxing, and DMARC/DKIM/SPF implementation prevent malicious email delivery
- Endpoint Detection & Response: EDR tools provide behavioral monitoring, process analysis, and automated containment capabilities
- Network Segmentation: Limiting lateral movement through micro-segmentation and zero-trust architecture contains breaches
- Multi-Factor Authentication: MFA significantly reduces credential compromise impact even when passwords are stolen

## 📸 Screenshot:
🔒 Screenshot Restriction Notice

Screenshots from IBM SkillsBuild simulated lab environments are proprietary content and cannot be shared externally per IBM's academic integrity policy and terms of use.

Lab Completion Verified:
- ✅ Platform: IBM SkillsBuild
- ✅ Module Status: 100% COMPLETE
- ✅ Activities Completed: 
  - Forensic disk imaging with FTK Imager
  - Multi-source digital evidence analysis with Autopsy
  - Chain of custody procedure evaluation
  - Attack timeline reconstruction and root cause analysis
  - Forensic reporting and security recommendations
- ✅ Completion Date: 2026-05-28

Alternative Evidence: Comprehensive written documentation provided in sections above.   