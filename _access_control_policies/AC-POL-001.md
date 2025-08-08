---
title: Identity and Access Management (IAM) Policy (AC-POL-001)
parent: Access Control Policies
nav_order: 1
---

### 1. Objective

The objective of this policy is to define the requirements for managing user identities and access rights to **[Company Name]**'s information systems and data throughout the complete user lifecycle. This policy ensures that access is granted based on the principles of least privilege and separation of duties, while implementing automated access management processes that minimize administrative overhead and enhance security effectiveness. This policy focuses on standard user access management, while privileged access is addressed in the Privileged Access Management Policy (AC-POL-004) and remote access is covered in the Remote Work Policy (AC-POL-003).

### 2. Scope

This policy applies to all **[Company Name]** workforce members, third-party contractors, and vendors who require access to company information assets. This includes standard user access to applications, file shares, collaboration tools, and business systems. This policy applies to all physical and virtual locations where company information assets are accessed, stored, or processed, including corporate offices and approved remote work locations. This policy does not cover privileged administrative access (see AC-POL-004) or remote work security requirements (see AC-POL-003).

### 3. Policy

Access to all **[Company Name]** information assets shall be managed through a formal, documented process that implements automated access management and exception-based reviews to ensure appropriate access while minimizing administrative overhead.

#### 3.1 Principle of Least Privilege

All access rights shall be granted based on the principle of least privilege. Workforce members shall only be provided with the minimum level of access to data and systems necessary to perform their assigned job responsibilities. Access that is not explicitly granted is implicitly denied.

#### 3.2 User Access Lifecycle Management

Access rights shall be managed throughout the entire duration of a user's relationship with the company.

##### 3.2.1 Access Provisioning

Access for new workforce members shall be provisioned through a formal request submitted by their direct manager via the official IT service request process. Access rights shall be assigned exclusively based on pre-defined roles and responsibilities documented in the user's job description and organizational role matrix.

##### 3.2.2 Access Modification

When a workforce member changes roles or responsibilities within the company, their manager shall submit a formal request to modify access rights through the designated change management process. All previous access rights that are no longer required for the new role shall be immediately revoked. New access rights shall be granted strictly according to the principle of least privilege and the requirements of the new role.

##### 3.2.3 Access Deprovisioning

Upon termination of employment or contract, all access to company systems, applications, and physical facilities shall be revoked according to risk-based timelines. **Critical/High-Risk Terminations** (involuntary terminations, security incidents, executive departures): All logical and physical access shall be revoked within **[Number, e.g., 2]** hours of notification. **Standard Terminations** (voluntary resignations, contract completions): All access shall be revoked within **[Number, e.g., 24]** hours from the official termination time. **Low-Risk Extended Transitions** (retirements, internal transfers): Access revocation shall be coordinated over **[Number, e.g., 72]** hours to ensure smooth knowledge transfer while maintaining security controls.
    

#### 3.3 Automated Access Reviews and Monitoring

To ensure access rights remain appropriate while minimizing administrative overhead, access reviews shall utilize automated monitoring and exception-based reviews rather than manual quarterly attestations.

##### 3.3.1 Automated Monitoring Requirements

Identity and access management systems shall be configured to automatically detect and alert on access anomalies. These monitoring systems shall identify dormant accounts with no login activity for **[Duration, e.g., 90 days]**, privilege escalation events, unusual access patterns, and accounts without recent manager validation.

##### 3.3.2 Role-Based Access Control Implementation

Access rights shall be managed primarily through automated role assignment based on job function, department, and manager hierarchy integrated with the HR information system. When employees change roles, access shall be automatically adjusted based on their new role assignment without manual intervention.

##### 3.3.3 Exception-Based Review Schedule

Formal access reviews shall be triggered by specific events rather than fixed quarterly schedules. **High-Risk Systems** (ePHI, financial data, production environments) shall undergo semi-annual reviews or when automated monitoring identifies exceptions. **Standard Systems** shall undergo annual reviews or when significant access anomalies are detected. **Low-Risk Systems** (internal tools, development environments) shall undergo exception-based reviews only when security concerns are identified.

##### 3.3.4 Escalation and Remediation Process

Automated alerts for access anomalies shall be sent to system owners and managers for resolution within **[Number, e.g., 7]** business days. Failure to respond to access alerts shall result in automatic escalation to the Security Officer and potential access suspension for high-risk systems.

##### 3.3.1 Automated Access Review Implementation

