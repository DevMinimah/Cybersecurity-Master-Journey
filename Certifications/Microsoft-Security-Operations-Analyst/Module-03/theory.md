# Module 3: Mitigate threats using Microsoft Purview

Learning Path: Mitigate threats using Microsoft Purview  
Date Started: June 26, 2026  
Date Completed: June 27, 2026  

---

## 1. Investigating and Responding to Data Loss Prevention (DLP) Alerts

### What I Learned:
- Understood how Microsoft Purview DLP policies identify, monitor, and automatically protect sensitive information (PII, financial data, IP) across Microsoft 365, on-premises, and cloud environments.
- Learned to triage DLP alerts in the compliance portal by analyzing policy matches, user actions, and severity levels to distinguish between true positives and false positives.
- Explored Endpoint DLP capabilities to monitor and restrict the movement of sensitive data on Windows, macOS, and Linux devices, including blocking unauthorized USB transfers or printing.
- Mastered response workflows: overriding false positives with business justifications, or escalating true positive data leaks to the incident response team.

---

## 2. Investigating Insider Risk Alerts and Related Activity

### What I Learned:
- Studied Insider Risk Management (IRM) as a critical tool for detecting malicious or inadvertent insider threats, such as data theft by departing users, IP leakage, or compliance violations.
- Utilized pre-built policy templates to detect specific risk patterns and correlated insider risk alerts with DLP alerts to build a comprehensive view of the user's behavior.
- Learned the importance of strict Role-Based Access Control (RBAC) and privacy controls within IRM to ensure that investigators only see the data they are authorized to review, protecting employee privacy during investigations.

---

## 3. Searching and Investigating with Microsoft Purview Audit

### What I Learned:
- Explored the foundational role of audit logs in security operations, understanding the difference between standard and advanced audit logs and their respective retention periods.
- Executed targeted audit log searches using filters for date ranges, specific users, activities, and workloads (Exchange, SharePoint, Entra ID) to reconstruct user actions.
- Analyzed audit records to trace the scope of unauthorized access, identify anomalous behavior, and establish a precise timeline of events during a security incident.
- Practiced exporting audit search results to CSV for deeper offline analysis or ingestion into external SIEM tools.

---

## 4. Searching for Content with Microsoft Purview eDiscovery

### What I Learned:
- Differentiated between eDiscovery (Standard) for basic searches and eDiscovery (Premium) for advanced case management, analytics, and review sets.
- Managed eDiscovery cases by adding custodians, placing legal holds to prevent data deletion, and defining search parameters across Exchange, SharePoint, OneDrive, and Teams.
- Executed complex content searches using keywords, metadata, and sensitive information types to locate specific data relevant to compliance or security investigations.
- Utilized Review sets to analyze, tag, and redact search results before exporting the preserved data for legal proceedings or internal incident scoping.

---

## 💡 Key Takeaways

1. Bridging Prevention and Response: While DLP and Insider Risk Management are proactive controls, the ability to deeply investigate their alerts is what turns a security policy into an effective incident response mechanism.

2. The Complexity of Insider Threats: Insider threats are uniquely difficult because the access is legitimate. Correlating Audit, DLP, and Insider Risk data is the only way to establish context and intent.

3. Audit Logs are the Source of Truth: In any investigation, audit logs provide the foundational, immutable timeline of user actions. Mastering Audit search is a non-negotiable skill for a SOC analyst.

4. eDiscovery is a Security Tool: eDiscovery isn't just for legal teams; security analysts rely on it to scope breaches, identify exactly what sensitive data was accessed, and preserve volatile evidence before it is deleted.

5. Privacy and Investigation must Coexist: Tools like Insider Risk Management require strict privacy boundaries. Effective security operations must balance aggressive threat hunting with strict adherence to data privacy and RBAC.

---

## 🔗 Links & Resources

- [Microsoft Learn: SC-200 Security Operations Analyst](https://learn.microsoft.com/en-us/certifications/exams/sc-200)
- [Microsoft Purview Documentation](https://learn.microsoft.com/en-us/purview/)
- [Data Loss Prevention (DLP) Overview](https://learn.microsoft.com/en-us/purview/dlp-learn-about-dlp)
- [Insider Risk Management Overview](https://learn.microsoft.com/en-us/purview/insider-risk-management)
- [Audit in Microsoft Purview](https://learn.microsoft.com/en-us/training/modules/purview-audit-search-investigate/)
- [eDiscovery Solutions in Microsoft Purview](https://learn.microsoft.com/en-us/purview/edisc)

---

*🔙 [Back to Microsoft SC-200 Learning Path](../index.md)*