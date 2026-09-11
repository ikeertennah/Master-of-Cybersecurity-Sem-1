# MECR1043 – Cloud Computing Security

**Semester:** 1 | **Year:** 2025/2026 | **Instructor:** Dr. Mohd Zamri Osman

---

## 🔍 Executive Summary

This repository showcases my comprehensive hands‑on experience in **Cloud Security** using **Microsoft Azure** and **Amazon Web Services (AWS)**. It covers the full spectrum of cloud security—from **Identity & Access Management (IAM)** and **Role-Based Access Control (RBAC)** to **infrastructure provisioning**, **data lifecycle security**, and **advanced threat mitigation in multi‑cloud environments**. Through structured labs, a video presentation, and a research‑based final project, I developed the practical and strategic skills required for roles in **Cloud Security Engineering, Cloud Governance, and Security Architecture**.

---

## 🎯 Core Learning Objectives

- Understand the **Azure** and **AWS Shared Responsibility Models**.
- Apply **Role-Based Access Control (RBAC)** to manage user permissions at subscription, resource group, and resource scopes.
- Assign and revoke **built-in and custom roles** (Owner, Contributor, Reader, Virtual Machine Contributor) using the Azure portal.
- Enforce the **principle of least privilege** by scoping role assignments appropriately.
- Monitor and audit administrative changes using the **Azure Activity Log**.
- Provision and secure **Azure Virtual Machines** using SSH key-based authentication and Network Security Group (NSG) rules.
- Analyse the **Cloud Data Lifecycle** (Create, Store, Use, Share, Archive, Destroy) and map security controls to each phase.
- Evaluate **advanced threat mitigation strategies** in multi-cloud environments, including Zero Trust, IAM, Continuous Authentication, and AI-driven detection.

---

## 🛠️ Tools & Technologies

| Category | Tools |
| :--- | :--- |
| **Cloud Platforms** | Microsoft Azure (Azure for Students), Amazon Web Services (AWS) |
| **Identity & Access Management** | Azure RBAC, Azure Active Directory (Entra ID), AWS IAM, AWS KMS, AWS STS |
| **Access Control** | Role Assignments, Scope Management (Subscription / Resource Group / Resource) |
| **Audit & Monitoring** | Azure Activity Log, AWS CloudTrail, CSV Export, Operation Filters |
| **Virtual Machines** | Azure VM (Ubuntu Server 22.04 LTS – Gen2), Standard D2s v3 (2 vCPUs, 8 GB RAM) |
| **Authentication** | SSH Public Key (RSA), myKey.pem private key |
| **Networking** | Network Security Group (NSG) inbound rules (SSH 22, HTTP 80) |
| **Linux Administration** | uname -a, sudo apt-get update, sudo apt-get install nginx |
| **Web Server** | NGINX (verified via public IP) |
| **AWS Security Services** | Amazon Macie, AWS KMS, Amazon S3 (Bucket Policies, Object Lock, Pre-signed URLs), S3 Glacier Vault Lock |
| **Governance Frameworks** | Zero Trust Architecture (NIST SP 800-207), Shared Responsibility Model, Least Privilege, Segregation of Duties |

---

## 📚 Key Skills Developed

### 🔐 Identity & Access Management (IAM)
- Navigated **Azure Access Control (IAM)** and **AWS IAM** to view and manage role assignments.
- Identified **current user permissions** and assigned roles (Owner, Contributor, Virtual Machine Contributor).
- Distinguished between **direct role assignments** and **inherited assignments**.
- Applied **scope-based access control** across subscription, resource group, and resource levels.
- Understood **AWS IAM policies**, **AWS KMS**, and **AWS STS temporary credentials**.

### 🛡️ Role-Based Access Control (RBAC)
- Explored Azure's **70+ built-in roles** (Owner, Contributor, Reader, Virtual Machine Contributor).
- Assigned the **Virtual Machine Contributor** role at the resource group scope.
- Enforced **least privilege** by restricting users to only the actions they need.
- Removed role assignments to **revoke access** when no longer required.

