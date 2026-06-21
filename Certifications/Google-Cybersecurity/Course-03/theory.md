# Course 03: Connect and Protect: Networks and Network Security

## 📅 Date Started: 2026-06-07
## 📅 Date Completed: 2026-06-09

## 🎯 What I Learned:

- Network Fundamentals & Architecture: 
  - Explored network structures (WANs, LANs) and standard networking tools (hubs, switches, routers, modems).
  - Studied the TCP/IP and OSI models, understanding their layers and respective functions for troubleshooting and communication.
  - Mapped network zones and segmentation: DMZ, internal zones, restricted zones, subnetting, and CIDR for isolating traffic and reducing the attack surface.
  - Analyzed modern network architecture, combining VPN and SD-WAN capabilities for secure, scalable connectivity across distributed locations.
  - Evaluated cloud networks, focusing on their benefits and specific security considerations.

- Network Protocols & Traffic Management: 
  - Categorized network protocols: Communication (TCP, UDP, SMTP), Management (ICMP), and Security (IPSec, SSL/TLS).
  - Understood application protocols: HTTP for web communication, DNS for hostname-to-IP mapping, and ARP for IP-to-MAC address resolution.
  - Studied firewalls (hardware, software, and cloud-based), differentiating between stateless and stateful operations and basic filtering rules.
  - Explored proxy servers (forward, reverse, and email) and how they add security layers to network traffic.

- Wireless & Remote Access Security: 
  - Analyzed wireless security, including IEEE 802.11 (Wi-Fi) standards, common vulnerabilities, and protection mechanisms.
  - Utilized Virtual Private Networks (VPNs) to establish encrypted tunnels for secure remote access and data transmission.

- Network Attacks & Packet Analysis: 
  - Identified network attacks: Interception, backdoor attacks, spoofing, packet sniffing, on-path attacks, DoS, DDoS, SYN flood, ICMP flood, and Ping of Death.
  - Explored IP spoofing variants, including on-path attacks, replay attacks, and Smurf attacks, along with their mitigation strategies.
  - Practiced packet analysis: reading tcpdump logs, understanding active vs. passive packet sniffing, and using protocol analyzers for threat detection.
  - Implemented protection from sniffing by enforcing VPNs, using HTTPS, and avoiding unsecured public WiFi networks.

- System & Network Hardening: 
  - Applied OS hardening techniques: patch management, effective password policies, multi-factor authentication (MFA), and secure hardware disposal practices.
  - Executed network hardening practices: port filtering with firewalls, network segmentation, and end-to-end encryption for data in transit.
  - Developed a comprehensive security hardening strategy: strengthening systems through baseline configurations, log analysis, firewall rule maintenance, and continuous monitoring.

- Network Security Tools: 
  - Deployed and analyzed core network security tools: Firewalls, Intrusion Detection Systems (IDS), Intrusion Detection and Prevention Systems (IDPS), and SIEM platforms for monitoring and response.

- Cloud Security & Cryptography: 
  - Studied cloud security fundamentals: the shared responsibility model, identity and access management (IAM), configuration management, attack surface reduction, and zero-day threat awareness.
  - Applied cryptography in the cloud: encryption at rest and in transit, cryptographic erasure, and crypto-shredding.
  - Managed cryptographic keys using technologies like the Trusted Platform Module (TPM) for local storage and Cloud Hardware Security Modules (CloudHSM) for secure cloud-based operations.

## 💡 Key Takeaways:
- Network security requires layered defense: firewalls, segmentation, encryption, and monitoring work together to protect data in transit.
- The OSI and TCP/IP models provide a universal framework for diagnosing network issues and communicating security findings across teams.
- Not all firewalls are equal: stateful firewalls track connection context, while stateless firewalls filter based on static rules, choosing the right type matters.
- Proxy servers add critical security layers by filtering traffic, masking internal infrastructure, and enforcing access policies.
- Network protocols are the rules of communication: understanding TCP, UDP, DNS, HTTP, and security protocols like TLS is essential for securing data flows.
- Attackers exploit network trust: spoofing, sniffing, and on-path attacks target protocol weaknesses defense requires encryption, authentication, and vigilant monitoring.
- Hardening is continuous: OS patches, strong passwords, MFA, and secure disposal practices reduce the attack surface before an incident occurs.
- Cloud security is shared: providers secure the infrastructure, but organizations must secure their data, identities, configurations, and access controls.
- Cryptography protects data everywhere: encryption, key management (TPM, CloudHSM), and cryptographic erasure (crypto-shredding) ensure data remains confidential even if storage is compromised.
- Security analysts need both breadth and depth: understanding network architecture, protocol behavior, attack patterns, and tooling enables effective detection and response.

## 🔗 Links/Resources:
- [Google Cybersecurity Professional Certificate](https://www.coursera.org/professional-certificates/google-cybersecurity)
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)
- [What is a computer port](https://www.cloudflare.com/learning/network-layer/what-is-a-computer-port/)
- [An introduction to using tcpdump at the Linux command line](https://opensource.com/article/18/10/introduction-tcpdump)

---

🎓 Google Cybersecurity Professional Certificate | Course 3 of 8