# Module 02: Network Traffic Capturing and Analysis with Wireshark
  
Practical Activity: Network Traffic Capturing and Analysis with Wireshark
Environment: Kali Linux virtual machine (Ubuntu/Debian-based)  
Role Assumed: Network Security Analyst  
Tools Utilized: Wireshark Packet Analyzer 

---

⚠️ Disclaimer:
This activity is a simulation for practical educational purposes only. All exercises are conducted in controlled, isolated virtual environments to develop cybersecurity skills and knowledge. No real production networks, systems, or sensitive data were accessed or modified.


🧪 Activity Type:
Hands-on technical lab: Practicing Wireshark for packet capture, filter application, protocol analysis, and security-focused network traffic investigation as part of foundational cybersecurity training.


🎯 Lab Goal:
To develop proficiency in using Wireshark for network traffic analysis by capturing packets, applying display filters, identifying security-relevant patterns (port scanning, DNS anomalies, HTTP errors), and interpreting HTTP status codes for incident investigation.

🛠 Tools Used:
- Kali Linux virtual machine
- Wireshark (open-source packet analyzer)
- Terminal/Shell (Bash)
- Sample packet capture files (.pcap/.pcapng)
- Web browser for generating test traffic
- Command-line utilities: wget, chmod

---

➢ Exercise 1: Applying Wireshark Filters

Filters help focus analysis on specific network activity. Let's start with capturing packets.

1. Capture packets using an interface
2. Use a provided Sample File

Option 1: Capture packets using an interface:
- Navigated to a test web application in browser
- Went to login page and started Wireshark capture
- Used test credentials to generate authentication traffic
- Stopped capture after traffic was generated

Option 2: Download a sample packet capture file with mixed traffic:

    wget -q https://s3.amazonaws.com/tcpreplay-pcap-files/smallFlows.pcap -O /home/kali/wireshark/sample.pcapng

Make sure the user has all access to the file:

    chmod 744 /home/kali/wireshark/sample.pcapng

Opened the sample file in Wireshark via File → Open.

---

➢ Exercise 2: User Interface Overview

Explored key Wireshark interface components:
- Menu Bar: Accessed File, Edit, Capture, Analyze, and more.
- Toolbar: Started/stopped captures, saved packets, reloaded captures.
- Packet List Pane: Viewed captured packets in real-time with columns for No., Time, Source, Destination, Protocol, Length, and Info.
- Packet Details Pane: Examined in-depth packet information (IP addresses, protocols, etc.) organized by protocol layers.
- Packet Bytes Pane: Reviewed raw packet data in hexadecimal format for deep inspection.

Practice: Clicked on different packets and observed how the Details and Bytes panes updated to reflect the selected packet's structure.

---

➢ Exercise 3: Display Filters (For Viewing Captured Traffic)

Applied filters in the display filter bar to narrow focus:

● Filter by Protocol (e.g., DNS, HTTP, ARP)

    http

● Filter by IP Address

    ip.addr == 192.168.1.1
    ip.src == 192.168.3.31

● Filter by Port (e.g., HTTP)

    tcp.port == 80

● Filter by MAC Address

    eth.addr == 00:1A:2B:3C:4D:5E

● Filter by TCP SYN (start of a connection):

    tcp.flags.syn == 1

Practice: Typed each filter into the display filter bar and pressed Enter. Observed how the packet list updated to show only matching traffic.

---

➢ Exercise 4: Combining Filters

Made filters more powerful by combining them using logical operators like and and or.

● HTTP traffic that uses port 80

    http and tcp.port == 80

Practice: Built compound filters to isolate specific conversation types. Used the filter expression builder for syntax assistance.

---

➢ Exercise 5: Analyzing Security-Related Traffic

Focused on using Wireshark filters for security analysis. Security analysis is crucial in the world of cybersecurity as it helps spot potentially malicious activities in network traffic.

Identifying Port Scanning Activities:
To detect potential port scanning, looked for a large number of connection attempts from a single source to multiple ports. This filter shows SYN packets without the ACK flag. In a TCP connection, the SYN packet is the first one sent to initiate a connection, and the ACK packet is used to acknowledge the connection. When seeing a lot of SYN packets without ACK from one source to different destination ports, it's a strong indication of port scanning.

Used a specific filter to identify such activities:

    tcp.flags.syn == 1 and tcp.flags.ack == 0

Detecting Suspicious DNS Traffic:
DNS tunneling and other DNS-based attacks use the DNS protocol to hide malicious activities, such as data exfiltration or command and control communication. To detect such attacks, looked for unusual DNS traffic. Once applied this filter, looked for unusually long domain names or a high volume of DNS requests to the same domain.

    dns

Analyzing HTTP Error Responses:
Web application attacks often generate HTTP error responses. Attackers may try to exploit vulnerabilities in web applications, and these attempts can result in error responses from the server. Filtered for these error responses with:

    http.response.code >= 400

This filter shows HTTP response packets with status codes of 400 or higher. All these status codes represent error responses. By examining these packets, can identify attempted web exploits.

---

🔍 What I Found:

### Filter Application Insights
- Display filters instantly narrow packet lists, making targeted analysis efficient
- Combining filters with and/or operators enables precise traffic isolation
- Syntax matters: ip.addr uses ==, while protocol names (http, dns) require no operator

### Security Pattern Recognition
- Port scanning detection via SYN-only packets reveals reconnaissance activity
- DNS filters help identify tunneling attempts through unusual query patterns
- HTTP error code filtering (>=400) surfaces potential web exploitation attempts