### 📋 Audit & Compliance
- Used **Azure Activity Log** to monitor administrative operations.
- Filtered audit logs by **Timespan** and **Operation Type** (role assignments, role definitions).
- Examined **detailed log entries** (Summary, JSON, Change history).
- Exported audit logs as **CSV files** for compliance reporting.
- Understood **AWS CloudTrail** for auditing AWS API activity.

### ☁️ Cloud Infrastructure Provisioning
- Provisioned an **Ubuntu Server 22.04 LTS (Gen2)** VM in Azure:
  - Resource group: myResourceGroup
  - VM name: myVM
  - Region: East Asia
  - Size: Standard D2s v3 (2 vCPUs, 8 GB RAM)
- Understood **Availability Zones** and **Infrastructure Redundancy**.

### 🔑 SSH Key-Based Authentication
- Generated a new **SSH key pair** (myKey).
- Safely downloaded and stored the private key file (myKey.pem).
- Connected remotely using SSH with the private key.
- Verified the **SSH fingerprint** to confirm host authenticity.
- Understood why **key-based auth is stronger than password-based auth**.

### 🛡️ Network Security Configuration
- Configured **Inbound Port Rules** in Azure NSG:
  - **SSH (port 22)** – Secure remote administration.
  - **HTTP (port 80)** – Public web access to NGINX.
- Learned how Azure NSGs act as a **stateful firewall**.

### 🐧 Linux System Administration
- Executed Linux commands:
  - uname -a – Verified kernel and architecture.
  - sudo apt-get update – Updated package lists.
  - sudo apt-get install nginx – Installed NGINX.
- Interpreted system info (system load, memory usage, swap, IP address).

### 🌐 Application Deployment & Validation
- Installed **NGINX** as a web server.
- Verified deployment via the VM's **public IP address**.
- Confirmed the default NGINX welcome page.

### 📊 Cloud Data Lifecycle Security (AWS)
- Analysed the **six phases**:
  - **Create** – Data classification, client-side encryption, API validation (Amazon Macie).
  - **Store** – Server-side encryption, S3 Bucket Policies, S3 Object Lock (WORM).
  - **Use** – Data masking, TLS, AWS Nitro Enclaves, Lambda least privilege.
  - **Share** – End-to-end encryption, S3 Pre-signed URLs, cross-account IAM, AWS RAM.
  - **Archive** – S3 Glacier Vault Lock (WORM enforcement), logical air-gapping.
  - **Destroy** – Cryptographic shredding via AWS KMS key deletion.
- Conducted **interdependency analysis**.
- Applied the **Shared Responsibility Model**.
- Analysed the **Capital One (2019) breach** as a real-world case study.

### 🧠 Advanced Threat Mitigation in Multi-Cloud (Research Project)
- Researched **identity-based attacks** (credential abuse, privilege sprawl, non-human identities).
- Analysed **policy inconsistency** (fragmentation, configuration drift).
- Evaluated **visibility gaps** across AWS, Azure, Google Cloud.
- Assessed **Zero Trust Architecture**, **IAM**, **Continuous Authentication**, **AI/ML detection**, and **SOAR**.
- Identified **strengths** (granularity, predictive AI, velocity).
- Identified **limitations** (black-box AI, integration complexity, performance trade-offs).
- Explored **future trends**: Cybersecurity Mesh Architecture (CSMA), self-healing systems, Federated Learning, and Quantum-Resistant Cryptography.

---

## 📂 Course Breakdown

| Component | Focus Area | Key Outcomes |
| :--- | :--- | :--- |
| **Lab 1.1** | List Access using Azure RBAC | Explored "My Permissions"; reviewed Role Assignments; distinguished direct vs. inherited scopes; listed built-in/custom roles. |
| **Lab 1.2** | Assign Roles using Azure RBAC | Assigned **Virtual Machine Contributor** at resource group scope; verified assignment; removed role to revoke access. |
| **Lab 1.3** | Monitor Access using Activity Log | Filtered by Timespan and Operation; reviewed detailed log entries; exported CSV for audit reporting. |
| **Lab 2** | Deploy Azure VM with SSH & NGINX | Provisioned Ubuntu 22.04 LTS VM; configured SSH key auth; configured NSG rules; installed NGINX; validated via public IP. |
| **Assignment 1** | AWS Cloud Data Lifecycle Security | Mapped AWS controls to all 6 lifecycle phases; analysed interdependencies; analysed Capital One breach. |
| **Final Project** | Multi-Cloud Threat Mitigation (Group) | Researched identity attacks, policy gaps, visibility issues; evaluated Zero Trust, AI, SOAR; identified future trends. |

