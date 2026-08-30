# Learning Path 10: Perform threat hunting in Microsoft Sentinel

## 📅 Date Started: 2026-08-28
## 📅 Date Completed: 2026-08-30

---

## 🎯 What I Learned

### 1. Explain threat hunting concepts in Microsoft Sentinel
- Explored the core concepts of proactive cybersecurity threat hunting, distinguishing it from reactive alert investigation.
- Studied how to develop and formulate testable hypotheses based on threat intelligence, observed anomalies, or known attacker behaviors.
- Learned to leverage the MITRE ATT&CK framework to map adversary tactics, techniques, and procedures (TTPs) and guide the hunting process.

### 2. Threat hunting with Microsoft Sentinel
- Explored the creation, execution, and management of custom threat-hunting queries using Kusto Query Language (KQL).
- Learned how to save key findings using bookmarks to preserve evidence, context, and specific log entries for future investigations.
- Studied how to track, manage, and collaborate on threat-hunting investigations over time using the dedicated Hunts feature in Sentinel.

### 3. Use Search jobs in Microsoft Sentinel
- Studied the Search Jobs feature to perform large-scale, long-running queries across massive datasets without experiencing query timeouts.
- Learned how to use Search Jobs to restore and query historical data that has been moved to the Archive tier, ensuring no hidden threats are missed due to data retention policies.

### 4. Hunt for threats using notebooks in Microsoft Sentinel
- Explored the integration of Jupyter Notebooks within Microsoft Sentinel to access, analyze, and visualize data using external tools like Python.
- Learned how to create, configure, and run notebooks directly within the Sentinel workspace.
- Studied how to explore and utilize pre-built notebook code (such as the Microsoft Sentinel Notebooks library) to perform advanced data science, machine learning, and deep-dive threat hunting.

---

## 💡 Key Takeaways

- **Proactive vs. Reactive Defense:** Threat hunting shifts the SOC from simply waiting for alerts to actively searching for hidden adversaries who may have bypassed automated detections.
- **Hypothesis-Driven Approach:** Effective hunting isn't random; it's driven by structured hypotheses and mapped to frameworks like MITRE ATT&CK to ensure comprehensive coverage of potential attack vectors.
- **Scale and History are Critical:** Search Jobs and Archive tier restoration are essential capabilities for hunting across massive historical datasets without performance bottlenecks, ensuring long-dwelling threats can be uncovered.
- **Data Science Meets Security:** Integrating Python and Jupyter Notebooks brings advanced data science and machine learning capabilities directly into the SIEM, allowing analysts to uncover complex, multi-stage attacks that standard KQL queries might miss.

---

## 🔗 Links/Resources

- [Microsoft Learn: SC-200 Security Operations Analyst](https://learn.microsoft.com/en-us/certifications/exams/sc-200)
- [A Getting Started Guide for Azure Sentinel ML Notebooks](https://nbviewer.org/github/Azure/Azure-Sentinel-Notebooks/blob/master/A%20Getting%20Started%20Guide%20For%20Azure%20Sentinel%20ML%20Notebooks.ipynb)
- [MSTICPy Documentation](https://msticpy.readthedocs.io/)
- [Become a Microsoft Sentinel Ninja (Level 400)](https://techcommunity.microsoft.com/t5/azure-sentinel/become-an-azure-sentinel-ninja-the-complete-level-400-training/ba-p/1246310)
- [Threat hunting overview in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/hunting-overview)
- [Track threat hunting with hunts and bookmarks](https://learn.microsoft.com/en-us/azure/sentinel/hunting-bookmarks)
- [Use Search jobs to query large datasets](https://learn.microsoft.com/en-us/azure/sentinel/search-jobs)
- [Restore archived log data in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/logs-archive-restore)
- [Use notebooks in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/notebooks)
- [Microsoft Sentinel Notebooks on GitHub](https://github.com/Azure/Azure-Sentinel-Notebooks)

---

**🎓 Microsoft Certified: Security Operations Analyst Associate (SC-200) | Learning Path 10: Perform threat hunting in Microsoft Sentinel**

---

*Note: This document represents knowledge consolidation, personal realization, and a mindset shift from passive user to active defender — foundational to my growth in cybersecurity operations.*

*🔙 [Back to Microsoft SC-200](../README.md)*
