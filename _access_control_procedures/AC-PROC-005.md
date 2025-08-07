---
title: Privileged Account Management Procedures (AC-PROC-005)
parent: Access Control Procedures
nav_order: 5
---

### 1. Purpose

This procedure establishes comprehensive management controls for privileged accounts with elevated access to systems containing electronic Protected Health Information (ePHI) and critical business systems. This procedure ensures privileged accounts are properly provisioned, monitored, and controlled to minimize security risks while maintaining operational capabilities for authorized administrative functions.

### 2. Scope

This procedure applies to all privileged accounts within **[Company Name]** systems and infrastructure, including:
- Administrative accounts for servers, databases, and network devices
- Application administrator accounts and service accounts
- Cloud platform administrative accounts (AWS, Azure, GCP)
- Emergency access accounts and break-glass procedures
- Vendor and contractor privileged access accounts
- System service accounts and automated process accounts

### 3. Overview

Privileged account management requires strict controls for account creation, access approval, monitoring, and periodic review. This includes multi-factor authentication, privileged access management (PAM) solutions, session recording, and comprehensive audit logging. All privileged account activities must be monitored and reviewed to detect unauthorized usage and ensure compliance with security policies.

### 4. Procedure

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | **Account Requestor** | Submit privileged account request through **[Access Management System]** with business justification, required access level, and duration |
| **2** | **Hiring Manager** | Review and approve privileged account request confirming business need and appropriate access level for role responsibilities |
| **3** | **Information Security Officer** | Conduct risk assessment for privileged account request evaluating access scope, duration, and potential security impact |
| **4** | **System Administrator** | Create privileged account with minimum necessary permissions and configure multi-factor authentication requirements |
| **5** | **System Administrator** | Enroll privileged account in Privileged Access Management (PAM) system with session recording and access approval workflows |
| **6** | **Account Owner** | Complete privileged account security training within **[Duration, e.g., 5 business days]** of account creation |
| **7** | **PAM System** | Require approval for each privileged session through **[Approval Process, e.g., manager approval, security team approval]** |
| **8** | **Security Operations Center** | Monitor privileged account usage in real-time and investigate suspicious activities within **[Duration, e.g., 15 minutes]** |
| **9** | **PAM System** | Record all privileged sessions including keystrokes, commands, and file access for audit and investigation purposes |
| **10** | **System Administrator** | Generate daily privileged account usage reports including login times, commands executed, and systems accessed |
| **11** | **Information Security Officer** | Review weekly privileged account activity reports and investigate any anomalous or unauthorized usage patterns |
| **12** | **Account Manager** | Conduct monthly review of assigned privileged accounts to verify continued business need and appropriate access levels |
| **13** | **Human Resources** | Immediately disable privileged accounts upon employee termination, role change, or extended leave of absence |
| **14** | **Information Security Officer** | Perform quarterly comprehensive review of all privileged accounts including access validation, usage analysis, and compliance assessment |
| **15** | **System Administrator** | Rotate privileged account passwords quarterly using **[Password Management System]** with **[Complexity Requirements, e.g., 20+ characters]** |
| **16** | **Compliance Officer** | Maintain privileged account audit logs and session recordings for minimum **[Retention Period, e.g., 7 years]** for regulatory compliance |
| **17** | **Information Security Officer** | Generate annual privileged access risk assessment and update access controls based on threat landscape and business requirements |

### 5. Standards Compliance

This procedure addresses the following regulatory and compliance requirements:

| **Procedure Section** | **Standard/Framework** | **Control Reference** |
| --------------------- | ---------------------- | --------------------- |
| **4.1, 4.2, 4.3** | HITRUST CSF v11.2.0 | 11.a - User Access Provisioning |
| **4.4, 4.6, 4.15** | HITRUST CSF v11.2.0 | 11.b - Privileged Access Management |
| **4.8, 4.9, 4.11** | HITRUST CSF v11.2.0 | 12.a - Audit Logging and Monitoring |
| **4.12, 4.14** | HITRUST CSF v11.2.0 | 11.c - User Access Review |
| **4.13** | HITRUST CSF v11.2.0 | 11.d - User Access Revocation |
| **4.1, 4.2, 4.3** | SOC 2 Trust Services Criteria | CC6.2 - Logical Access Controls |
| **4.4, 4.5, 4.6** | SOC 2 Trust Services Criteria | CC6.3 - Multi-Factor Authentication |
| **4.8, 4.9, 4.11** | SOC 2 Trust Services Criteria | CC7.2 - System Monitoring |
| **4.1, 4.13** | HIPAA Security Rule | 45 CFR § 164.308(a)(4) - Access Management |
| **4.8, 4.9, 4.16** | HIPAA Security Rule | 45 CFR § 164.312(b) - Audit Controls |

### 6. Artifact(s)

- Privileged account request and approval documentation
- PAM system session recordings and audit logs
- Quarterly privileged account review reports
- Annual privileged access risk assessment documentation

### 7. Definitions

- **Privileged Access Management (PAM):** Security solution that helps organizations restrict privileged access within an existing Active Directory environment and control, monitor, and audit privileged users.

- **Break-Glass Access:** Emergency access procedure that allows authorized personnel to bypass normal access controls during critical situations.

- **Multi-Factor Authentication (MFA):** Security method that requires multiple forms of verification to authenticate user identity.

- **Session Recording:** Automated capture of all activities performed during a privileged user session for audit and investigation purposes.

### 8. Responsibilities

| **Role** | **Responsibility** |
| -------- | ---------------- |
| **Information Security Officer** | Configure automated monitoring rules, approve privileged account requests, conduct quarterly reviews, and coordinate compliance assessments. |
| **System Administrator** | Create privileged accounts, configure PAM systems, generate usage reports, and rotate passwords according to schedule. |
| **Account Manager** | Conduct monthly reviews of assigned privileged accounts and verify continued business need for access. |
| **Human Resources** | Immediately notify IT of employee terminations and role changes affecting privileged access. |
| **Compliance Officer** | Maintain audit logs and session recordings for regulatory compliance and retention requirements. |


