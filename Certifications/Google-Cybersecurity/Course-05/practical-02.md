# Practical Exercise: PASTA Threat Modeling for a Mobile E-Commerce Application

Assessment Context: Scenario-Based Simulation (Google Cybersecurity Professional Certificate)
Activity: Process for Attack Simulation and Threat Analysis (PASTA) Framework  
Case Study: Sneaker Company Mobile App Pre-Launch Security Assessment    
Role Assumed: Junior Security Analyst / Threat Modeler  
Framework: PASTA (7-Stage Threat Modeling Methodology)  

---

## Project Description
This project involved conducting a comprehensive threat model for a mobile e-commerce application targeting sneaker enthusiasts and collectors. Using the PASTA (Process for Attack Simulation and Threat Analysis) framework, I systematically evaluated the application across all seven stages to identify architectural strengths, potential attack vectors, and security gaps prior to launch. The assessment focused on aligning technical security controls with business objectives, analyzing the application's trust boundaries, and developing actionable remediation strategies to ensure a secure, compliant, and user-friendly deployment.

---

### Stage 1: Define Business and Security Objectives
Before I could protect anything, I had to understand what the business actually cares about. Security without context is just noise.

* Frictionless Experience: Buyers and sellers need seamless communication with multiple checkout options. Security cannot become a barrier to the user experience.
* Data Privacy: The company deeply values how user data is protected. This isn't just a checkbox—it's a trust relationship with every customer who downloads the app.
* Regulatory Compliance: The company needs to maintain good standing with data protection regulations. A single breach doesn't just hurt users—it can shut down the business.

What this taught me: Security objectives must always serve business objectives. If I design controls that slow users down or break functionality, I've failed even if the system is technically "secure."

---

### Stage 2: Define the Technical Scope
I mapped out the technology stack powering the application to understand the attack surface.

* Application Programming Interface (API): Used to allow merchants to showcase sneakers on their own personal storefronts, with customers seamlessly routed to the app for checkout. This is a critical integration point and a high-value target for attackers.
* Public Key Infrastructure (PKI): Implemented for encryption to guarantee that communication and transactions are fully secured between the client and the server.
* SHA-256: Used as the hashing algorithm for data integrity verification.
* SQL Database: Selected for efficient storage and retrieval of customer data and order processing.

What this taught me: Every technology choice introduces both capability and risk. APIs enable growth but expand the attack surface. Databases hold the crown jewels but become the primary target. Understanding the stack is the foundation of every good threat model.

---

### Stage 3: Decompose Application
I worked with the application's data flow diagram to visualize how information moves through the system—from the user's mobile device, through the API layer, into the SQL database, and back out through PKI-encrypted channels. 

This decomposition helped me see the application not as a single monolith, but as interconnected trust boundaries where data is most vulnerable during transit and processing.

---

### Stage 4: Threat Analysis
With the architecture mapped, I shifted into the attacker's mindset and identified realistic threat scenarios:

* Social Engineering of Internal Staff: Employees being tricked into opening files containing malicious code that could hijack network operations. The human element remains the weakest link, even in well-architected systems.
* SQL Injection by External Threat Actors: An attacker exploiting poorly sanitized input fields to manipulate the SQL database, potentially extracting or destroying customer records.

What this taught me: Threats come from both outside and inside. A company can have the strongest firewall in the world, but if an employee clicks the wrong link, it's all bypassed. Threat modeling must account for both technical and human attack vectors.

---

### Stage 5: Vulnerability Analysis
I identified specific weaknesses in the application's current implementation that the threats from Stage 4 could exploit:

* Unsalted SHA-256 Hashing: While SHA-256 is a strong algorithm, using it without a salt makes stored passwords vulnerable to rainbow table attacks. This is a subtle but dangerous oversight.
* Broken API Access Control (IDOR): Insecure Direct Object References could allow an attacker to manipulate API calls and access other users' data simply by changing an ID number in the request.
* SQL Injection (SQLi): If user inputs are not properly parameterized, attackers can inject malicious SQL commands to read, modify, or delete database records.

What this taught me: Vulnerabilities are often hiding in plain sight—inside choices that seem safe on the surface but lack critical implementation details. Security isn't just about choosing the right tools; it's about using them correctly.

---

### Stage 6: Attack Modeling
I analyzed the sample attack tree diagram to map out how a threat actor could realistically chain together the identified vulnerabilities to achieve their objectives, whether that's stealing customer payment data, hijacking user accounts, or disrupting the entire platform.

The attack tree made it clear that these vulnerabilities don't exist in isolation. A successful attacker would combine social engineering to gain internal access, then exploit the unsalted hashes to crack credentials, and finally use those credentials to escalate privileges through the broken API controls.

---

### Stage 7: Risk Analysis and Impact
This is where I translated everything into actionable solutions. Identifying risks without offering remediation is incomplete work.

| Identified Risk | Remediation Strategy |
| :--- | :--- |
| General web and API attacks | Deploy a Web Application Firewall (WAF) and implement API Rate Limiting as a foundational defense layer |
| Unsalted SHA-256 Hashing | Implement salting for all SHA-256 hashes to protect stored credentials against offline attacks |
| SQL Injection | Implement prepared statements across all database queries to eliminate injection vulnerabilities at the code level |
| Broken API Access Control (IDOR) | Implement strict object-level authorization to ensure users can only access their own data |

---

## Summary
This PASTA threat modeling exercise reinforced a truth I carry with me as I build my career in cybersecurity: security is not a product you install it's a process you practice. By walking through all seven stages, I didn't just find vulnerabilities in a simulated app; I practiced the discipline of thinking systematically about risk before it becomes a crisis.

What excites me most about this work is the responsibility that comes with it. Every application that handles real people's data, real transactions, and real trust deserves someone who takes the time to ask, "What could go wrong, and how do I stop it before it does?" That's the mindset I'm developing, and that's the value I'm determined to bring to every security team I join.

---

📄 [View Full Strategy Document (PDF)](./PASTA-worksheet.pdf)

---

*Note: This document outlines my hands-on practice and learning proficiency in threat modeling, risk analysis, and security-by-design methodologies required for cybersecurity operations.*