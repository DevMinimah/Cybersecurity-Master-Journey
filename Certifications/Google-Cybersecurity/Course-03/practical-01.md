# Security Analysis: Analyze Network Attacks

Assessment Context: Scenario-Based Simulation (Google Cybersecurity Professional Certificate)  
Activity: Analyze Network Attacks  
Role Assumed: Security Analyst  
Incident Type: Denial of Service (DoS) / Network Interruption  

---


> *Note: This document is a practical activity for the Google Cybersecurity Professional Certificate. It represents a scenario-based simulation where I assume the role of a Security Analyst conducting a post-incident analysis for a fictional travel agency that advertises sales and promotions on the company’s website.*

---

## Executive Summary
This document outlines the technical analysis of a recent network interruption where multiple customers reported severe connection timeouts when trying to access the company's public-facing website. Based the our network log analysis, the disruption was traced back to a specific IP address suspected to be a malicious actor flooding the web server with a massive volume of TCP SYN requests at an abnormally fast rate. This behavior was identified as a targeted TCP SYN flood Denial of Service (DoS) attack. This report details the identification of the attack vector and explains the mechanical process of how the exploitation of the TCP three-way handshake caused the website to malfunction and deny access to legitimate users.

---

### 1. Identification of the Type of Attack

**Analysis:**  
Based on the  network log analysis, the website's connection timeouts are the direct result of a targeted TCP SYN flood Denial of Service (DoS) attack. The logs show a specific IP address bombarding the web server with a massive volume of TCP SYN (synchronize) requests at an unsustainable rate. In a standard TCP three-way handshake, a server receives a client's SYN request, replies with a SYN-ACK, and waits for the client's final ACK to establish the connection. In this attack, the malicious actor is either spoofing source IP addresses or deliberately ignoring the server's SYN-ACK responses. This traps the connections in a half-open state.

As a result, the server's SYN backlog queue rapidly fills up, completely exhausting its available memory and processing power. Because the connection queue is entirely saturated with these fraudulent, half-open requests, the web server has no resources left to allocate to legitimate users, which directly causes the connection timeout errors our customers are experiencing.

---

### 2. Explanation on How the Attack Causes the Website to Malfunction

**Analysis:**  
The details in the logs confirm that the company's web server is experiencing a targeted SYN flood attack. To understand the malfunction, it is helpful to look at how a normal connection is established versus how the attack disrupts it.

**The Normal TCP 3-Way Handshake:**
*   **Step 1: SYN (The Request):** The client wants to connect to the server, so it sends a SYN (synchronize) message. This is the initiation stage of the communication.
*   **Step 2: SYN-ACK (The Reply):** The server receives the request. If it is ready and able to connect, it sends back a SYN-ACK (synchronize-acknowledge) message, indicating receipt of the request and readiness to communicate.
*   **Step 3: ACK (The Confirmation):** The client receives the server's reply and sends a final ACK (acknowledge) message to confirm. This marks the beginning of a successful, established connection.

**The Attack Mechanism:**  
When a malicious entity sends a massive volume of SYN requests to a web server—exceeding what it can process at one time—it forces the server to slow down as it struggles to handle the growing backlog. The server allocates memory to wait for the final ACK that never comes. 

If the requests persist, the server's resources are completely exhausted. This inadvertently forces the web server to become unresponsive or shut down, thereby denying legitimate users access to the website. The logs indicate a massive influx of SYN packet requests at a high rate, giving the web server little to no time to respond. This is a clear indication of a SYN flood attack targeted at disrupting normal web traffic.

---

*Note: This document was generated from a practical cybersecurity activity to demonstrate the ability to analyze network logs, identify Denial of Service attack vectors, and explain TCP/IP protocol exploitation in a clear, professional manner.*


📄 [View Full Risk Assessment Document (PDF)](./cybersecurity-incident-report.pdf)