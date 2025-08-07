---
title: Access Control Policy (AC-POL-001)
parent: Access Control Policies
nav_order: 1
---

### 1. Objective

The objective of this policy is to define the requirements for managing access to **[Company Name]**'s information systems, data, and physical facilities. This policy ensures that access is granted based on the principles of least privilege and separation of duties, thereby protecting the confidentiality, integrity, and availability of corporate and customer information, including electronic Protected Health Information (ePHI).

### 2. Scope

This policy applies to all **[Company Name]** workforce members, third-party contractors, and vendors who require access to any company information asset. This includes, but is not limited to, applications, servers, databases, network devices, and cloud services. This policy applies to all physical and virtual locations where company information assets are accessed, stored, or processed, including corporate offices, remote work locations, and third-party sites.

### 3. Policy

Access to all **[Company Name]** information assets shall be managed through a formal, documented process that is consistently applied and audited.

#### 3.1 Principle of Least Privilege

All access rights shall be granted based on the principle of least privilege. Workforce members shall only be provided with the minimum level of access to data and systems necessary to perform their assigned job responsibilities. Access that is not explicitly granted is implicitly denied.

#### 3.2 User Access Lifecycle Management

Access rights shall be managed throughout the entire duration of a user's relationship with the company.

- **Provisioning:** Access for new workforce members shall be requested by their direct manager through the official IT service request process. Access rights shall be assigned based on pre-defined roles and responsibilities documented in the user's job description.
    
- **Modification:** When a workforce member changes roles or responsibilities within the company, their manager shall submit a request to modify access rights. All previous access rights that are no longer required for the new role shall be revoked, and new access rights shall be granted according to the principle of least privilege.
    
- **Deprovisioning:** Upon termination of employment or contract, all access to company systems, applications, and physical facilities shall be revoked in a timely manner. **Critical/High-Risk Terminations** (involuntary terminations, security incidents, executive departures): All logical and physical access shall be revoked within **[Number, e.g., 2]** hours. **Standard Terminations** (voluntary resignations, contract completions): All access shall be revoked within **[Number, e.g., 24]** hours from the official termination time. **Low-Risk Extended Transitions** (retirements, internal transfers): Access revocation may be coordinated over **[Number, e.g., 72]** hours to ensure smooth knowledge transfer.
    

#### 3.3 Automated Access Reviews and Monitoring

To ensure access rights remain appropriate while minimizing administrative overhead, access reviews shall utilize automated monitoring and exception-based reviews rather than manual quarterly attestations.

- **Automated Monitoring:** Identity and access management systems shall be configured to automatically detect and alert on access anomalies including: dormant accounts (no login for **[Duration, e.g., 90 days]**), privilege escalation, unusual access patterns, and accounts without recent manager validation.
    
- **Role-Based Access Control (RBAC):** Access rights shall be primarily managed through automated role assignment based on job function, department, and manager hierarchy integrated with the HR information system. When employees change roles, access shall be automatically adjusted based on their new role assignment.
    
- **Exception-Based Reviews:** Formal access reviews shall be triggered by specific events rather than fixed quarterly schedules: **High-Risk Systems** (ePHI, financial data, production environments): Semi-annual reviews or when automated monitoring identifies exceptions. **Standard Systems**: Annual reviews or when significant access anomalies are detected. **Low-Risk Systems** (internal tools, development environments): Exception-based reviews only when security concerns are identified.
    
- **Escalation and Remediation:** Automated alerts for access anomalies shall be sent to system owners and managers for resolution within **[Number, e.g., 7]** business days. Failure to respond to access alerts shall result in automatic escalation to the Security Officer and potential access suspension for high-risk systems.
    

#### 3.4 Privileged Access Management

Accounts with elevated (administrative) privileges pose a significant risk and shall be subject to enhanced controls utilizing modern just-in-time access principles.

- **Just-In-Time (JIT) Access:** Administrative access shall be granted on a limited, time-bound basis using automated JIT access systems where technically feasible. **Critical Infrastructure Access** (production databases, cloud administrative consoles): Maximum session duration of **[Duration, e.g., 4 hours]** with automatic termination. **Standard Administrative Access** (system administration, application management): Maximum session duration of **[Duration, e.g., 8 hours]** with renewal available. **Development and Testing Access**: Maximum session duration of **[Duration, e.g., 24 hours]** with self-service renewal.
    
