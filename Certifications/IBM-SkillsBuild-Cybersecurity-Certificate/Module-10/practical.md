# Module 10: Security Monitoring - Practical Activity

## 📅 Date Started: 2026-05-24
## 📅 Date Completed: 2026-05-25

## ⚠️ Disclaimer:
Every scenario is a simulation for practical educational purposes only. All activities are conducted in controlled learning environments to develop cybersecurity skills and knowledge. No real systems, networks, or data were accessed or modified.

## 🧪 Activity Type:
Scenario-based professional simulation: Acting as a cybersecurity professional to perform network reconnaissance using scanning tools, implement endpoint detection and response (EDR) solutions, and conduct threat investigation using SIEM technology (Splunk Enterprise) across multiple organizational contexts.

## 🎯 Lab Goal:
To develop comprehensive security monitoring capabilities by performing network reconnaissance using command-line tools and network scanning utilities, applying endpoint management principles through EDR tool implementation, and conducting threat investigation using Splunk Enterprise to detect, analyze, and document potential cyber threats including brute force attacks.

## 🛠 Tools Used:
- Command Prompt/CLI (network reconnaissance commands)
- Zenmap/Nmap (network scanning and topology visualization)
- EDR (Endpoint Detection and Response) tool
- Splunk Enterprise (SIEM platform)
- Microsoft Excel (log analysis and reporting)
- Regular expressions (Splunk query language)

## 📋 What I Did:

### Task 1: Network Reconnaissance Using Network Scanning Tools
1. Scenario Setup: Assumed role as cybersecurity professional at a financial services company preparing for security audit
2. Explored Command Prompt: Utilized CLI tools to gather initial network information and perform basic reconnaissance
3. Configured Network Scan:
   - Executed aggressive network scan with OS detection, version detection, script scanning, and traceroute
   - Applied aggressive timing template for efficient scanning
   - Enabled verbose output for detailed results
4. Analyzed Scan Results:
   - Identified multiple active hosts on the network
   - Reviewed open ports across various hosts
   - Examined host status, uptime, and system information
   - Interpreted vulnerability indicators based on open port counts
5. Prioritized Vulnerabilities: Used scan data to identify which systems required immediate security hardening before audit

### Task 2: Endpoint Security Quest with EDR Tool
1. Scenario Setup: Joined an automotive manufacturing company as security analyst responding to multiple endpoint attacks
2. Implemented EDR Solution:
   - Deployed endpoint detection and response tool across organizational infrastructure
   - Installed EDR agents on endpoints (workstations, servers, network devices)
   - Configured security policies and detection rules tailored to manufacturing environment
3. Established Monitoring Framework:
   - Set up real-time monitoring dashboards for endpoint visibility
   - Configured alert thresholds for suspicious activities
   - Defined escalation procedures for different threat severity levels
4. Developed Incident Response Protocols:
   - Created playbooks for common endpoint threats (malware, ransomware, unauthorized access)
   - Established containment, eradication, and recovery procedures
   - Integrated EDR alerts with broader security operations workflow

### Task 3: Threat Investigation Using Splunk Enterprise
1. Scenario Setup: Worked as security professional at a video game company investigating increased failed login attempts at online store
2. Uploaded Log Files to Splunk:
   - Accessed Splunk Enterprise configuration interface
   - Selected data source for web environment logs
   - Configured input settings for log ingestion
   - Successfully uploaded log files containing millions of records
   3. Configured Splunk Search Parameters:
   - Applied regular expression to sort events by host names
   - Understood expression components including escape characters, wildcards, and pattern matching
   - Started searching through indexed data
4. Analyzed Search Results:
   - Filtered through massive log dataset to identify patterns
   - Discovered evidence of brute force attack:
     - Multiple failed password attempts for invalid users
     - Systematic username enumeration attempts
     - All attempts originating from single IP address
     - Sequential port usage indicating automated attack
     - SSH protocol exploitation attempts
     - Timestamps showing coordinated attack pattern
5. Created and Exported Results Table:
   - Generated table displaying: time, client IP, host, source, sourcetype, and raw log data
   - Exported table to Microsoft Excel format
   - Documented findings for incident report inclusion
   - Provided actionable intelligence for security team response

## 🔍 What I Found:

### Network Reconnaissance Findings:
- GUI-Based Scanning Effectiveness: The graphical network scanning interface provided comprehensive network visualization with topology mapping, making it easier to identify network structure and potential entry points
- Host Discovery: Scanning revealed multiple active hosts, some with multiple open ports indicating potential vulnerabilities
- Vulnerability Indicators: Visual icon system provided quick assessment of risk levels based on open port counts
- Timing and Aggressiveness: Aggressive timing options balanced speed with accuracy, though in production environments, timing must be adjusted to avoid network disruption
- Information Gathering: Comprehensive scan flags revealed OS versions, service versions, and potential misconfigurations critical for audit preparation
- Audit Preparation Value: Proactive scanning before external audit allows internal teams to remediate vulnerabilities before attackers or auditors discover them

### EDR Implementation Findings:
- Endpoint Visibility: EDR tools provide granular visibility into endpoint activities that traditional antivirus cannot detect, including behavioral patterns and lateral movement
- Automated Response: Pre-configured policies enable automatic containment of threats without waiting for analyst intervention, reducing dwell time
- Centralized Management: Single console management of distributed endpoints simplifies security operations for organizations with remote workers and multiple offices
- Threat Intelligence Integration: EDR platforms integrate threat feeds to identify known malicious indicators across all endpoints simultaneously
- Manufacturing Sector Risks: The scenario highlighted that industrial and manufacturing companies face unique endpoint threats targeting intellectual property, operational technology, and supply chain systems

### Splunk Threat Investigation Findings:
- SIEM Power: Splunk successfully processed millions of log records that would be impossible to analyze manually, demonstrating SIEM essential value for modern security operations
- Brute Force Pattern Recognition: The attack showed classic brute force characteristics:
  - Single source IP attempting multiple username/password combinations
  - Targeting common service accounts and weak passwords
  - Rapid succession attempts (multiple attempts within same second)
  - SSH protocol exploitation
  - Invalid user enumeration to discover valid accounts
- Log Analysis Complexity: Without Splunk's search capabilities and regular expressions, identifying this attack pattern across millions of records would require impractical manual effort
- Regex Importance: Regular expressions enabled efficient sorting and filtering by host, demonstrating that security analysts need regex skills for effective SIEM operation
- Export Capability: The ability to export structured data to Excel enables:
  - Sharing findings with non-technical stakeholders
  - Long-term archival outside SIEM retention limits
  - Integration with incident management systems
  - Evidence preservation for potential legal action
- Incident Response Value: The exported table provided concrete evidence (timestamps, IP addresses, attempted usernames) needed for:
  - Blocking malicious IP at firewall
  - Notifying affected users if any accounts were compromised
  - Reporting to security leadership and potentially law enforcement
  - Updating detection rules to catch similar attacks

## 💡 What I Learned:

### Network Reconnaissance Skills:
- Proactive Security Posture: Regular network scanning is essential for maintaining security awareness; you cannot protect what you don't know exists
- Tool Selection: GUI-based scanning tools provide user-friendly visualization while maintaining powerful scanning capabilities, making them ideal for both beginners and experienced professionals
- Scan Profile Customization: Different scenarios require different scan intensities; aggressive scans are fast but may trigger IDS/IPS, while stealth scans take longer but avoid detection
- Vulnerability Prioritization: Not all open ports are equally risky; understanding which services run on which ports helps prioritize remediation efforts based on business impact
- Audit Preparation: Performing internal reconnaissance before external audits reveals vulnerabilities early, allowing remediation without audit findings or compliance failures
- Legal and Ethical Considerations: Network scanning must only be performed on authorized networks; unauthorized scanning violates computer crime laws and organizational policies

### Endpoint Security Management:
- Defense-in-Depth: EDR complements but doesn't replace traditional security controls; layered defense provides better protection than any single tool
- Agent Deployment Strategy: Successful EDR implementation requires comprehensive agent coverage; unmanaged endpoints become blind spots attackers exploit
- Policy Configuration Balance: Overly restrictive policies generate alert fatigue and user frustration; overly permissive policies miss threats; finding the right balance requires continuous tuning
- Incident Response Integration: EDR alerts must trigger defined response procedures; without clear playbooks, alerts become noise rather than actionable intelligence
- Industry-Specific Risks: Different sectors have unique endpoint security needs including OT/IT convergence, legacy system support, and intellectual property protection
- Remote Work Challenges: Distributed workforces require cloud-managed EDR solutions that function effectively outside corporate network perimeter

### SIEM and Threat Investigation:
- Data Volume Management: Modern organizations generate terabytes of security logs; SIEM tools are not optional but essential for processing, correlating, and analyzing this data
- Pattern Recognition: Brute force attacks follow predictable patterns (same source, multiple usernames, rapid succession); understanding these patterns enables faster detection
- Regular Expression Mastery: Regex skills are fundamental for effective SIEM operation; analysts who master expressions can extract insights that point-and-click interfaces cannot provide
- Log Source Integration: Comprehensive security monitoring requires ingesting logs from diverse sources (firewalls, servers, applications, endpoints); gaps in log coverage create blind spots
- Incident Documentation: Exporting and formatting investigation results is as important as the investigation itself; clear documentation enables:
- Management decision-making
  - Regulatory compliance reporting
  - Legal proceedings
  - Knowledge transfer between security team members
  - Historical trend analysis
- Threat Intelligence Application: Identified attack patterns should trigger:
  - Immediate blocking at perimeter
  - Search across historical logs for same indicators
  - Sharing with threat intelligence platforms
  - Updating detection rules for future prevention
- SIEM Query Optimization: Efficient searches reduce resource consumption and return faster results; understanding how SIEM platforms index and search data improves investigation speed
- Attack Timeline Analysis: Attacks often occur in bursts; continuous monitoring ensures rapid detection rather than delayed discovery
- Username Enumeration Defense: Attacks targeting common usernames demonstrate the need for implementing account lockout policies, strong password requirements, and multi-factor authentication


## 📸 Screenshot:
🔒 Screenshot Restriction Notice

Screenshots from IBM SkillsBuild simulated lab environments are proprietary content and cannot be shared externally per IBM's academic integrity policy and terms of use.

Lab Completion Verified:
- ✅ Platform: IBM SkillsBuild
- ✅ Module Status: 100% COMPLETE
- ✅ Activities Completed: Network reconnaissance (scanning tools), EDR implementation, Splunk Enterprise threat investigation
- ✅ Completion Date: 2026-05-25

Alternative Evidence: Comprehensive written documentation provided in sections above.