# MECR1043 – Cloud Computing Security 

**Semester:** 1 | **Year:** 2025/2026 | **Instructor:** Dr. Mohd Zamri Osman

---

## 🔍 Executive Summary

This repository showcases my hands-on experience in **Cloud Security** using **Microsoft Azure**. It covers the three pillars of cloud security governance—**Identity & Access Management (IAM)**, **Role-Based Access Control (RBAC)**, and **audit logging**—alongside practical **infrastructure provisioning** on Azure Virtual Machines. Through structured lab exercises, I developed the ability to control who accesses cloud resources, enforce least privilege, monitor administrative changes, and securely deploy Linux-based services in the cloud.

---

## 🎯 Core Learning Objectives

- Understand the **Azure Shared Responsibility Model** and the security boundaries between cloud provider and customer.
- Apply **Role-Based Access Control (RBAC)** to manage user permissions at subscription, resource group, and resource scopes.
- Assign and revoke **built-in and custom roles** (Owner, Contributor, Reader, Virtual Machine Contributor) using the Azure portal.
- Enforce the **principle of least privilege** by scoping role assignments appropriately.
- Monitor and audit administrative changes using the **Azure Activity Log**.
- Provision and secure **Azure Virtual Machines** using SSH key-based authentication and Network Security Group (NSG) rules.
- Deploy and validate application-level services (NGINX) on cloud-hosted Linux servers.

---

## 🛠️ Tools & Technologies

| Category | Tools |
| :--- | :--- |
| **Cloud Platform** | Microsoft Azure (Azure for Students subscription) |
| **Identity & Access Management** | Azure RBAC, Azure Active Directory (Entra ID), Access Control (IAM) |
| **Access Control** | Role Assignments, Scope Management (Subscription / Resource Group / Resource) |
| **Audit & Monitoring** | Azure Activity Log, CSV Export, Operation Filters |
| **Virtual Machines** | Azure VM (Ubuntu Server 22.04 LTS – Gen2), Standard D2s v3 (2 vCPUs, 8 GB RAM) |
| **Authentication** | SSH Public Key (RSA), `myKey.pem` private key |
| **Networking** | Network Security Group (NSG) inbound rules (SSH 22, HTTP 80) |
| **Linux Administration** | `uname -a`, `sudo apt-get update`, `sudo apt-get install nginx` |
| **Web Server** | NGINX (verified via public IP) |
| **Governance** | Least Privilege, Segregation of Duties, Role Definition Management |

---

## 📚 Key Skills Developed

### 🔐 Identity & Access Management (IAM)
- Navigated **Azure Access Control (IAM)** to view and manage role assignments.
- Identified **current user permissions** and assigned roles (e.g., Owner, Contributor).
- Distinguished between **direct role assignments** ("This resource") and **inherited assignments** ("Inherited from parent scope").
- Applied **scope-based access control** across subscription, resource group, and resource levels.

### 🛡️ Role-Based Access Control (RBAC)
- Explored Azure's **70+ built-in roles** (Owner, Contributor, Reader, Virtual Machine Contributor, etc.).
- Assigned the **Virtual Machine Contributor** role to a user at the resource group scope.
- Understood how RBAC enforces **least privilege** by restricting users to only the actions they need.
- Removed role assignments to **revoke access** when no longer required.

### 📋 Audit & Compliance
- Used **Azure Activity Log** to monitor administrative operations.
- Filtered audit logs by **Timespan** (Last month) and **Operation Type** (role assignments, role definitions).
- Identified key RBAC operations: Create/Delete role assignment, Create/Delete custom role definition.
- Examined **detailed log entries** (Summary, JSON, Change history) to trace who did what and when.
- Exported audit logs as **CSV files** for compliance reporting and external analysis.

### ☁️ Cloud Infrastructure Provisioning
- Provisioned an **Ubuntu Server 22.04 LTS (Gen2)** VM in Azure with custom parameters:
  - Resource group: `myResourceGroup`
  - VM name: `myVM`
  - Region: East Asia
  - Size: Standard D2s v3 (2 vCPUs, 8 GB RAM)
- Understood the importance of **Availability Zones** and **Infrastructure Redundancy** for production workloads.

### 🔑 SSH Key-Based Authentication
- Generated a new **SSH key pair** (`myKey`) during VM creation.
- Safely downloaded and stored the private key file (`myKey.pem`).
- Connected remotely using:
  ```bash
  ssh -i "myKey.pem" azureuser@20.24.209.243