---

## 🏆 Spotlight #1: AWS Cloud Data Lifecycle Security

**Format:** Video Presentation | **Platform:** AWS | **Case Study:** Capital One (2019)

| Phase | Key AWS Security Controls |
| :--- | :--- |
| **Create** | Amazon Macie, client-side encryption, IAM write policies |
| **Store** | S3 Bucket Policies, default encryption, S3 Object Lock (WORM) |
| **Use** | Data masking, TLS, AWS Nitro Enclaves, Lambda least privilege |
| **Share** | S3 Pre-signed URLs, cross-account IAM roles, AWS RAM |
| **Archive** | S3 Glacier Vault Lock (immutable retention policies) |
| **Destroy** | AWS KMS cryptographic shredding |

**Key Insight:** The **Capital One breach** demonstrated how an over-privileged IAM role in the "Use" phase led to the compromise of the "Store" phase—resulting in **$80M in fines and a $190M settlement**.

---

## 🏆 Spotlight #2: Multi-Cloud Threat Mitigation (Final Project)

**Format:** Group Research Project | **Team Size:** 3 | **Video:** [YouTube Link](https://youtu.be/Fd1Md9EvHFQ)

**Core Findings:**

- **Identity is the new perimeter.** Federated trust can become a single point of failure.
- **Policy inconsistency is a governance failure.** Fragmented models create exploitable gaps.
- **AI-driven detection is powerful but opaque.** 96%+ detection against APTs, but "black box" explainability causes alert fatigue.
- **Automation (SOAR) is essential for speed.** Reduces dwell time from days to seconds.
- **The future is architectural unity.** CSMA, self-healing systems, and quantum-resistant cryptography will define the next generation.

---

## 🎓 Why This Matters

This portfolio demonstrates I can:

- **Design and enforce least-privilege access** using Azure RBAC and AWS IAM.
- **Assign and revoke roles** at the appropriate scope.
- **Audit administrative activity** for compliance and incident response.
- **Provision and secure cloud VMs** using SSH keys and NSG rules.
- **Map security controls** to every phase of the cloud data lifecycle.
- **Evaluate advanced mitigation strategies** in multi-cloud environments.
- **Communicate findings** through professional presentations and reports.

These skills transfer directly to roles in **Cloud Security Engineering, IAM Administration, Security Architecture, Security Operations, DevOps, and Cloud Governance**.

---


---

## 🔍 Reflection

This course transformed my understanding of cloud security from isolated tools into a **holistic, interconnected system**.

**Governance (Labs 1.1–1.3):** Understanding **scope inheritance** was key. Assigning the **Virtual Machine Contributor** role at the **resource group scope** rather than subscription scope practiced **least privilege** in a real environment. **Activity Log** showed that in the cloud, audit logging is your only safety net.

**Infrastructure (Lab 2):** Using **SSH keys instead of passwords** and verifying host fingerprints reflected production-grade secure access. Configuring NSG rules to open only ports 22 and 80 demonstrated **least exposure**.

**Data Lifecycle (Assignment 1):** Analysing the **AWS Cloud Data Lifecycle** showed security is continuous. The **Capital One breach** proved a single over-privileged IAM role can render encryption useless—reinforcing **system thinking**.

**Multi-Cloud (Final Project):** Researching advanced mitigation revealed that the future is **architectural unity, not point solutions**. Zero Trust, AI, and SOAR must integrate into a **Cybersecurity Mesh Architecture** to be effective.

I plan to build on this by exploring **Azure Policy, Conditional Access, PIM, Microsoft Defender for Cloud, and Terraform for IaC security**.



