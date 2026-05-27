# Module 11: Incident Response - Practical Activity

## 📅 Date Started: 2026-05-26
## 📅 Date Completed: 2026-05-27

## ⚠️ Disclaimer:
Every scenario is a simulation for practical educational purposes only. All activities are conducted in controlled learning environments to develop cybersecurity skills and knowledge. No real systems, networks, or data were accessed or modified.

## 🧪 Activity Type:
Scenario-based professional simulation: Acting as a security analyst to respond to a brute force attack incident at a technology company, including threat assessment, mitigation, ongoing monitoring setup, and comprehensive incident reporting.

## 🎯 Lab Goal:
To apply incident response frameworks by assessing a brute force attack threat through SIEM analysis, implementing immediate mitigation measures including firewall blocking and password policy updates, establishing continuous monitoring capabilities, and documenting comprehensive incident reports with lessons learned for organizational security improvement.

## 🛠 Tools Used:
- Adobe file editor
- Splunk Enterprise (SIEM platform)
- Network firewall configuration interface
- Microsoft Excel (incident documentation)
- Email communication system
- Password policy management tools
- Incident response framework (MITRE ATT&CK, Cyber Kill Chain)

## 📋 What I Did:

### Task 1: Assess the Threat
1. Scenario Setup: Assumed role as security analyst at a technology company reviewing exported SIEM report
2. Identified Brute Force Attack:
   - Analyzed SIEM report indicating high volume of failed login attempts
   - Identified malicious source IP address
   - Focused analysis on _raw column containing comprehensive log data
3. Examined Attack Patterns:
   - Reviewed multiple failed password attempts for invalid users
   - Identified targeted usernames (common and invalid accounts)
   - Analyzed timestamps showing coordinated attack timing
   - Examined port numbers and SSH protocol exploitation attempts
4. Assessed Attack Scope:
   - Determined attack targeted multiple user accounts systematically
   - Evaluated potential impact on web servers and authentication systems
   - Identified attack as brute force credential stuffing attempt

### Task 2: Mitigate the Threat
1. Immediate IP Blocking Actions:
   - Identified malicious IP address requiring immediate blocking
   - Accessed network firewall configuration interface
   - Navigated to firewall settings and access control rules section
   - Created new access control rule targeting identified IP
   - Set rule action to "Block" or "Deny"
   - Applied rule to incoming traffic to prevent further attack attempts
   - Saved and activated configuration changes
2. Password Policy Review and Enhancement:
   - Located and reviewed current password policy documentation
   - Analyzed existing requirements:
     - Minimum character length
     - Complexity requirements (numbers, special characters)
     - Password expiration period
     - No restriction on common passwords (identified gap)
   - Identified weaknesses in current policy allowing potential vulnerabilities
3. Security Settings Update:
   - Enhanced password requirements to address identified gaps
   - Implemented restrictions on common passwords
   - Strengthened complexity requirements
   - Updated system configurations to enforce new policy
4. User Communication:
   - Composed and sent organization-wide email explaining new password policy
   - Provided clear rationale for changes related to security incident
   - Included link to internal web page with detailed instructions
   - Offered tips and best practices for creating strong passwords
   - Ensured user awareness and compliance with new requirements

### Task 3: Ensure Ongoing Monitoring
1. Continuous Monitoring Setup:
   - Configured Splunk Enterprise for real-time log analysis
   - Established automated alerting for failed login attempt thresholds
   - Set up monitoring dashboards for authentication events
   - Implemented correlation rules to detect brute force patterns
2. Detection Rule Configuration:
   - Created alerts for multiple failed login attempts from single IP
   - Established baseline for normal authentication activity
   - Configured notifications for anomalous login patterns
   - Enabled rapid detection of similar future attacks
3. Monitoring Scope Expansion:
   - Ensured all web servers integrated into SIEM monitoring
   - Extended logging to authentication systems and access controls
   - Implemented comprehensive visibility across infrastructure

### Task 4: Report on Actions Taken
1. Incident Report Creation:
   - Compiled comprehensive incident report documenting all aspects of attack and response
   - Structured report for organizational understanding and future reference
2. Documented Timeline of Events:
   - Threat Detection:
     - Web team noticed unusual activity on web servers
     - Observed significant increase in failed login attempts
     - Promptly notified security team
     - Provided log files for detailed analysis
   - Log Analysis:
     - Security team uploaded logs into Splunk Enterprise
     - Utilized SIEM capabilities to process millions of records
     - Searched and filtered data to identify attack patterns
   - Attack Identification:
     - Confirmed brute force attack through Splunk analysis
     - Characterized by numerous failed login attempts from single IP
     - Documented attack methodology and scope
3. Threat Assessment Documentation:
   - Failed Login Analysis:
     - Detailed multiple failed login attempts from malicious IP
     - Listed targeted user IDs and accounts
     - Analyzed attack frequency and timing patterns
   - Successful Login Analysis:
     - Confirmed no successful login attempts from malicious IP
     - Validated attack did not compromise any accounts
     - Assessed overall security posture remained intact
