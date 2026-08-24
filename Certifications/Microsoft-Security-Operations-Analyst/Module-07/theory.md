# Learning Path 07: Configure your Microsoft Sentinel environment

## 📅 Date Started: 2026-08-23
## 📅 Date Completed: 2026-08-24

---

## 🎯 What I Learned

### 1. Introduction to Microsoft Sentinel
- Explored the core architecture and purpose of Microsoft Sentinel as a cloud-native Security Information and Event Management (SIEM) and Security Orchestration, Automation, and Response (SOAR) solution.
- Studied how Sentinel works by ingesting data, detecting threats, investigating incidents, and automating responses across the enterprise.
- Learned the ideal use cases for Microsoft Sentinel, particularly for organizations needing scalable, centralized security operations and unified visibility.

### 2. Create and manage Microsoft Sentinel workspaces
- Studied the planning considerations for deploying a Microsoft Sentinel workspace, including data residency, retention policies, and cost management.
- Learned how to create and configure a workspace, and explored managing workspaces across multiple tenants using Azure Lighthouse for centralized administration.
- Understood Microsoft Sentinel permissions and roles (e.g., Reader, Contributor, Security Reader, Security Admin) and how to manage workspace settings and configure log ingestion.

### 3. Query logs in Microsoft Sentinel
- Explored the Logs page and learned how to query data using Kusto Query Language (KQL) to investigate security events.
- Studied the structure of Microsoft Sentinel tables, focusing on common tables (like `SecurityEvent`, `SigninLogs`) and Microsoft Defender XDR tables (like `DeviceEvents`, `AlertInfo`) to understand where specific telemetry lives.

### 4. Use watchlists in Microsoft Sentinel
- Learned how to plan for and use watchlists to enrich security data with external, business-specific information (e.g., VIP users, trusted IPs, critical assets).
- Studied the process of creating watchlists from CSV files and managing them to keep threat hunting and detection rules highly contextual and accurate.

### 5. Utilize threat intelligence in Microsoft Sentinel
- Explored the concept of threat intelligence and how it integrates into Sentinel to proactively identify malicious activity based on known Indicators of Compromise (IOCs).
- Learned how to manage threat indicators via the Threat Intelligence platform (TIP) and used KQL to query and view threat intelligence data directly within the workspace.

### 6. Integrate Microsoft Defender XDR with Microsoft Sentinel
- Studied the benefits of integrating Microsoft Sentinel with Microsoft Defender XDR for unified Extended Detection and Response (XDR).
- Explored the capability differences between the standalone portals and learned the onboarding process to seamlessly connect them.
- Understood how to leverage Microsoft Sentinel features directly within the Microsoft Defender XDR portal for a cohesive, unified analyst experience.

---

## 💡 Key Takeaways

- **Centralization is the Foundation of Modern SOC:** Microsoft Sentinel acts as the central nervous system for security, aggregating data from across the entire Microsoft ecosystem and third-party sources to eliminate silos.
- **Data Structure Drives Query Efficiency:** Understanding the specific schemas of common tables and Defender XDR tables is crucial for writing efficient, accurate KQL queries and avoiding performance bottlenecks.
- **Context Enriches Detection:** Watchlists and Threat Intelligence are not just add-ons; they are critical for adding business context to raw telemetry, which drastically reduces false positives and highlights true risks.
- **XDR Unifies the Analyst Experience:** Integrating Sentinel with Defender XDR breaks down operational silos, allowing analysts to pivot seamlessly between SIEM data and endpoint/email/identity telemetry without context switching.

---

## 🔗 Links/Resources

- [Microsoft Learn: SC-200 Security Operations Analyst](https://learn.microsoft.com/en-us/certifications/exams/sc-200)
- [Microsoft Sentinel Overview](https://learn.microsoft.com/en-us/azure/sentinel/overview)
- [Onboard Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/quickstart-onboard)
- [Manage Microsoft Sentinel with Azure Lighthouse](https://learn.microsoft.com/en-us/azure/sentinel/azure-lighthouse)
- [Microsoft Sentinel Roles and Permissions](https://learn.microsoft.com/en-us/azure/sentinel/roles)
- [Microsoft Sentinel Data Schema and Tables](https://learn.microsoft.com/en-us/azure/sentinel/data-schema)
- [Use watchlists with Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/watchlists)
- [Manage threat intelligence in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/manage-threat-intelligence)
- [Connect Microsoft Defender XDR to Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/connect-microsoft-defender-xdr)

---

**🎓 Microsoft Certified: Security Operations Analyst Associate (SC-200) | Learning Path 07: Configure your Microsoft Sentinel environment**

---

*Note: This document represents knowledge consolidation, personal realization, and a mindset shift from passive user to active defender — foundational to my growth in cybersecurity operations.*

*🔙 [Back to Microsoft SC-200](../README.md)*
