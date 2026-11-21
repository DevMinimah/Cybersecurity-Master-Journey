# TS Academy Cybersecurity: Module 06 - Cloud Security & Identity Management

## 📅 Date Started: 2026-10-31
## 📅 Date Completed: 2026-10-31

---

## 🎯 What I Learned

### 1. Cloud Computing Fundamentals
- Explored the foundational concept of cloud computing as the practice of renting computing resources (storage, processing, networking) over the internet, rather than purchasing and maintaining physical hardware.
- Studied the physical reality of the cloud: powerful, 24/7 servers housed in highly secure, climate-controlled data centers owned by major providers like AWS, Microsoft Azure, and Google Cloud Platform (GCP).
- Understood how cloud computing solves traditional IT challenges, specifically by eliminating high upfront capital expenditures and providing elastic scalability to handle unpredictable demand.

### 2. Cloud Service Models
- Studied the three primary cloud service models and the trade-offs between control and management overhead:
  - *IaaS (Infrastructure as a Service):* Renting virtualized hardware (e.g., AWS EC2, Azure VMs). Offers full control but requires the user to manage the OS, applications, and security.
  - *PaaS (Platform as a Service):* Providing a managed environment for developers to build and deploy applications (e.g., Heroku, Google App Engine) without managing the underlying infrastructure.
  - *SaaS (Software as a Service):* Delivering finished, ready-to-use software applications over the internet (e.g., Gmail, Slack, Dropbox), requiring minimal management from the user.

### 3. Cloud Deployment Models
- Learned the different ways cloud infrastructure can be deployed based on organizational needs:
  - *Public Cloud:* Shared infrastructure owned by a third-party provider, open to anyone who rents it.
  - *Private Cloud:* Dedicated cloud infrastructure used exclusively by a single organization (on-premises or hosted).
  - *Hybrid Cloud:* A mix of public and private clouds, allowing data and applications to be shared between them.
  - *Multi-Cloud:* The strategic use of multiple public cloud providers simultaneously to avoid vendor lock-in and increase resilience.

### 4. Cloud Engineering vs. Cloud Security
- Explored the distinction between Cloud Engineering (designing, building, and maintaining cloud systems for reliability, speed, and cost-efficiency) and Cloud Security (protecting those systems, data, and identities from threats).
- Understood that modern cloud security must be integrated into the engineering and design phases (DevSecOps) to prevent misconfigurations, which are the leading cause of cloud breaches.

### 5. Cloud Security Frameworks & Best Practices
- Studied foundational cloud security concepts, emphasizing the critical Shared Responsibility Model: the cloud provider secures the *cloud* (hardware, hypervisor, physical data centers), while the customer is always responsible for securing what is *in* the cloud (data, Identity and Access Management (IAM), configurations, and applications).
- Reviewed industry-standard resources and frameworks for cloud security, including the Cloud Security Alliance (CSA) and OWASP Cloud Security guidelines.

### 6. Industry Certifications & Continuous Learning
- Identified key entry-level and foundational certifications to validate cloud and security knowledge, including AWS Certified Cloud Practitioner, Microsoft Azure Fundamentals (AZ-900), Google Cloud Digital Leader, CompTIA Security+, and CompTIA Cloud+.
- Explored hands-on practice platforms and free tiers (AWS Free Tier, Azure Free Account, Google Cloud Free Tier, TryHackMe) to safely build and secure cloud environments.

---

## 💡 Key Takeaways

- The Cloud is Not Magic: It is simply someone else's computer. Understanding the underlying infrastructure (servers, data centers, networking) is absolutely crucial for securing it effectively.
- The Shared Responsibility Model is Non-Negotiable: A common and dangerous misconception is that moving to the cloud outsources all security. In reality, misconfigurations (like public S3 buckets or overly permissive IAM roles) remain the customer's responsibility and are the primary attack vector.
- Security Responsibilities Shift with Service Models: As you move from IaaS to PaaS to SaaS, you gain convenience but lose granular control. Your security focus must shift accordingly (e.g., from patching OS kernels in IaaS to managing data access and SaaS application configurations in SaaS).
- Identity is the New Perimeter: In cloud environments, traditional network perimeters are porous or non-existent. Robust Identity and Access Management (IAM), enforcing the Principle of Least Privilege and Multi-Factor Authentication (MFA), is the most critical security control.

---

## 🔗 Links/Resources

Cloud Computing Fundamentals:
- [AWS Cloud Practitioner Essentials (Free Course)](https://aws.amazon.com/training/digital/aws-cloud-practitioner-essentials/)
- [Google Cloud Fundamentals (Free on Coursera)](https://www.coursera.org/learn/gcp-fundamentals)
- [Microsoft Azure Fundamentals Learning Path (AZ-900)](https://learn.microsoft.com/en-us/training/paths/az-900-describe-cloud-concepts/)
- [IBM: What Is Cloud Computing?](https://www.ibm.com/topics/cloud-computing)

Cloud Security Frameworks & Guidelines:
- [Cloud Security Alliance (CSA) Research](https://cloudsecurityalliance.org/research/)
- [OWASP Cloud Security Project](https://owasp.org/www-project-cloud-security/)
- [Google Cloud Security Overview](https://cloud.google.com/docs/security/overview)
- [AWS Security Fundamentals (Free Course)](https://aws.amazon.com/training/digital/aws-security-fundamentals/)

Cloud Engineering & Architecture:
- [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/)
- [Terraform Tutorials (HashiCorp)](https://developer.hashicorp.com/terraform/tutorials)
- [Docker Getting Started](https://docs.docker.com/get-started/)
- [Kubernetes Basics](https://kubernetes.io/docs/tutorials/kubernetes-basics/)

Practice Platforms & Free Tiers:
- [AWS Free Tier](https://aws.amazon.com/free/)
- [Microsoft Azure Free Account](https://azure.microsoft.com/en-us/free/)
- [Google Cloud Free Tier](https://cloud.google.com/free)
- [TryHackMe: Cloud Security Rooms](https://tryhackme.com)

---

🎓 TS Academy Cybersecurity Program | Module 06: Cloud Security & Identity Management

---

*Note: This document represents knowledge consolidation, personal realization, and a mindset shift from passive user to active defender — foundational to my growth in cybersecurity operations.*

*🔙 [Back to TS Academy Cybersecurity](../README.md)*