- **Separated Administrative Accounts:** Workforce members with administrative privileges shall use dedicated administrative accounts separate from their standard user accounts. Standard day-to-day activities shall be performed using non-privileged accounts with automatic elevation requests for administrative tasks when needed.
    
- **Enhanced Authentication:** Multi-Factor Authentication (MFA) is mandatory for all privileged access accounts. Additional authentication factors (hardware tokens, biometrics) may be required for critical infrastructure access.
    
- **Automated Monitoring and Alerting:** All privileged account activities shall be automatically logged and monitored. Real-time alerts shall be generated for unusual privileged access patterns, after-hours usage, and potential privilege abuse.
    

#### 3.5 System and Network Access Controls

Logical access to systems and networks shall be secured as follows:

- **Unique Identification:** Every user shall be assigned a unique user ID. The use of shared or generic user accounts is strictly prohibited.
    
- **Authentication:** All access shall be authenticated through a combination of a unique user ID and a strong password, as defined in the Password Policy (SEC-POL-002). MFA is required for all sensitive systems.
    
- **Session Timeouts:** Systems shall be configured to automatically terminate user sessions after a defined period of inactivity, not to exceed **[Duration, e.g., 15 minutes]** for systems containing ePHI.
    
- **Network Segregation:** The corporate network shall be segregated into logical zones (e.g., production, development, DMZ) with access controls and firewalls in place to restrict traffic between zones to only what is explicitly authorized.
    

#### 3.6 Third-Party Access

Prior to granting any access, all third parties shall undergo a formal security and compliance review, as defined in the Vendor Management Policy. Any third party that will access, store, or process ePHI on behalf of **[Company Name]** shall have a signed Business Associate Agreement (BAA) in place before access is provisioned.

Third-party access shall be:

- Limited to only the specific systems and data required for their function.
    
- Time-bound, with access automatically expiring upon contract termination.
    
- Monitored, with all activities logged and reviewed.
    

### 4. Standards Compliance

This policy is designed to comply with and support the following industry standards and regulations.

| **Policy Section** | **Standard/Framework**        | **Control Reference**                                         |
| ------------------ | ----------------------------- | ------------------------------------------------------------- |
| **All**            | HITRUST CSF v11.2.0          | 11.a - Access Control Policy                                 |
| **3.2, 3.3**       | HITRUST CSF v11.2.0          | 11.b - User Access Management                                |
| **3.4**            | HITRUST CSF v11.2.0          | 11.c - User Responsibilities                                 |
| **3.5**            | HITRUST CSF v11.2.0          | 11.d - Network Access Control                                |
| **3.6**            | HITRUST CSF v11.2.0          | 11.e - Operating System Access Control                       |
| **All**            | HIPAA Security Rule           | 45 CFR § 164.308(a)(4) - Information Access Management        |
| **3.2, 3.5**       | HIPAA Security Rule           | 45 CFR § 164.312(a)(1) - Access Control                       |
| **3.5**            | HIPAA Security Rule           | 45 CFR § 164.312(a)(2)(i) - Unique User Identification        |
| **All**            | SOC 2 Trust Services Criteria | CC6.1 - Logical Access Security                               |
| **3.2, 3.3**       | SOC 2 Trust Services Criteria | CC6.2 - Prior to issuing system credentials...                |
| **3.2, 3.6**       | SOC 2 Trust Services Criteria | CC6.3 - Authorization, modification, and removal of access... |

### 5. Definitions

- **Least Privilege:** The security principle of restricting access rights for users to the bare minimum permissions they need to perform their work.
    
- **Role-Based Access Control (RBAC):** A method of restricting network access based on the roles of individual users within an enterprise.
    
- **Privileged Account:** A user account with elevated permissions, such as administrator, root, or system accounts.
    
- **Business Associate Agreement (BAA):** A written contract between a covered entity and a business associate as required by HIPAA.
    

### 6. Responsibilities

| **Role**                     | **Responsibility**                                                                                                                |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Security Officer / Team**  | Own, review, and update this policy annually. Audit access controls and review compliance.                                        |
| **IT Department**            | Implement, manage, and monitor technical access controls. Process access provisioning, modification, and deprovisioning requests. |
| **Managers / System Owners** | Request and approve access for their direct reports. Conduct periodic access reviews for their teams and systems.                 |
| **All Workforce Members**    | Adhere to this policy, use only their assigned accounts, and report any unauthorized access or suspicious activity.               |