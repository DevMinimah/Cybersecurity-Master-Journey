# Module 05: Firmware & Endpoint Security - Practical Activity

## 📅 Date Started: 2026-05-08
## 📅 Date Completed: 2026-08

## 🧪 Activity Type:
Scenario-based professional simulation: Acting as a help desk technician to develop a 4-step firmware security plan and configure endpoint firewall controls for remote workers.

## 🎯 Lab Goal:
To establish a structured lifecycle plan for securing device firmware against tampering and exploits, and to verify/configure Windows Defender Firewall on a remote employee’s laptop to ensure continuous endpoint protection, threat detection, and log monitoring.

## 🛠 Tools Used:
- Adobe file editor
- Windows Defender Firewall console
- Firmware management/verification tools (simulated)
- Remote desktop/access interface (simulated)
- Log review & monitoring dashboard

## 📋 What I Did:
1. Developed a 4-step firmware security plan covering: (1) Inventory & baseline mapping, (2) Vendor-signed update/patch management, (3) Cryptographic integrity verification, and (4) Access control & secure storage.
2. Remotely accessed a remote employee’s (Luke’s) Windows laptop to verify Windows Defender Firewall status, ensure correct network profile assignment (Domain/Private/Public), and confirm it was actively blocking unauthorized inbound connections.
3. Enabled and reviewed firewall logging to capture dropped packets and connection anomalies, establishing a baseline for ongoing remote endpoint monitoring.
4. Documented configuration steps and compliance checkpoints to ensure firmware and firewall controls align with organizational remote-work security policies.

## 🔍 What I Found:
- Firmware Security Lifecycle: Firmware is a foundational attack surface; without structured management, outdated or unsigned firmware can enable persistent malware, supply chain compromises, or hardware-level exploits. The 4-step plan ensures continuous visibility, timely patching, validation, and restricted access.
- Windows Defender Firewall Configuration: Remote laptops often default to permissive or misaligned firewall profiles. Properly configuring profiles, enabling stateful inspection, and logging blocked connections creates a critical network-level defense layer for off-premises devices.
- Log Monitoring Value: Firewall logs provide early indicators of reconnaissance, brute-force attempts, or misconfigured applications. Enabling log rotation and alert thresholds prevents log bloat while maintaining audit readiness.
- Help Desk Security Role: Endpoint hardening is not solely an IT admin task; help desk technicians are the first line of verification for remote device compliance, ensuring baseline security controls are active before granting network access.

## 💡 What I Learned:
- Firmware security requires a proactive, lifecycle-driven approach; inventorying, patching, verifying signatures, and restricting flash/admin access prevent low-level compromises that bypass OS defenses.
- Endpoint firewalls are essential for remote workers; correct profile configuration and active logging transform a basic OS feature into a verifiable security control.
- Defense-in-depth starts at the hardware/firmware layer; securing the lowest tier ensures that higher-level controls (OS, applications, network) remain effective.
- Help desk operations directly impact security posture; validating configurations, reviewing logs, and enforcing baselines reduce organizational risk and support compliance audits.

##  Screenshot: