# Module 02: Network & Threat Fundamentals

## 📅 Date Started: 2026-07-04
## 📅 Date Completed: 2026-07-18

---

## 🎯 What I Learned

### 1. Defense-in-Depth Strategy
- Explored the Defense-in-Depth security model, understanding that no single security measure is sufficient and that multiple overlapping layers are required to protect assets.
- Studied the 7 core layers of defense:
  - **Policies & People:** Security awareness training, acceptable use policies, incident response playbooks.
  - **Physical Security:** Badge access, surveillance, environmental controls for server rooms.
  - **Perimeter Security:** Firewalls, DMZs, email gateways, DDoS mitigation.
  - **Network Security:** Segmentation, VLANs, IDS/IPS, NAC, encrypted tunnels (IPsec, TLS).
  - **Endpoint Security:** EDR agents, host firewalls, disk encryption, patch management.
  - **Application Security:** Secure SDLC, input validation, WAFs, code reviews, dependency scanning.
  - **Data Security:** Encryption at rest/in transit, DLP, tokenization, access controls, backups.
- Analyzed real-world attack scenarios (e.g., a phishing campaign) to understand how these layers work in concert: from email filters blocking the initial payload, to security training preventing clicks, to EDR isolating an infected machine, and finally, backups ensuring recovery without paying a ransom.
- **Practical Application:** In a SOC context, Defense-in-Depth means correlating alerts across layers—a suspicious email (perimeter) + unusual PowerShell execution (endpoint) + outbound C2 traffic (network) = high-confidence incident requiring immediate escalation.

### 2. Network Fundamentals & Simulation (Cisco Packet Tracer)
- Explored network topologies and device roles through hands-on simulation, learning the critical differences between hubs (insecure broadcasting) and switches (targeted MAC-based forwarding).
- Studied the importance of IP addressing and subnet masks, observing how misconfigured subnets immediately break local network communication.
  - **Key Insight:** A /24 subnet (255.255.255.0) allows 254 usable hosts; misunderstanding this leads to segmentation failures and security gaps.
- Learned how DNS servers function to resolve human-readable domain names into machine-readable IP addresses.
  - **Security Relevance:** DNS is a common attack vector (tunneling, poisoning, DGA domains); monitoring DNS queries is critical for threat detection.
- Practiced basic router configuration via the Command Line Interface (CLI), understanding the necessity of default gateways for inter-network routing and using commands like:
  
bash
  enable
  configure terminal
  interface gigabitethernet 0/0
  ip address 192.168.1.1 255.255.255.0
  no shutdown
  exit
  ip Practical Application:168.1.254
 
- **Practical Application:** Understanding subnetting and routing is essential for network forensics, identifying lateral movement, mapping attack paths, and isolating compromised segments during incident response.

### 3. Packet Analysis & Network Monitoring (Wireshark)
- Explored Wireshark as an open-source packet sniffing and network analysis tool, understanding that it is an investigative asset, not an automated Intrusion Detection System (IDS).
- Learned how to navigate the Wireshark interface (Packet List, Details, and Bytes panes) and capture live or sampled network traffic.
- Studied how to apply and combine display filters to isolate specific traffic:
  
  # Protocol-based
  http  dns  tls
  
  # IP/Port-based
  ip.addr == 192.168.1.100 && tcp.port == 443
  # MAC-based
  eth.addr == aa:bb:cc:dd:ee:ff
  
  # Security-focused
  tcp.flags.syn==1 and tcp.flags.ack==0          # SYN scan detection
  dns.qry.name contains "evil"                   # Suspicious DNS query
  http.response.code >= 400                      # HTTP error monitoring
  tcp.payload contains "password"                # Cleartext credential leak
  `
- Learned how to analyze security-related traffic anomalies:
  - Port Scanning: Hundreds of SYN packets without ACKs from a single source.
  - DNS Tunneling: Unusually long or frequent DNS queries to non-standard domains.
  - HTTP Anomalies: Spikes in 401/403 errors followed by 200 OK (potential brute-force success).
  - Data Exfiltration: Large outbound transfers to unknown IPs during off-hours.
- Practical Application: In SOC triage, Wireshark is used to validate SIEM alerts—downloading a PCAP of suspicious traffic to confirm malicious intent before escalating to Level 2.

### 4. HTTP Protocol & Status Codes
- Studied the structure of HTTP responses and memorized the five categories of status codes to better interpret web traffic and identify potential application-layer attacks:
  - 1xx (Informational): e.g., 100 Continue—rarely seen in attacks but useful for protocol analysis.
  - 2xx (Success): e.g., 200 OK—normal traffic; unexpected 200s after auth failures may indicate bypass.
  - 3xx (Redirection): e.g., 301 Moved Permanently, 302 Found—can be abused for phishing or open redirect attacks.
  - 4xx (Client Error): e.g., 400 Bad Request, 401 Unauthorized, 403 Forbidden, 404 Not Found—spikes may indicate scanning, brute-force, or directory traversal attempts.
  - 5xx (Server Error): e.g., 500 Internal Server Error, 502 Bad Gateway, 503 Service Unavailable—may signal application exploitation (e.g., SQLi causing DB crash).
- Practical Application: Correlating HTTP status codes with source IPs and timestamps helps reconstruct attack timelines—e.g., a series of 404s (recon) followed by a 200 (successful exploit) from the same IP is a high-priority alert.

---

## 💡 Key Takeaways

- Redundancy is the Core of Security: Defense-in-Depth proves that security is not about building one impenetrable wall, but about creating a layered ecosystem where the failure of one control is caught by the next.
- You Cannot Secure What You Do Not Understand: Hands-on practice with Packet Tracer reinforced that concepts like subnetting, default gateways, and DNS are not just "IT networking" topics; they are the foundational mechanics that every security analyst must understand to troubleshoot and secure a network.
- Wireshark is About Asking the Right Questions: Effective packet analysis isn't about memorizing every protocol field. It's about establishing a baseline of what "normal" traffic looks like so that anomalies (like hundreds of SYN packets without ACKs) immediately stand out as suspicious.
- Context is Everything in Logs: An HTTP 404 error might just be a broken link, but a sudden spike in 401/403 errors followed by a 200 OK could indicate a successful brute-force or directory traversal attack. Understanding the story the status codes tell is a critical analyst skill.
- Network Fundamentals Enable Threat Hunting: You cannot detect lateral movement, C2 traffic, or data exfiltration if you don't understand how packets move, how routing works, and what "normal" looks like for your environment.

---

## 🔗 Links/Resources

- [Cisco Networking Academy (Packet Tracer)](https://www.netacad.com/courses/packet-tracer)
- [Wireshark Official Documentation & User Guide](https://www.wireshark.org/docs/)
- [Wireshark Display Filter Reference](https://www.wireshark.org/docs/dfref/)
- [MDN Web Docs: HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
- [CISA: Defense in Depth Overview](https://www.cisa.gov/news-events/news/defense-depth)
- [NIST SP 800-41: Guidelines on Firewalls and Firewall Policy](https://csrc.nist.gov/publications/detail/sp/800-41/rev-1/final)
- [SANS Reading Room: Practical Packet Analysis](https://www.sans.org/reading-room/)


---
*Note: This document represents knowledge consolidation, personal realization, and a mindset shift from passive user to active defender, foundational to my growth in cybersecurity operations.*

*🔙 [Back to TS Academy Cybersecurity](../README.md)*
`