# Module 08: Securing Cloud Infrastructure - Practical Activity

## 📅 Date Started: 2026-05-13
## 📅 Date Completed: 2026-05-13

## ⚠️ Disclaimer:
Every scenario is a simulation for practical educational purposes only. All activities are conducted in controlled learning environments to develop cybersecurity skills and knowledge. No real systems, networks, or data were accessed or modified.

## 🧪 Activity Type:
Scenario-based professional simulation: Acting as a cybersecurity professional at Nexusfields to create and secure a Linux virtual machine in Microsoft Azure for development and testing purposes.

## 🎯 Lab Goal:
To implement foundational cloud security controls in Microsoft Azure by creating a resource group, provisioning a secure Linux virtual machine, enabling Microsoft Defender for Cloud, and configuring a firewall to protect cloud infrastructure from unauthorized access and threats.

## 🛠 Tools Used:
- Microsoft Azure Portal (simulated environment)
- Microsoft Defender for Cloud
- Azure Firewall configuration interface
- Linux VM provisioning & security settings

## 📋 What I Did:
1. Task 1: Create a Resource Group – Organized cloud resources into a logical container for management, billing, and access control, establishing a foundation for secure infrastructure deployment.
2. Task 2: Create a Secure Linux Virtual Machine – Provisioned a Linux VM with hardened configuration settings, selecting appropriate regions, VM sizes, and authentication methods (SSH keys) to minimize attack surface.
3. Task 3: Explore Microsoft Defender for Cloud – Enabled and reviewed Defender for Cloud recommendations, security posture dashboard, and threat detection capabilities to monitor and protect Azure resources.
4. Task 4: Create a Firewall – Configured an Azure Firewall to filter inbound and outbound traffic, enforcing network security policies and blocking unauthorized access to the Linux VM.
5. Documented all configuration steps and aligned them with cloud security best practices for startup development environments.

## 🔍 What I Found:
- Resource Groups: Grouping resources simplifies governance, role-based access control (RBAC), and cost tracking. It also enables bulk security policy application and easier compliance auditing.
- Linux VM Security: Using SSH key authentication instead of passwords significantly reduces brute-force risk. Selecting managed disks, enabling encryption, and restricting public IP exposure are critical baseline controls.
- Microsoft Defender for Cloud: Provides unified security management across Azure, on-premises, and multi-cloud environments. It offers actionable recommendations, compliance tracking (CIS, NIST, ISO), and advanced threat protection with minimal configuration overhead.
- Azure Firewall: Acts as a stateful, managed network security service that protects VNet resources. It supports application FQDN filtering, network traffic filtering, and threat intelligence-based filtering to block known malicious IPs/domains.
- Defense-in-Depth in Cloud: Combining VM hardening, Defender for Cloud monitoring, and firewall network controls creates layered security that addresses compute, management, and network attack vectors.

## 💡 What I Learned:
- Cloud security begins with proper resource organization; resource groups enable consistent policy enforcement and simplify security operations at scale.
- Microsoft Defender for Cloud is essential for continuous security posture management, providing real-time alerts, compliance benchmarks, and prioritized remediation guidance.
- Firewalls in cloud environments must be configured with least-privilege principles; allowing only necessary ports/protocols reduces exposure to internet-based threats.
- SSH key-based authentication is a non-negotiable security control for Linux workloads, eliminating password-based vulnerabilities and enabling automated, secure access management.
- Startup and development environments still require enterprise-grade security controls; secure-by-design practices prevent costly breaches and ensure scalability as the organization grows.
- Cloud infrastructure security is a shared responsibility: Azure secures the underlying platform, but customers must configure VMs, networks, identities, and data protection correctly.

## 📸 Screenshot:
🔒 Screenshot Restriction Notice

Screenshots from IBM SkillsBuild simulated lab environments are proprietary content and cannot be shared externally per IBM's academic integrity policy and terms of use.

Lab Completion Verified:
- ✅ Platform: IBM SkillsBuild
- ✅ Module Status: 100% COMPLETE
- ✅ Activities Completed: Resource group creation, Linux VM provisioning, Microsoft Defender for Cloud exploration, Azure Firewall configuration
- ✅ Completion Date: 2026-05-13

Alternative Evidence: Comprehensive written documentation of Creation of a Resource Group, Creating of a Secure Linux Virtual Machine, Explore Microsoft Defender for Cloud and Creation a Firewall provided in sections above.