4. Threat Mitigation Actions:
   - IP Address Blocking:
     - Documented blocking of malicious IP at firewall
     - Explained prevention of further attack attempts
   - Password Reset Initiative:
     - Initiated mandatory password reset for all users
     - Ensured integrity of user accounts
     - Prevented potential unauthorized access
5. Preventive Measures Implementation:
   - Continuous Monitoring:
     - Added web servers to Splunk for ongoing surveillance
     - Enabled rapid detection of future threats
   - Security Audits:
     - Scheduled periodic security audits
     - Planned regular vulnerability assessments
   - Employee Training:
     - Developed comprehensive cybersecurity training program
     - Educated employees on incident prevention and response
     - Emphasized employee role in maintaining security
     - Conducted regular training sessions on latest threats

### Incident Response Checklist Application:
1. Initial Analysis:
   - Reviewed incident details to identify security measure weaknesses
   - Gathered all relevant information about the brute force attack
   - Documented attack methods (credential stuffing, SSH exploitation)
   - Identified entry points (authentication systems, web servers)
2. Focus of Analysis:
   - Pinpointed gaps in existing security measures
   - Identified weaknesses that allowed attack to occur
   - Analyzed password policy inadequacies
   - Evaluated monitoring and detection capabilities
3. Action Plan Development:
   - Implemented immediate containment (IP blocking)
   - Established long-term preventive measures
   - Scheduled regular security audits
   - Developed employee training program
4. Employee Training Emphasis:
   - Ensured staff awareness of incident prevention
   - Conducted training on latest threats and response techniques
   - Emphasized employee role in organizational security

## 🔍 What I Found:

### Threat Assessment Findings:
- Attack Characteristics:
  - Single source IP conducting systematic brute force attack
  - Targeted multiple invalid and common usernames
  - Exploited SSH protocol on standard and non-standard ports
  - Rapid succession attempts indicating automated attack tool
  - No successful logins confirmed attack did not breach accounts
- SIEM Effectiveness:
  - Splunk Enterprise successfully processed millions of log records
  - _raw column provided comprehensive attack details
  - Search and filtering capabilities enabled rapid threat identification
  - Without SIEM, manual analysis would be impractical and impossible
- Attack Pattern Recognition:
  - Classic brute force characteristics: multiple usernames, single source, rapid attempts
  - Targeted common service accounts and weak credentials
  - SSH protocol exploitation attempting to gain unauthorized access

### Mitigation Effectiveness:
- Firewall Blocking:
  - Immediate IP blocking prevented continuation of attack
  - Access control rules effectively stopped malicious traffic
  - Firewall configuration changes applied successfully
  - Blocking at perimeter prevented internal system exposure
- Password Policy Gaps:
  - Previous policy lacked restrictions on common passwords
  - Expiration period adequate but complexity needed enhancement
  - No technical controls preventing weak password selection
  - User education on password strength was insufficient
- Policy Improvements:
  - Enhanced requirements addressed identified vulnerabilities
  - Common password restrictions eliminated obvious weaknesses
  - User communication ensured awareness and compliance
  - Training resources provided ongoing support

### Monitoring Capabilities:
- Continuous Surveillance:
  - Splunk integration enabled real-time threat detection
  - Automated alerts configured for failed login thresholds
  - Baseline establishment allowed anomaly detection
  - Correlation rules identified brute force patterns automatically
- Detection Speed:
  - Web team notification demonstrated effective human monitoring
  - SIEM analysis provided rapid technical investigation
  - Combined human and automated detection proved effective
  - Future attacks would be detected more quickly with enhanced monitoring

### Incident Response Process:
- Timeline Documentation:
  - Clear chronology enabled understanding of attack progression
  - Web team to security team handoff demonstrated effective communication
  - Log preservation maintained evidence integrity
  - Structured response followed incident response framework
- Team Coordination:
  - Web team identified anomaly and escalated appropriately
  - Security team performed technical analysis and mitigation
  - Cross-functional collaboration ensured comprehensive response
  - Roles and responsibilities clearly defined

### Security Gaps Identified:
- Password Policy Weaknesses:
  - No restriction on common passwords created vulnerability
  - User education insufficient to prevent weak credential selection
  - Technical enforcement needed beyond policy documentation
- Monitoring Coverage:
  - Online store activity not previously tracked in Splunk
  - Log analysis required manual upload indicating automation gap
  - Real-time alerting not configured for authentication events
- Preventive Controls:
  - Account lockout policies may not have been enforced
  - Multi-factor authentication not mentioned as control
  - Rate limiting on authentication attempts may be insufficient

## 💡 What I Learned:
### Incident Response Framework Application:
- Structured Approach: Following incident response phases (preparation, detection, analysis, containment, eradication, recovery, lessons learned) ensures comprehensive response without missing critical steps
- MITRE ATT&CK Framework: The brute force attack mapped to ATT&CK techniques including:
  - T1110.001: Brute Force - Password Guessing
  - T1078: Valid Accounts (attempted)
  - Understanding attacker TTPs (Tactics, Techniques, Procedures) improves detection and response