### Interface Navigation
- Packet Details pane provides protocol-layer breakdown essential for understanding traffic flow
- Packet Bytes pane enables raw data inspection for advanced forensic analysis
- Colorizing rules can visually highlight suspicious traffic

### Practical Workflow Development
- Starting with broad filters, then narrowing, prevents missing relevant packets
- Saving filtered views as display filter presets accelerates repeat investigations
- Exporting filtered packets supports report generation

---

💡 What I Learned:

### Foundational Wireshark Competencies
- Capture vs. display filters serve different purposes: capture filters reduce data at source; display filters refine analysis post-capture
- Understanding protocol hierarchies (Ethernet → IP → TCP → HTTP) is essential for meaningful packet interpretation
- Filter syntax mastery (==, and, or, contains) dramatically improves investigation speed and accuracy

### Security Analysis Applications
- Wireshark is a detection and investigation tool, not a prevention system; analyst expertise determines value
- Recognizing "normal" traffic patterns in your environment is prerequisite to spotting anomalies
- HTTP status code awareness enables rapid assessment of web application interactions during incident response

### Best Practices Developed
- Always verify filter syntax before applying; malformed filters return no results without error
- Use sample captures for practice before analyzing live or sensitive traffic
- Document filter expressions used during investigations for reproducibility and knowledge sharing

### Transferable Skills for Cybersecurity Roles
- Packet analysis proficiency is required for SOC analysis, penetration testing, network forensics, and threat hunting
- Filter logic translates to SIEM query languages (Splunk SPL, Elastic KQL) and EDR investigation tools
- Protocol understanding supports cloud security, container networking, and infrastructure troubleshooting

### Next Steps for Skill Development
- Practice building complex filters for multi-protocol investigations
- Learn to export and share filtered packet sets for collaborative analysis
- Explore Wireshark plugins and Lua scripting for automated analysis workflows
- Study protocol specifications (RFCs) to deepen interpretation capabilities


---

# HTTP Status Codes to Remember

## Informational (1xx)

### 100 Continue
The server has received the request headers and the client should proceed to send the request body.

### 101 Switching Protocols
The requester has asked the server to switch protocols and the server has agreed to do so.

### 102 Processing
The server has received and is processing the request, but no response is available yet.

---

## Success (2xx)

### 200 OK
The request has succeeded.

---

## Redirection (3xx)

### 301 Moved Permanently
The URL of the requested resource has been changed permanently.

### 302 Found
The URL of the requested resource has been changed temporarily.

### 303 See Other
The response to the request can be found under another URI using a GET method.

### 307 Temporary Redirect
The URL of the requested resource has been changed temporarily.

### 308 Permanent Redirect
The URL of the requested resource has been changed permanently.

---

## Client Error (4xx)

### 400 Bad Request
The server cannot or will not process the request due to an apparent client error.

### 401 Unauthorized
Authentication is required and has failed or has not yet been provided.

### 403 Forbidden
The request was valid, but the server is refusing action.

### 404 Not Found
The requested resource could not be found but may be available in the future.

### 408 Request Timeout
The server timed out waiting for the request.

### 414 URI Too Long
The URI provided was too long for the server to process.

### 415 Unsupported Media Type
The request entity has a media type which the server or resource does not support.

---

## Server Error (5xx)

### 500 Internal Server Error
A generic error message, given when an unexpected condition was encountered.

### 501 Not Implemented
The server either does not recognize the request method, or it lacks the ability to fulfill the request.

### 502 Bad Gateway
The server was acting as a gateway or proxy and received an invalid response from the upstream server.

### 503 Service Unavailable
The server is currently unavailable (because it is overloaded or down for maintenance).

### 504 Gateway Timeout
The server was acting as a gateway or proxy and did not receive a timely response from the upstream server.



---

Key Takeaways:

- What should normal look like? (so abnormal becomes obvious). When sanity-checking a capture, asked:
  ● Does this make sense for what I was doing?
    - I visited a website → I expect DNS + TCP handshake
  ● Is it talking to destinations I recognise?
    - OS update servers, cloud storage, organisation's domains
  ● Is the pattern consistent or noisy?
    - A few connections can be normal
    - Hundreds of repeated attempts may suggest automation, misconfig, or malicious activity

Using Wireshark isn't about trying to memorize every protocol. Need to know what you are looking at and recognizing when something does not belong.

Personal reflection: This lab reinforced that Wireshark proficiency comes from asking the right questions, not memorizing every protocol detail. The ability to filter, correlate, and interpret network traffic is foundational to security operations work.

---

## 📸 Screenshot:
🔒 **Screenshot Restriction Notice**

Screenshots from TS Academy or affiliated simulated lab environments may contain proprietary educational content. Specific packet captures, IP addresses, or system identifiers are not shared publicly to maintain academic integrity and platform terms of use.

Lab Completion Verified:
- ✅ Platform: TS Academy Cybersecurity Program
- ✅ Module Status: 100% COMPLETE
- ✅ Activities Completed: 
  - Wireshark interface navigation and packet capture
  - Display filter application (protocol, IP, port, MAC, TCP flags)
  - Combined filter logic using and/or operators
  - Security-focused traffic analysis (port scanning, DNS anomalies, HTTP errors)
  - HTTP status code interpretation for incident investigation
- ✅ Completion Date: 2026-07-18


---
Alternative Evidence: Comprehensive written documentation of filter syntax, security patterns analyzed, and investigative workflows provided in sections above.
