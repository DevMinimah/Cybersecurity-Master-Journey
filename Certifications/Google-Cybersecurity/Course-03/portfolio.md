# Incident Analysis & Network Hardening Strategy

Framework Alignment: NIST Cybersecurity Framework (CSF) 2.0  
Scenario Context: Post-incident review and strategic remediation following a 2-hour ICMP Denial of Service (DoS) attack at a multimedia services company.

---

## Executive Summary
The multimedia company experienced a two-hour network outage when internal services suddenly stopped responding. The cybersecurity team determined the disruption was caused by a Denial of Service (DoS) attack, where a massive flood of incoming ICMP packets overwhelmed an unconfigured perimeter firewall. The incident management team responded by blocking the malicious traffic and taking non-critical services offline so that critical business operations could be restored.

---

### Identify
A malicious actor targeted the organization’s network with an ICMP flood attack, exploiting the lack of perimeter filtering. The outage impacted all internal resources, including critical web design servers and client marketing data. The team had to quickly identify which assets were essential to prioritize during the restoration process.

### Protect
To prevent recurrence, the cybersecurity team implemented strict firewall rate-limiting for incoming ICMP packets and enabled source IP verification to automatically drop spoofed traffic. Additionally, an Intrusion Detection and Prevention System (IDPS) was deployed to actively filter and block malicious traffic patterns in real-time.

### Detect
The team deployed network monitoring software to establish a baseline of normal daily traffic and configured automated alerts for abnormal spikes, such as sudden increases in ICMP requests. They also centralized all firewall and IDPS logs to a secure server to ensure continuous visibility and faster detection of future anomalies.

### Respond
For future incidents, the team will follow a newly developed DoS playbook to immediately isolate affected network segments and apply emergency firewall rules. They will analyze centralized network logs to trace the attack source and communicate clearly with internal staff and clients according to a defined escalation matrix.

### Recover
To recover from the ICMP flood, the team first blocked the malicious traffic at the perimeter firewall. Next, they intentionally stopped all non-critical network services to free up bandwidth. Critical systems, such as the web design servers, were then restored to a functioning state. Finally, once the attack subsided, the remaining non-critical services were safely brought back online.

### Govern
Leadership addressed the root organizational failure by establishing a "secure-by-default" policy, mandating that no network device operates without a verified baseline configuration. Clear ownership for perimeter security was explicitly assigned to the Network Security Team, ensuring regular audits and ongoing executive oversight of the company's security posture.

---

### 💡 Analyst’s Reflection
Analyzing this incident highlighted a critical lesson: technical failures are almost always symptoms of organizational gaps. My initial instinct was simply to block the ICMP traffic and tune the firewall. However, mapping the event to the Govern function of the NIST CSF made it clear that an unconfigured firewall is a policy failure, not just a technical oversight. A two-hour outage for a multimedia agency means missed client deadlines and damaged trust. This experience reinforced that effective cybersecurity requires bridging the gap between packet-level details and executive-level strategy, ensuring we fix not just the immediate vulnerability, but the organizational process that allowed it to exist.

---

📄 [View Full Strategy Document](./Incident_Analysis_Network_Hardening.md) | 📥 [Download PDF](./incident-report-analysis.pdf)

*Note: This document was developed as part of a cybersecurity portfolio project to demonstrate practical application of the NIST CSF 2.0 in post-incident analysis and strategic network hardening.*