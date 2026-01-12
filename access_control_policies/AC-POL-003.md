# Remote Work Policy (AC-POL-003)

### 1. Objective

The objective of this policy is to establish the requirements for securely accessing **[Company Name]**'s information assets from locations outside of corporate offices. Because we handle sensitive health information, these security measures are not just company rules—they are essential for protecting patients, complying with laws like HIPAA, and maintaining the trust of our clients. This policy is designed to enable workforce productivity while ensuring the confidentiality, integrity, and availability of all data, including electronic Protected Health Information (ePHI), regardless of where work is performed.

### 2. Scope

This policy applies to all **[Company Name]** workforce members (including employees, contractors, and temporary staff) who work remotely, either on a full-time, part-time, or occasional basis. It covers any and all locations outside of a designated corporate office, including home offices, co-working spaces, and travel locations. This policy governs the use of both company-provided and personally-owned equipment used to access company resources.

### 3. Policy

All remote work must be conducted in a manner that actively protects company information and systems from unauthorized access, disclosure, or damage. This policy focuses on network connectivity, workspace security, and data handling requirements. Device security requirements are comprehensively addressed in the Mobile Device Security Policy (OP-POL-002).

#### 3.1 General Remote Work Security

Remote work arrangements shall be formally authorized and conducted in accordance with documented security procedures. Workforce members shall maintain the same level of information security when working remotely as when working in company facilities.

#### 3.3 Network Security

Workforce members shall ensure secure network connectivity for all remote work activities.

##### 3.3.1 VPN Requirements

All access to internal company systems, applications, and data repositories shall be established through the company-approved Virtual Private Network (VPN). The VPN client shall remain active for the entire duration of the remote work session.

##### 3.3.2 Network Security Restrictions

The use of public or untrusted Wi-Fi networks (e.g., in cafes, airports, hotels) for accessing or transmitting ePHI or other data classified as Confidential shall be strictly prohibited. If such a network must be used for general tasks, the VPN shall be mandatory.

##### 3.3.3 Home Network Security Standards

Workforce members shall secure their home wireless networks with strong encryption (WPA2 or better) and a complex, unique password. As part of their annual security attestation, all workforce members shall formally attest that their primary remote work network is secured in accordance with this policy.
    

#### 3.2 Endpoint Device Security Requirements

All devices used to access company resources remotely shall comply with the comprehensive security requirements defined in the Mobile Device Security Policy (OP-POL-002). This includes but is not limited to encryption, access controls, malware protection, patch management, and mobile device management (MDM) enrollment requirements.

Workforce members shall ensure their devices meet all applicable security standards as specified in OP-POL-002 before accessing company systems remotely. Device compliance verification and ongoing monitoring shall be conducted according to the procedures established in the Mobile Device Security Policy.
    

#### 3.3 Data Handling and Physical Security

Workforce members shall take precautions to protect the physical and digital privacy of information when working remotely.

##### 3.3.1 Data Storage Restrictions

Storing ePHI or other Confidential data on the local hard drive of a personally-owned device shall be strictly prohibited. All sensitive data shall be accessed and stored exclusively on company-managed cloud platforms or network shares.

#### 3.4 Data Handling and Storage

Workforce members shall take precautions to protect the confidentiality and integrity of company information when working remotely.

##### 3.4.1 Data Storage Restrictions

Storing ePHI or other Confidential data on the local hard drive of any remote device shall be strictly prohibited. All sensitive data shall be accessed and stored exclusively on company-managed cloud platforms or network shares.

##### 3.4.2 Physical Privacy Controls

Workforce members shall ensure their remote workspace provides adequate visual and auditory privacy to prevent unauthorized access to or disclosure of ePHI. This includes positioning screens away from public view and using privacy screens when working in shared environments.

#### 3.5 Physical Security of Remote Workspace

The remote workspace shall be secured against unauthorized physical access to company equipment and information.

##### 3.5.1 Workspace Security

