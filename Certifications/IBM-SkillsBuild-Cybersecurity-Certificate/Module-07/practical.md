# Module 07: Cloud Computing and Virtualization - Practical Activity

## 📅 Date Started: 2026-05-12
## 📅 Date Completed: 2026-05-12

## ⚠️ Disclaimer:
Every scenario is a simulation for practical educational purposes only. All activities are conducted in controlled learning environments to develop cybersecurity skills and knowledge. No real systems, networks, or data were accessed or modified.

## 🧪 Activity Type:
Scenario-based professional simulation: Acting as a help desk technician to create and configure virtual machines for troubleshooting, and evaluating cloud deployment models (Public, Private, Community, Hybrid) to match organizational requirements.

## 🎯 Lab Goal:
To apply cloud computing concepts by selecting appropriate deployment models based on organizational needs, and to gain hands-on virtualization experience by creating, configuring, and managing a Windows 10 virtual machine using Oracle VM VirtualBox for help desk troubleshooting scenarios.

## 🛠 Tools Used:
- Oracle VM VirtualBox (virtualization platform)
- Windows 10 ISO image (guest operating system)
- Cloud deployment model evaluation framework
- Virtual machine configuration interface

## 📋 What I Did:
1. Cloud Deployment Model Selection Activity:
   - Analyzed four distinct business scenarios with varying security, compliance, and operational requirements
   - Evaluated organizational needs including data sensitivity, regulatory constraints, cost considerations, and scalability requirements
   - Matched each business case to the most appropriate cloud deployment model:
     - Public Cloud: For organizations needing cost-effective, scalable resources with minimal infrastructure management
     - Private Cloud: For organizations requiring maximum control, security, and compliance with dedicated infrastructure
     - Community Cloud: For organizations with shared concerns (mission, security, compliance) collaborating on shared infrastructure
     - Hybrid Cloud: For organizations needing to balance sensitive data protection with public cloud scalability

2. Virtual Machine Creation & Configuration (Oracle VM VirtualBox):
   - Received a help desk ticket from Jordan (systems administrator) regarding an employee's Windows 10 computer issue
   - Launched Oracle VM VirtualBox and initiated creation of a new virtual machine
   - Configured VM specifications:
     - Allocated appropriate RAM (memory) based on Windows 10 minimum requirements
     - Created and configured a virtual hard disk (VDI format) with dynamic or fixed allocation
     - Selected Windows 10 ISO as the installation media
     - Configured network adapter settings (NAT/Bridged/Host-only)
     - Set up processor allocation and enablement of virtualization extensions
   - Installed Windows 10 guest operating system within the virtual environment
   - Configured VM settings for optimal performance and security isolation
   - Validated that the VM replicated the employee's environment for safe troubleshooting

## 🔍 What I Found:
- Cloud Deployment Models:
  - Public Cloud (e.g., AWS, Azure, Google Cloud): Best for startups, development/testing, and non-sensitive workloads requiring rapid scaling and pay-as-you-go pricing. Lower upfront costs but less control over infrastructure.
  - Private Cloud (on-premises or hosted): Essential for government agencies, healthcare, and financial institutions with strict compliance (HIPAA, PCI-DSS, GDPR) and data sovereignty requirements. Maximum security and customization at higher cost.
  - Community Cloud: Ideal for collaborative sectors like healthcare networks, research institutions, or government agencies sharing similar regulatory frameworks. Costs and resources are shared among trusted organizations.
  - Hybrid Cloud: Provides the flexibility to keep sensitive data on-premises (private cloud) while leveraging public cloud resources for burst capacity, disaster recovery, and non-critical applications. Requires robust orchestration and security integration.
- Virtualization Benefits for Help Desk:
  - Isolation: VMs provide sandboxed environments where issues can be replicated without risking production systems
  - Snapshots: Ability to capture VM state before testing fixes, enabling instant rollback if changes cause problems
  - Resource Efficiency: Multiple VMs can run on a single physical machine, reducing hardware costs
  - Rapid Deployment: Pre-configured VM templates enable quick environment setup for testing and training
  - Portability: VMs can be easily copied, shared, and migrated between hosts

- VirtualBox Configuration Considerations:
  - Memory Allocation: Must balance guest OS needs with host system resources (typically 2-4GB for Windows 10)
  - Storage Type: Dynamically allocated disks save space; fixed-size disks offer better performance
  - Network Mode: NAT for internet access without host network exposure; Bridged for network visibility; Host-only for isolated testing
  - Virtualization Extensions: Enabling VT-x/AMD-V improves VM performance and enables 64-bit guest OS support

- Security Implications:
  - VMs must be patched and secured like physical machines
  - Hypervisor vulnerabilities could potentially allow VM escape attacks
  - Network segmentation between VMs and host is critical for containment
  - Snapshots may contain sensitive data and require secure storage

## 💡 What I Learned:
- Cloud Deployment Decision-Making: Selecting the right cloud model requires analyzing multiple factors: data classification, compliance requirements, budget constraints, technical expertise, scalability needs, and risk tolerance. There is no one-size-fits-all solution.
- Virtualization as a Security Tool: Virtual machines are essential for cybersecurity professionals—they enable safe malware analysis, vulnerability testing, network simulation, and incident response training without endangering production environments.
- Oracle VM VirtualBox Fundamentals: As a Type 2 (hosted) hypervisor, VirtualBox runs on top of an existing OS and provides enterprise-grade virtualization features at no cost, making it ideal for learning, testing, and small-to-medium deployments.
- Resource Management: Proper VM configuration requires understanding host resource constraints; over-allocation can degrade both host and guest performance, while under-allocation causes poor VM responsiveness.
- Help Desk Efficiency: Creating isolated test environments accelerates troubleshooting by allowing technicians to test patches, configuration changes, and fixes before deploying to end-user systems, reducing downtime and error rates.
- Defense-in-Depth with Virtualization: VMs add a security layer by isolating risky activities (web browsing, software testing, file analysis) from the host system, limiting the blast radius of potential compromises.
- Cloud Security Shared Responsibility: In public cloud models, the provider secures the infrastructure while the customer secures their data and applications; private clouds shift more responsibility to the organization but provide greater control.
- Hybrid Cloud Complexity: While hybrid models offer maximum flexibility, they introduce integration challenges requiring consistent identity management, encryption standards, and security policies across environments.

## 📸 Screenshot:
🔒 Screenshot Restriction Notice

Screenshots from IBM SkillsBuild simulated lab environments are proprietary content and cannot be shared externally per IBM's academic integrity policy and terms of use.

Lab Completion Verified:
- ✅ Platform: IBM SkillsBuild (comprehend.ibm.com)
- ✅ Module Status: 100% COMPLETE
- ✅ Activities Completed:
  - Cloud deployment model selection (Community/Public/Private/Hybrid)
  - Oracle VM VirtualBox VM creation and configuration
  - Windows 10 guest OS installation and setup
- ✅ Completion Date: 2026-05-12

Alternative Evidence: Comprehensive written documentation of cloud deployment model evaluations, VM configuration procedures, and virtualization security considerations provided in sections above.