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

**3.1 Principle of Least Privilege**

All access rights shall be granted based on the principle of least privilege. Workforce members shall only be provided with the minimum level of access to data and systems necessary to perform their assigned job responsibilities. Access that is not explicitly granted is implicitly denied.

**3.2 User Access Lifecycle Management**

Access rights shall be managed throughout the entire duration of a user's relationship with the company.

- **Provisioning:** Access for new workforce members shall be requested by their direct manager through the official IT service request process. Access rights shall be assigned based on pre-defined roles and responsibilities documented in the user's job description.
    
- **Modification:** When a workforce member changes roles or responsibilities within the company, their manager shall submit a request to modify access rights. All previous access rights that are no longer required for the new role shall be revoked, and new access rights shall be granted according to the principle of least privilege.
    
- **Deprovisioning:** Upon termination of employment or contract, all access to company systems, applications, and physical facilities shall be revoked in a timely manner, not to exceed **[Number, e.g., 24]** hours from the official termination time. For involuntary terminations or other high-risk separation events, all logical and physical access shall be revoked immediately, concurrent with the termination event whenever possible.
    

**3.3 Access Reviews**

To ensure access rights remain appropriate, formal access reviews shall be conducted periodically. The designation of systems as containing ePHI or Confidential data shall be formally documented in the **[Company Name]** System & Data Inventory.

- Access to systems containing ePHI or other data classified as Confidential shall be reviewed by the respective system owner or manager on a quarterly basis.
    
- All other user access rights shall be reviewed on at least an annual basis.
    
- The review shall require a formal, documented attestation (e.g., digital sign-off via a ticket) from the designated manager or system owner. Failure to complete a required access review within **[Number, e.g., 14]** days of the deadline shall result in an automatic escalation to the Security Officer and the manager's direct superior.
    
- The results of all access reviews, including any modifications made, shall be documented and retained as evidence of compliance.
    

**3.4 Privileged Access Management**

Accounts with elevated (administrative) privileges pose a significant risk and shall be subject to stricter controls.

- Administrative access shall be granted on a limited, as-needed basis. For accounts with the highest level of administrative privilege (e.g., 'root' or 'global administrator'), access shall be granted on a time-bound, just-in-time (JIT) basis where technically feasible. All such access sessions shall require explicit approval and be automatically logged and terminated after the approved duration.
    
- Workforce members with administrative privileges shall use a dedicated, separate account for performing administrative tasks. Standard day-to-day activities shall be performed using a non-privileged user account.
    
- Multi-Factor Authentication (MFA) is mandatory for all privileged access accounts.
    
- All activities performed using a privileged account shall be logged and monitored for suspicious behavior.
    

**3.5 System and Network Access Controls**

Logical access to systems and networks shall be secured as follows:

- **Unique Identification:** Every user shall be assigned a unique user ID. The use of shared or generic user accounts is strictly prohibited.
    
- **Authentication:** All access shall be authenticated through a combination of a unique user ID and a strong password, as defined in the Password Policy (SEC-POL-002). MFA is required for all sensitive systems.
    
- **Session Timeouts:** Systems shall be configured to automatically terminate user sessions after a defined period of inactivity, not to exceed **[Duration, e.g., 15 minutes]** for systems containing ePHI.
    
- **Network Segregation:** The corporate network shall be segregated into logical zones (e.g., production, development, DMZ) with access controls and firewalls in place to restrict traffic between zones to only what is explicitly authorized.
    

**3.6 Third-Party Access**

Prior to granting any access, all third parties shall undergo a formal security and compliance review, as defined in the Vendor Management Policy. Any third party that will access, store, or process ePHI on behalf of **[Company Name]** shall have a signed Business Associate Agreement (BAA) in place before access is provisioned.

Third-party access shall be:

- Limited to only the specific systems and data required for their function.
    
- Time-bound, with access automatically expiring upon contract termination.
    
- Monitored, with all activities logged and reviewed.
    

### 4. Standards Compliance

This policy is designed to comply with and support the following industry standards and regulations.

| **Policy Section** | **Standard/Framework**        | **Control Reference**                                         |
| ------------------ | ----------------------------- | ------------------------------------------------------------- |
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