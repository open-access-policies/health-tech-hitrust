---
title: Automated Access Review and Monitoring Procedure (AC-PROC-003)
parent: Access Control Procedures
nav_order: 3
---

### 1. Purpose

To define the process for automated monitoring and exception-based review of user access rights to ensure adherence to the principle of least privilege while minimizing administrative overhead through automation and intelligent alerting.

### 2. Scope

This procedure applies to all user accounts with access to company information systems, automated identity and access management systems, and the Security Officer and managers responsible for responding to access anomaly alerts.

### 3. Overview

This procedure describes the automated approach to access monitoring and exception-based reviews that replace traditional manual quarterly access reviews. It utilizes role-based access control (RBAC), automated anomaly detection, and targeted reviews triggered by specific events or risk indicators, ensuring compliance while enabling operational efficiency for a growing organization.

### 4. Procedure

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Platform Engineer | **Automated RBAC Configuration**: Configure identity and access management (IAM) systems to automatically assign access based on job roles, department, and manager hierarchy integrated with HR systems. Ensure role definitions align with job functions and are automatically updated when employees change positions. |
| **2** | Security Officer | **Access Monitoring Rules Setup**: Configure automated monitoring rules to detect access anomalies including: accounts with no login activity for **[Duration, e.g., 90 days]**, privilege escalation events, access from unusual locations, and users with access beyond their role requirements. |
| **3** | DevOps Engineer | **Automated Alert Configuration**: Set up automated alerts for access anomalies that require review: dormant accounts, excessive privileges, failed access attempts, and role misalignments. Configure alert thresholds to minimize false positives while maintaining security visibility. |
| **4** | IAM System | **Daily Automated Monitoring**: Automated systems continuously monitor user access patterns, login activities, and privilege usage. Generate daily reports on access anomalies and potential security risks without requiring manual intervention. |
| **5** | Security Officer | **Weekly Anomaly Review**: Review weekly automated reports of access anomalies and security alerts. Investigate high-priority alerts within **[Timeframe, e.g., 3 business days]** and coordinate with managers for access validation or remediation. |
| **6** | Manager/System Owner | **Exception-Based Review Response**: When alerted about access anomalies for their team members or systems, review and validate access requirements within **[Timeframe, e.g., 5 business days]**. Approve continued access or request access modification through automated workflows. |
| **7** | Platform Engineer | **Automated Access Remediation**: Implement automated access remediation for common scenarios: disable dormant accounts after **[Duration, e.g., 120 days]** of inactivity, remove access for terminated employees, and adjust access based on role changes automatically synced from HR systems. |
| **8** | Security Officer | **Risk-Based Targeted Reviews**: Conduct targeted access reviews for high-risk scenarios: **Critical Systems** (ePHI, production databases): Semi-annual automated reviews with manager attestation. **Privileged Accounts**: Quarterly automated validation with usage analysis. **Third-Party Access**: Event-driven reviews when contracts change or security incidents occur. |
| **9** | Platform Engineer | **Compliance Reporting**: Generate automated compliance reports showing access control effectiveness, review completion rates, remediation actions, and audit trail documentation for regulatory requirements. |
| **10** | Security Officer | **Quarterly Program Assessment**: Assess the effectiveness of automated access monitoring, review alert accuracy and response times, and optimize automation rules to reduce false positives while maintaining security coverage. |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework** | **Control Reference** |
| --------------------- | ---------------------- | --------------------- |
| **All** | SOC 2 Trust Services Criteria | CC6.1 - Logical Access Security |
| **4.4-4.6** | SOC 2 Trust Services Criteria | CC6.2 - Access Authorization |
| **4.7-4.8** | SOC 2 Trust Services Criteria | CC6.3 - Access Reviews |
| **All** | HIPAA Security Rule | 45 CFR § 164.308(a)(4) - Information Access Management |
| **4.8** | HIPAA Security Rule | 45 CFR § 164.312(a)(1) - Access Control |
| **All** | HITRUST CSF v11.2.0 | 11.b - User Access Management |
| **6** | HITRUST CSF v11.2.0 | 11.c - User Responsibilities |

### 6. Artifact(s)

- Automated access monitoring configuration documentation
- Weekly access anomaly reports and investigation summaries
- Semi-annual high-risk system access validation records
- Manager access validation responses and approval workflows
- Automated remediation logs and compliance reporting summaries

### 7. Definitions

**Role-Based Access Control (RBAC):** Access control method that restricts system access based on pre-defined roles within an organization.

**Access Anomaly:** Deviation from normal access patterns that may indicate security risks or policy violations.

**Exception-Based Review:** Access review process triggered by specific events or risk indicators rather than fixed time schedules.

**Just-In-Time (JIT) Access:** Security feature that provides temporary, time-limited access to resources when needed.

**Principle of Least Privilege:** Security concept that users should have the minimum levels of access necessary to complete their job functions.

### 8. Responsibilities

| **Role** | **Responsibility** |
| -------- | ---------------- |
| **Security Officer** | Configure automated monitoring rules, review access anomalies, and coordinate exception-based reviews. |
| **Platform Engineer** | Implement RBAC systems, configure automated remediation, and maintain IAM integrations with HR systems. |
| **DevOps Engineer** | Set up automated alerting, monitor system performance, and optimize alert thresholds. |
| **Managers/System Owners** | Respond to access validation requests and approve access changes for their team members or systems. |
| **HR Department** | Maintain accurate role and manager information in HR systems for automated access management. |