- **RBAC Configuration and Management:**
    - Identity and access management (IAM) systems shall be configured to automatically assign access based on job roles, department, and manager hierarchy integrated with HR systems
    - Role definitions shall align with job functions and be automatically updated when employees change positions
    - Access assignments shall be standardized across the organization based on pre-defined role templates and business function requirements
    - Integration with HR systems shall ensure real-time synchronization of organizational changes affecting access requirements

- **Access Monitoring Rules and Alerting:**
    - Automated monitoring rules shall be configured to detect access anomalies including accounts with no login activity for **[Duration, e.g., 90 days]**, privilege escalation events, access from unusual locations, and users with access beyond their role requirements
    - Automated alerts shall be configured for access anomalies that require review: dormant accounts, excessive privileges, failed access attempts, and role misalignments
    - Alert thresholds shall be configured to minimize false positives while maintaining security visibility and effectiveness
    - Daily automated monitoring shall continuously assess user access patterns, login activities, and privilege usage without requiring manual intervention

- **Exception-Based Review Process:**
    - Weekly automated reports of access anomalies and security alerts shall be generated for Security Officer review
    - High-priority alerts shall be investigated within **[Timeframe, e.g., 3 business days]** with coordination between Security Officers and system managers
    - Managers and system owners shall review and validate access requirements within **[Timeframe, e.g., 5 business days]** when alerted about access anomalies for their team members or systems
    - Approval of continued access or requests for access modification shall be processed through automated workflows with proper documentation and audit trails

- **Automated Access Remediation:**
    - Automated access remediation shall be implemented for common scenarios including: disabling dormant accounts after **[Duration, e.g., 120 days]** of inactivity, removing access for terminated employees, and adjusting access based on role changes automatically synced from HR systems
    - Remediation actions shall be logged and reviewed to ensure appropriate application and effectiveness
    - Emergency access suspension capabilities shall be available for immediate response to security incidents or policy violations
    - Automated workflows shall handle routine access modifications while preserving audit trails and management oversight

- **Risk-Based Targeted Reviews:**
    - Targeted access reviews shall be conducted for high-risk scenarios based on automated risk assessment and monitoring:
    - **Critical Systems** (ePHI, production databases): Semi-annual automated reviews with manager attestation and usage analysis
    - **Privileged Accounts**: Quarterly automated validation with detailed usage analysis and anomaly detection
    - **Third-Party Access**: Event-driven reviews when contracts change, security incidents occur, or automated monitoring identifies anomalies
    - Risk-based review schedules shall be dynamically adjusted based on threat intelligence, business changes, and compliance requirements

- **Compliance Reporting and Assessment:**
    - Automated compliance reports shall be generated showing access control effectiveness, review completion rates, remediation actions, and audit trail documentation for regulatory requirements
    - Quarterly program assessments shall evaluate the effectiveness of automated access monitoring, review alert accuracy and response times, and optimize automation rules to reduce false positives while maintaining security coverage
    - Monthly metrics shall be maintained on access anomaly detection rates, remediation times, and manager response compliance
    - Annual reviews of the automated access monitoring program shall include effectiveness assessment, cost-benefit analysis, and recommendations for process improvements
    

#### 3.4 System and Network Access Controls

Logical access to systems and networks shall be secured through standardized authentication and session management controls.

##### 3.4.1 Unique User Identification

Every user shall be assigned a unique user ID for all system access. The use of shared or generic user accounts is strictly prohibited across all company systems and applications.

##### 3.4.2 Authentication Requirements

All system access shall be authenticated through a combination of a unique user ID and a strong password, as defined in the Password Policy (SEC-POL-002). Multi-factor authentication (MFA) shall be required for all systems containing sensitive data including ePHI.

##### 3.4.3 Session Management

Systems shall be configured to automatically terminate user sessions after a defined period of inactivity, not to exceed **[Duration, e.g., 15 minutes]** for systems containing ePHI. Session timeouts shall be enforced at both the application and network levels.

##### 3.4.4 Network Access Controls

Network access controls shall restrict user access to only authorized network segments and resources based on role and business need. Network segregation shall be implemented and maintained to enforce access boundaries.

#### 3.5 Privileged Access Management

Accounts with elevated administrative privileges are subject to enhanced controls as defined in the Privileged Access Management Policy (AC-POL-004). Standard users requiring administrative access shall follow the just-in-time access procedures and enhanced authentication requirements specified in that policy.
    

#### 3.6 Third-Party Access

Prior to granting any access, all third parties shall undergo a formal security and compliance review, as defined in the Vendor Management Policy. Any third party that will access, store, or process ePHI on behalf of **[Company Name]** shall have a signed Business Associate Agreement (BAA) in place before access is provisioned.

##### 3.6.1 Third-Party Security Review