- Cyber Kill Chain: The attack was stopped at the "Exploitation" phase before achieving "Installation" or "Actions on Objectives," demonstrating value of early detection
- NIST Incident Response Lifecycle: Applied preparation, detection & analysis, containment eradication & recovery, and post-incident activity phases

### SIEM for Threat Detection:
- Log Analysis Power: SIEM tools like Splunk transform overwhelming log volumes into actionable intelligence; manual analysis of millions of records is impossible
- Search and Correlation: Advanced search capabilities and correlation rules detect patterns invisible in individual log entries
- Real-Time Monitoring: Continuous log ingestion and analysis enables rapid threat detection rather than delayed discovery
- Export and Reporting: Ability to export structured data supports incident documentation, management reporting, and evidence preservation

### Brute Force Attack Characteristics:
- Pattern Recognition: Brute force attacks exhibit identifiable patterns:
  - Single source IP with multiple username attempts
  - Rapid succession of failed logins
  - Targeting of common/invalid accounts
  - Automated tool usage (timing consistency)
- SSH Exploitation: SSH services are common brute force targets due to remote access capabilities
- Credential Stuffing: Attackers systematically try username/password combinations hoping for weak credentials
- No Success ≠ No Threat: Even unsuccessful brute force attacks indicate:
  - Active threat actors targeting organization
  - Need for enhanced monitoring and controls
  - Potential for future, more sophisticated attacks

### Immediate Mitigation Strategies:
- IP Blocking: Firewall-based IP blocking provides immediate containment but has limitations:
  - Attackers can use different IPs or botnets
  - Blocking is reactive, not preventive
  - Must be combined with other controls
- Password Policy Enhancement:
  - Technical enforcement more effective than policy alone
  - Common password restrictions eliminate obvious vulnerabilities
  - User education must accompany technical controls
  - Regular policy reviews ensure adaptation to emerging threats
- Mandatory Password Resets:
  - Proactive measure to eliminate potential compromise
  - Demonstrates security-first organizational culture
  - May cause temporary user inconvenience but prevents long-term damage

### Ongoing Monitoring Importance:
- Continuous Vigilance: Security is not one-time fix; requires continuous monitoring and adaptation
- Automated Detection: Automated alerts reduce reliance on manual log review and human vigilance
- Baseline Establishment: Understanding normal activity enables detection of anomalous behavior
- Rapid Response: Early detection through monitoring enables faster response, reducing potential impact

### Incident Documentation Value:
- Organizational Learning: Comprehensive incident reports create institutional knowledge for future incidents
- Management Communication: Clear documentation enables leadership understanding of threats and resource needs
- Compliance Requirements: Many regulations require incident documentation and reporting
- Legal Evidence: Properly documented incidents may support legal action against attackers
- Trend Analysis: Historical incident data reveals patterns and informs security strategy
### Employee Training Critical Role:
- Human Firewall: Employees are first line of defense; their awareness prevents many attacks
- Password Hygiene: Training on strong password creation reduces credential-based attack success
- Incident Reporting: Employees must know how to recognize and report suspicious activity
- Security Culture: Regular training fosters organizational security-conscious culture
- Evolving Threats: Ongoing education keeps staff updated on latest attack techniques

### Cross-Functional Collaboration:
- Team Coordination: Effective incident response requires coordination between web teams, security teams, IT operations, and management
- Clear Communication: Timely, accurate information sharing enables rapid response
- Defined Roles: Understanding who does what prevents confusion during incidents
- Escalation Procedures: Clear escalation paths ensure appropriate resource allocation

### Defense-in-Depth Strategy:
- Layered Controls: No single control is sufficient; multiple layers provide better protection:
  - Firewall (network layer)
  - Password policies (authentication layer)
  - Monitoring (detection layer)
  - Training (human layer)
- Compensating Controls: When one control has gaps, others compensate (e.g., monitoring compensates for password weaknesses)
- Continuous Improvement: Each incident reveals gaps; addressing them strengthens overall security posture

### Incident Response Best Practices:
- Preparation: Having tools, procedures, and trained personnel ready before incidents occur
- Rapid Containment: Quick action to stop attack progression minimizes damage
- Thorough Analysis: Understanding what happened, how it happened, and why it happened
- Eradication: Removing attacker access and closing vulnerabilities
- Recovery: Restoring systems and operations safely
- Lessons Learned: Applying incident insights to prevent future occurrences

## 📸 Screenshot:
🔒 Screenshot Restriction Notice

Screenshots from IBM SkillsBuild simulated lab environments are proprietary content and cannot be shared externally per IBM's academic integrity policy and terms of use.

Lab Completion Verified:
- ✅ Platform: IBM SkillsBuild
- ✅ Module Status: 100% COMPLETE
- ✅ Activities Completed: Threat assessment (brute force attack analysis), threat mitigation (IP blocking, password policy update), ongoing monitoring setup, incident reporting, incident response checklist application
- ✅ Completion Date: 2026-05-27

Alternative Evidence: Comprehensive written documentation provided in sections above.