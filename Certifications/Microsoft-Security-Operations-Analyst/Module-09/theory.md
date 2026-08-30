# Learning Path 09: Create detections and perform investigations using Microsoft Sentinel

## 📅 Date Started: 2026-08-27
## 📅 Date Completed: 2026-08-28

---

## 🎯 What I Learned

### 1. Threat detection with Microsoft Sentinel analytics
- Explored Microsoft Sentinel Analytics as the core engine for generating security alerts and detecting threats.
- Studied the different types of analytics rules, including Scheduled, Near-Real-Time (NRT), and Machine Learning Behavioral Analytics.
- Learned how to create and customize analytics rules using both built-in templates and the custom rule wizard, and understood how to manage and tune existing rules to reduce false positives.

### 2. Automation in Microsoft Sentinel
- Studied the various automation options available within Sentinel to streamline SOC workflows.
- Learned how to create and configure Automation Rules to automatically assign incidents, change statuses, and trigger downstream actions based on specific alert or incident criteria.

### 3. Threat response with Microsoft Sentinel playbooks
- Explored Microsoft Sentinel Playbooks (built on Azure Logic Apps) as the primary mechanism for orchestrating automated threat response.
- Learned how to trigger playbooks in real-time via Automation Rules and how to run them on-demand for manual incident response tasks.
- Understood how playbooks integrate with third-party APIs to automate actions like blocking IPs, isolating hosts, or notifying stakeholders.

### 4. Security incident management in Microsoft Sentinel
- Studied the anatomy of security incidents, understanding how multiple related alerts are grouped into a single incident for investigation.
- Learned how to analyze incident evidence and entities (users, hosts, IPs) to determine the blast radius and context of an attack.
- Explored the incident management lifecycle, practicing how to investigate, triage, and resolve incidents within the Sentinel portal.

### 5. Identify threats with Behavioral Analytics
- Explored Behavioral Analytics to detect anomalous activities and insider threats that bypass traditional signature-based detections.
- Learned how to explore entities and display entity behavior information to establish a baseline of normal activity.
- Studied how to implement and tune Anomaly Detection analytical rule templates to identify deviations in user and entity behavior over time.

### 6. Data normalization in Microsoft Sentinel
- Studied the critical concept of data normalization to ensure logs from diverse vendors are structured uniformly.
- Learned how to use and create Advanced Security Information Model (ASIM) parsers to normalize data into standard schemas.
- Explored parameterized KQL functions to write reusable, vendor-agnostic queries.
- Understood how to configure Azure Monitor Data Collection Rules (DCRs) to filter and normalize data at the ingestion level.

### 7. Query, visualize, and monitor data in Microsoft Sentinel
- Explored Microsoft Sentinel Workbooks as a powerful tool for querying, visualizing, and monitoring security data.
- Learned how to use default, out-of-the-box Workbooks and how to build custom Workbooks from scratch using KQL and interactive visual elements.
- Studied how to create interactive dashboards that provide stakeholders with clear, actionable insights into the organization's security posture.

---

## 💡 Key Takeaways

- **Automation is the Key to SOC Scalability:** Manual incident triage does not scale. Combining Automation Rules with Playbooks (Logic Apps) shifts the SOC from a reactive, alert-fatigued team to a proactive, highly efficient operation.
- **Context is Everything in Incident Management:** An alert is just a data point; an incident is a story. Grouping alerts and analyzing the associated entities and evidence is what allows an analyst to understand the true scope and impact of a breach.
- **Normalization Unlocks True Threat Hunting:** Without data normalization (ASIM), analysts must write different KQL queries for every different firewall or EDR vendor. Normalizing data allows for a single, unified query to hunt across the entire environment.
- **Behavioral Analytics Catches the "Unknown Unknowns":** Signature-based rules catch known bad. Behavioral analytics and anomaly detection are essential for catching compromised credentials, insider threats, and novel attack techniques that lack known signatures.

---

## 🔗 Links/Resources

- [Microsoft Learn: SC-200 Security Operations Analyst](https://learn.microsoft.com/en-us/certifications/exams/sc-200)
- [Detect threats with built-in analytics rules](https://learn.microsoft.com/en-us/azure/sentinel/tutorial-detect-threats-built-in)
- [Automate incident handling with automation rules](https://learn.microsoft.com/en-us/azure/sentinel/automate-incident-handling-with-automation-rules)
- [Automate responses with playbooks](https://learn.microsoft.com/en-us/azure/sentinel/automate-responses-with-playbooks)
- [Investigate incidents in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/investigate-cases)
- [Behavioral analytics in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/behavioral-analytics)
- [Advanced Security Information Model (ASIM) overview](https://learn.microsoft.com/en-us/azure/sentinel/normalization-about)
- [Visualize your data with Microsoft Sentinel Workbooks](https://learn.microsoft.com/en-us/azure/sentinel/visualize-your-data)

---

**🎓 Microsoft Certified: Security Operations Analyst Associate (SC-200) | Learning Path 09: Create detections and perform investigations using Microsoft Sentinel**

---

*Note: This document represents knowledge consolidation, personal realization, and a mindset shift from passive user to active defender — foundational to my growth in cybersecurity operations.*

*🔙 [Back to Microsoft SC-200](../README.md)*
