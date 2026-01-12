# Identity and Access Management (IAM) Policy (AC-POL-001)

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

Access reviews for standard (non-privileged) access shall be conducted at least annually. Privileged access review cadence is defined in the Privileged Access Management Policy (AC-POL-004) and shall be performed quarterly. Continuous monitoring and event-driven reviews shall supplement these schedules.

##### 3.3.1 Automated Monitoring Requirements

Identity and access management systems shall be configured to automatically detect and alert on access anomalies. These monitoring systems shall identify dormant accounts with no login activity for **[Duration, e.g., 90 days]**, privilege escalation events, unusual access patterns, and accounts without recent manager validation.

##### 3.3.2 Role-Based Access Control Implementation

Access rights shall be managed primarily through automated role assignment based on job function, department, and manager hierarchy integrated with the HR information system. When employees change roles, access shall be automatically adjusted based on their new role assignment without manual intervention.

##### 3.3.3 Exception-Based Review Schedule

- Standard (non-privileged) access: Annual reviews with manager/system owner attestation and usage analysis
- Privileged accounts: Quarterly reviews per AC-POL-004 (PAM), with detailed usage analysis and anomaly detection
- Event-driven reviews: Conducted upon significant role changes, mergers/acquisitions, security incidents, or when monitoring identifies anomalies

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

See [Annex: Control Mapping](../_annexes/control_mapping.md)

### 5. Definitions

See [Annex: Glossary](../_annexes/glossary.md)

### 6. Responsibilities

| **Role**                     | **Responsibility**                                                                                                                |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Security Officer / Team**  | Own, review, and update this policy annually. Audit access controls and review compliance. Configure automated monitoring rules, review access anomalies, and coordinate exception-based reviews. |
| **IT Department**            | Implement, manage, and monitor technical access controls. Process access provisioning, modification, and deprovisioning requests. |
| **Platform Engineer**        | Implement RBAC systems, configure automated remediation, and maintain IAM integrations with HR systems. |
| **DevOps Engineer**          | Set up automated alerting, monitor system performance, and optimize alert thresholds. |
| **Managers / System Owners** | Request and approve access for their direct reports. Conduct annual access reviews for their teams and systems and respond to access validation requests. |
| **HR Department**            | Maintain accurate role and manager information in HR systems for automated access management. Immediately notify IT of employee terminations and role changes. |
| **Compliance Officer**       | Maintain access management documentation for audit purposes and ensure regulatory compliance requirements are met. |
| **All Workforce Members**    | Adhere to this policy, use only their assigned accounts, and report any unauthorized access or suspicious activity.               |