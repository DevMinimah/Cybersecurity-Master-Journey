# Portfolio Project: SQL Filtering for Security Investigations

**Assessment Context:** Scenario-Based Simulation (Google Cybersecurity Professional Certificate)  
**Activity:** SQL Filtering for Security Investigations  
**Environment:** MariaDB Database (organization database)  
**Role Assumed:** Security Analyst  
**Tools Utilized:** SELECT, FROM, WHERE, AND, OR, NOT, LIKE  

---

## Project Description
As a security professional at a large organization, my role involves investigating security issues to maintain system integrity. In this project, I examined the organization’s data within the `employees` and `log_in_attempts` tables to investigate potential security anomalies involving login attempts and employee machines. By applying advanced SQL filters, I successfully retrieved targeted records to isolate suspicious activity and identify specific employee groups requiring system updates.

*Note: All query outputs in screenshots were truncated using LIMIT 5 for brevity. In production environments, queries return full result sets.*

---

## Retrieve after hours failed login attempts

To investigate potential unauthorized access, I needed to identify failed login attempts that occurred outside of standard business hours (after 18:00). I used the `AND` operator to filter for both the time condition and the failure status simultaneously.

**Command used:**
```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = FALSE;
```

**Output/Result:**
The query successfully returned only the failed login attempts that occurred after 6 PM. This precise filter is critical for identifying suspicious after-hours activity that warrants further security investigation.

![Failed logins after hours](sql-logic-failed-afterhours.png)

---

## Retrieve login attempts on specific dates

The security team needed to review all login activity surrounding a specific suspicious event that occurred over a two-day period. I used the `OR` operator to combine the results from two distinct dates into a single dataset.

**Command used:**
```sql
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
```

**Output/Result:**
The query returned all login attempts from both May 8th and May 9th, providing the complete timeline of user activity needed to investigate the suspicious event without having to run separate queries.

![Logins on specific dates](sql-logic-specific-dates.png)

---

## Retrieve login attempts outside of Mexico

To investigate potential unauthorized access from unexpected geographic regions, I needed to filter out all legitimate login attempts originating from Mexico. I used the `NOT` and `LIKE` operators to exclude all countries starting with 'MEX'.

**Command used:**
```sql
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';
```

**Output/Result:**
The query successfully excluded entries like 'MEX' and 'MEXICO', returning only logins from other regions (like CAN and USA). This demonstrates how to quickly filter out known-safe data to focus on geographic anomalies.

![Logins outside Mexico](sql-logic-not-mexico.png)

---

## Retrieve employees in Marketing

The IT team needed to update machines for employees in the Marketing department, but only for those located in the East building. I combined an exact match filter with a wildcard pattern filter using the `AND` operator to pinpoint the exact records.

**Command used:**
```sql
SELECT *
FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';
```

**Output/Result:**
The query returned exactly the Marketing employees located in East building offices (e.g., East-170, East-195). This precision prevents unnecessary updates to employees in other buildings and ensures the right assets are targeted.

![Marketing employees in East building](sql-logic-marketing-east.png)

---

## Retrieve employees in Finance or Sales

A separate update was required for all employees in either the Finance or Sales departments. I used the `OR` operator to include records from two different departments in a single query.

**Command used:**
```sql
SELECT *
FROM employees
WHERE department = 'Finance' OR department = 'Sales';
```

**Output/Result:**
The query successfully returned a combined list of all Finance and Sales employees, streamlining the process of gathering the required device information for the cross-departmental update.

![Finance and Sales employees](sql-logic-finance-sales.png)

---

## Retrieve all employees not in IT

The final update had already been completed for the Information Technology department. I needed to generate a list of all employees *except* those in IT to avoid redundant work. I used the `NOT` operator to exclude this specific department.

**Command used:**
```sql
SELECT *
FROM employees
WHERE NOT department = 'Information Technology';
```

**Output/Result:**
The query returned all employees across the organization while successfully filtering out the IT staff, ensuring the update team only targets the remaining departments that still require the security patch.

![Employees not in IT](sql-logic-not-it.png)

---

## Summary
Through this project, I demonstrated my ability to use SQL filtering operators to investigate security issues and manage employee machine updates. By applying `AND`, `OR`, and `NOT` operators to the `employees` and `log_in_attempts` tables, I isolated after-hours failed logins, tracked specific date-based activity, excluded geographic regions, and targeted specific departments for system maintenance. These SQL filtering skills are essential for efficiently extracting actionable data from large organizational databases to maintain system security and operational efficiency.

---

📄 [View Full Strategy Document (PDF)](./apply-filters-to-sql-queries.pdf)

---

*Note: This document outlines my hands-on practice and learning proficiency in advanced SQL Boolean logic, multi condition filtering, and targeted data extraction required for cybersecurity operations.*