Prior to granting any access, all third parties shall undergo a formal security and compliance review, as defined in the Vendor Management Policy. Any third party that will access, store, or process ePHI on behalf of **[Company Name]** shall have a signed Business Associate Agreement (BAA) in place before access is provisioned.

##### 3.6.2 Third-Party Access Restrictions

Third-party access shall be limited to only the specific systems and data required for their contractual function. Access scope shall be documented and approved by the system owner and security team before provisioning.

##### 3.6.3 Third-Party Access Management

Third-party access shall be time-bound, with access automatically expiring upon contract termination or completion of work. All third-party activities shall be monitored, with all access attempts and activities logged and reviewed according to the organization's monitoring standards.

#### 3.7 Remote Access

Remote access to company systems and data is governed by the Remote Work Policy (AC-POL-003), which establishes comprehensive security requirements for accessing company resources from locations outside corporate offices. All workforce members working remotely must comply with the network connectivity, device security, and data handling requirements specified in that policy.
    

### 4. Standards Compliance

This policy is designed to comply with and support the following industry standards and regulations.

| **Policy Section** | **Standard/Framework**        | **Control Reference**                                         |
| ------------------ | ----------------------------- | ------------------------------------------------------------- |
| **All**            | HITRUST CSF v11.2.0          | 11.a - Access Control Policy                                 |
| **3.2, 3.3**       | HITRUST CSF v11.2.0          | 11.b - User Access Management                                |
| **3.3.1**          | HITRUST CSF v11.2.0          | 11.c - User Responsibilities                                 |
| **3.4**            | HITRUST CSF v11.2.0          | 11.d - Network Access Control                                |
| **3.6**            | HITRUST CSF v11.2.0          | 11.e - Operating System Access Control                       |
| **All**            | HIPAA Security Rule           | 45 CFR § 164.308(a)(4) - Information Access Management        |
| **3.2, 3.4**       | HIPAA Security Rule           | 45 CFR § 164.312(a)(1) - Access Control                       |
| **3.3.1**          | HIPAA Security Rule           | 45 CFR § 164.312(a)(1) - Access Control                       |
| **3.4**            | HIPAA Security Rule           | 45 CFR § 164.312(a)(2)(i) - Unique User Identification        |
| **All**            | SOC 2 Trust Services Criteria | CC6.1 - Logical Access Security                               |
| **3.2, 3.3**       | SOC 2 Trust Services Criteria | CC6.2 - Prior to issuing system credentials...                |
| **3.3.1**          | SOC 2 Trust Services Criteria | CC6.2 - Access Authorization                                  |
| **3.3.1**          | SOC 2 Trust Services Criteria | CC6.3 - Access Reviews                                        |
| **3.2, 3.6**       | SOC 2 Trust Services Criteria | CC6.3 - Authorization, modification, and removal of access... |

### 5. Definitions

- **Identity and Access Management (IAM):** System of policies, processes, and technologies used to manage digital identities and control access to resources based on user roles and responsibilities.
    
- **Least Privilege:** The security principle of restricting access rights for users to the bare minimum permissions they need to perform their work.
    
- **Role-Based Access Control (RBAC):** A method of restricting network access based on the roles of individual users within an enterprise.
    
- **Account Lifecycle:** Complete process of user account creation, modification, review, and termination aligned with employment status and role changes.
    
- **Business Associate Agreement (BAA):** A written contract between a covered entity and a business associate as required by HIPAA.
    

### 6. Responsibilities

| **Role**                     | **Responsibility**                                                                                                                |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Security Officer / Team**  | Own, review, and update this policy annually. Audit access controls and review compliance. Configure automated monitoring rules, review access anomalies, and coordinate exception-based reviews. |
| **IT Department**            | Implement, manage, and monitor technical access controls. Process access provisioning, modification, and deprovisioning requests. |
| **Platform Engineer**        | Implement RBAC systems, configure automated remediation, and maintain IAM integrations with HR systems. |
| **DevOps Engineer**          | Set up automated alerting, monitor system performance, and optimize alert thresholds. |
| **Managers / System Owners** | Request and approve access for their direct reports. Conduct periodic access reviews for their teams and systems. Respond to access validation requests and approve access changes for their team members or systems. |
| **HR Department**            | Maintain accurate role and manager information in HR systems for automated access management. Immediately notify IT of employee terminations and role changes. |
| **Compliance Officer**       | Maintain access management documentation for audit purposes and ensure regulatory compliance requirements are met. |
| **All Workforce Members**    | Adhere to this policy, use only their assigned accounts, and report any unauthorized access or suspicious activity.               |