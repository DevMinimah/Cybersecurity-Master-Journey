# Learning Path 08: Connect logs to Microsoft Sentinel

## 📅 Date Started: 2026-08-24
## 📅 Date Completed: 2026-08-25

---

## 🎯 What I Learned

### 1. Connect data to Microsoft Sentinel using data connectors
- Explored data connectors as the primary mechanism for ingesting log data into Microsoft Sentinel.
- Studied the different data connector providers (Microsoft, Partner, Community) and learned how to view and manage connected hosts within the workspace.

### 2. Connect Microsoft services to Microsoft Sentinel
- Learned how to plan for and connect native Microsoft services to centralize telemetry.
- Studied the specific configuration steps for the Microsoft 365, Microsoft Entra, Microsoft Entra ID Protection, and Azure Activity connectors to ensure comprehensive visibility across identity, cloud, and productivity environments.

### 3. Connect Microsoft Defender XDR to Microsoft Sentinel
- Explored the integration of Microsoft Defender XDR and Microsoft Defender for Cloud to unify Extended Detection and Response (XDR) telemetry.
- Studied the process of connecting Microsoft Defender for IoT and understood the transition from legacy Defender connectors to the unified, modern Defender XDR connector.

### 4. Connect Windows hosts to Microsoft Sentinel
- Learned the methods for collecting Windows security events, comparing the modern Azure Monitor Agent (AMA) connector with the legacy Microsoft Monitoring Agent (MMA).
- Studied how to collect, configure, and ingest detailed Sysmon event logs to achieve advanced endpoint visibility and behavioral tracking.

### 5. Connect Common Event Format logs to Microsoft Sentinel
- Explored the Common Event Format (CEF) connector to ingest and normalize logs from external, non-Microsoft security solutions (such as third-party firewalls, proxies, and legacy SIEMs).

### 6. Connect syslog data sources to Microsoft Sentinel
- Studied how to plan and configure syslog data collection from Linux-based sources and network appliances.
- Learned how to configure Data Collection Rules (DCRs) for syslog data sources and practiced parsing raw syslog data using KQL to extract actionable fields.

### 7. Connect threat indicators to Microsoft Sentinel
- Explored threat intelligence connectors, including the Defender Threat Intelligence connector, the TAXII connector, and the Upload API connector.
- Learned how to view, manage, and query ingested threat indicators using KQL to proactively match internal telemetry against known Indicators of Compromise (IOCs).

---

## 💡 Key Takeaways

- **Data Ingestion is the Lifeblood of a SIEM:** A SIEM is only as effective as the data it ingests. Properly planning and configuring data connectors ensures comprehensive visibility without overwhelming storage costs or generating excessive noise.
- **AMA and DCRs are the Modern Standard:** The shift from the legacy MMA to the Azure Monitor Agent (AMA) and Data Collection Rules (DCRs) represents a crucial modernization in how Microsoft handles telemetry, offering better performance, granular filtering, and centralized management.
- **Unified XDR Telemetry Breaks Down Silos:** Connecting Defender XDR and Defender for Cloud natively provides a holistic view of identity, endpoint, cloud, and email security in a single pane of glass, drastically reducing context-switching for analysts.
- **Standardization is Key for Third-Party Logs:** Using standard formats like CEF and Syslog is essential for integrating third-party tools, ensuring that external telemetry is normalized, structured, and queryable alongside native Microsoft logs.

---

## 🔗 Links/Resources

- [Microsoft Learn: SC-200 Security Operations Analyst](https://learn.microsoft.com/en-us/certifications/exams/sc-200)
- [Connect data sources to Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/connect-data-sources)
- [Connect Microsoft 365 to Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/connect-office-365)
- [Connect Azure Activity logs to Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/connect-azure-activity)
- [Connect Microsoft Defender XDR to Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/connect-microsoft-defender-xdr)
- [Connect Windows Security Events via AMA](https://learn.microsoft.com/en-us/azure/sentinel/connect-windows-security-events-ama)
- [Connect Common Event Format (CEF) logs](https://learn.microsoft.com/en-us/azure/sentinel/connect-common-event-format)
- [Connect Syslog data sources to Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/connect-syslog)
- [Connect Threat Intelligence platforms (TIP/TAXII)](https://learn.microsoft.com/en-us/azure/sentinel/connect-threat-intelligence-tip)

---

**🎓 Microsoft Certified: Security Operations Analyst Associate (SC-200) | Learning Path 08: Connect logs to Microsoft Sentinel**

---

*Note: This document represents knowledge consolidation, personal realization, and a mindset shift from passive user to active defender — foundational to my growth in cybersecurity operations.*

*🔙 [Back to Microsoft SC-200](../README.md)*