Company equipment and sensitive information shall be secured when not in use. Workstations shall be locked when unattended, and devices shall be stored securely.

##### 3.5.2 Visitor Access Controls

Workforce members shall ensure that visitors to their remote workspace do not have access to company equipment or confidential information unless authorized.

#### 3.6 Incident Reporting

Any security incident, including but not limited to loss or theft of devices, suspected unauthorized access, or potential data breaches, shall be reported immediately to the Security Officer or IT Department according to the Incident Response Policy (RES-POL-001).
    

#### 3.4 Use of Personal Equipment (BYOD)

The use of personally-owned devices to access company resources is a privilege and is contingent upon adherence to specific security requirements. As a condition of using a personal device for work, workforce members shall provide formal consent to the installation of required security software and acknowledge **[Company Name]**'s right to remotely wipe corporate data (a process that targets only company information and applications, not personal data like photos, texts, or contacts). All personal devices shall be formally registered with the IT Department and may be required to have company-managed security software installed before access is granted, as further defined in the Bring Your Own Device (BYOD) Policy.

### 4. Standards Compliance

This policy is designed to comply with and support the following industry standards and regulations.

| **Policy Section** | **Standard/Framework**        | **Control Reference**                                                                                                            |
| ------------------ | ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **All**            | HITRUST CSF v11.2.0          | 11.g - Remote Access Control                                                                                                    |
| **3.3**            | HITRUST CSF v11.2.0          | 08.e - Network Security Controls                                                                                                |
| **3.2**            | HITRUST CSF v11.2.0          | 02.f - Remote Endpoint Security (via OP-POL-002)                                                                               |
| **3.3**            | HITRUST CSF v11.2.0          | 09.f - Secure Remote Access                                                                                                     |
| **All**            | HIPAA Security Rule           | 45 CFR § 164.308(a)(1)(ii)(B) - Authorization and/or supervision                                                                 |
| **3.3**            | HIPAA Security Rule           | 45 CFR § 164.312(e)(1) - Transmission Security                                                                                   |
| **3.2, 3.4**       | HIPAA Security Rule           | 45 CFR § 164.310(d)(1) - Device and Media Controls (via OP-POL-002)                                                            |
| **All**            | SOC 2 Trust Services Criteria | CC6.1 - Logical Access Security                                                                                                  |
| **3.2, 3.4**       | SOC 2 Trust Services Criteria | CC6.6 - The entity implements logical access security measures for assets...                                                     |
| **3.5**            | SOC 2 Trust Services Criteria | CC6.8 - The entity implements controls to prevent or detect and act upon the introduction of unauthorized or malicious software. |

### 5. Definitions

- **Remote Work:** Any work performed for **[Company Name]** from a location that is not a designated corporate office.
    
- **Virtual Private Network (VPN):** A secure, encrypted connection over a public network to a private network.
    
- **Company-Provided Equipment:** Laptops, mobile devices, and any other hardware owned by **[Company Name]** and issued to a workforce member.
    
- **Mobile Device Management (MDM):** Software used by the IT Department to manage and secure mobile devices like phones and tablets.
    
- **Endpoint Detection and Response (EDR):** Security software that monitors devices like laptops for suspicious activity and potential threats.
    

### 6. Responsibilities

| **Role**                    | **Responsibility**                                                                                                                                                                                   |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Security Officer / Team** | Own, review, and update this policy annually. Monitor remote access logs for compliance and suspicious activity.                                                                                     |
| **IT Department**           | Maintain and manage the VPN and other remote access technologies. Assist workforce members with the secure configuration of their devices.                                                           |
| **Managers**                | Ensure their direct reports are aware of and understand this policy. Report any non-compliance or remote-work-related security concerns to the IT Department or Security Officer.                    |
| **All Workforce Members**   | Adhere to this policy at all times when working remotely. Ensure the security of their remote work environment and company assets. Immediately report any security incidents or lost/stolen devices. |