# Learning Path 06: Create queries for Microsoft Sentinel using Kusto Query Language (KQL)

## 📅 Date Started: 2026-08-22
## 📅 Date Completed: 2026-08-23

---

## 🎯 What I Learned

### 1. Construct KQL statements for Microsoft Sentinel
- Explored the fundamental structure and syntax of the Kusto Query Language (KQL), understanding how statements are built and executed.
- Learned how to use core operators to filter and shape data, including `search` for broad text searches, `where` for precise conditional filtering, and `let` for defining variables and improving query readability.
- Studied how to manipulate and format output using the `extend` operator to create calculated columns, `order by` to sort results, and `project` to select specific columns for the final output.

### 2. Analyze query results using KQL
- Studied the powerful `summarize` operator to aggregate data, learning how to group results and apply aggregation functions (like `count`, `sum`, `avg`) to filter and prepare large datasets for analysis.
- Explored the `render` operator, understanding how to transform raw query results into visual charts (such as bar charts, time charts, and pie charts) directly within the query results pane.

### 3. Build multi-table statements using KQL
- Learned how to combine data from multiple tables using the `union` operator to append rows from different tables with similar schemas.
- Studied the `join` operator to correlate data across disparate tables based on a common key, understanding the different join strategies (e.g., inner, left outer) to map complex relationships between entities.

### 4. Work with data in Microsoft Sentinel using Kusto Query Language
- Explored techniques for parsing and extracting valuable telemetry from unstructured string fields using operators like `parse` and regular expressions (`extract`).
- Studied how to extract data from structured string formats (like JSON or CSV) using `parse_json` and `split` to normalize complex log payloads.
- Learned how to integrate external data into queries and create custom parsers using KQL functions to standardize log ingestion and streamline recurring investigative queries.

---

## 💡 Key Takeaways

- **KQL is the Backbone of Sentinel:** Mastering KQL is non-negotiable for a Sentinel analyst. It is the primary language for hunting threats, building custom detection rules, and investigating incidents.
- **Data Normalization is Critical:** Real-world logs are rarely perfectly structured. Knowing how to parse, extract, and normalize unstructured or semi-structured string data (like JSON) is what separates a basic query writer from an advanced threat hunter.
- **Context Requires Correlation:** Security incidents rarely live in a single table. The ability to seamlessly `join` and `union` disparate data sources (e.g., correlating network flow logs with endpoint process logs) is essential for mapping the full attack chain.
- **Visualizations Drive Action:** Raw data is hard to digest quickly. Using the `render` operator to create immediate visualizations helps analysts spot anomalies, trends, and spikes in malicious activity at a glance.

---

## 🔗 Links/Resources

- [Microsoft Learn: SC-200 Security Operations Analyst](https://learn.microsoft.com/en-us/certifications/exams/sc-200)
- [Kusto Query Language (KQL) overview](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/)
- [Azure Monitor log query tutorial](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/kql-tutorial)
- [KQL operators reference (where, project, summarize, join, etc.)](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/)
- [Parse and extract data in KQL](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/parseoperator)
- [Microsoft Sentinel documentation](https://learn.microsoft.com/en-us/azure/sentinel/)
- [Write queries in Microsoft Sentinel](https://learn.microsoft.com/en-us/azure/sentinel/queries)

---

**🎓 Microsoft Certified: Security Operations Associate (SC-200) | Learning Path 06: Create queries for Microsoft Sentinel using Kusto Query Language (KQL)**

---

*Note: This document represents knowledge consolidation, personal realization, and a mindset shift from passive user to active defender — foundational to my growth in cybersecurity operations.*

*🔙 [Back to Microsoft SC-200](../README.md)*
