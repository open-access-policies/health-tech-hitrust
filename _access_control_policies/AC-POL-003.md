---
title: Remote Work Policy (AC-POL-003)
parent: Access Control Policies
nav_order: 3
---
### 1. Objective

The objective of this policy is to establish the requirements for securely accessing **[Company Name]**'s information assets from locations outside of corporate offices. Because we handle sensitive health information, these security measures are not just company rules—they are essential for protecting patients, complying with laws like HIPAA, and maintaining the trust of our clients. This policy is designed to enable workforce productivity while ensuring the confidentiality, integrity, and availability of all data, including electronic Protected Health Information (ePHI), regardless of where work is performed.

### 2. Scope

This policy applies to all **[Company Name]** workforce members (including employees, contractors, and temporary staff) who work remotely, either on a full-time, part-time, or occasional basis. It covers any and all locations outside of a designated corporate office, including home offices, co-working spaces, and travel locations. This policy governs the use of both company-provided and personally-owned equipment used to access company resources.

### 3. Policy

All remote work must be conducted in a manner that actively protects company information and systems from unauthorized access, disclosure, or damage.

**3.1 Secure Network Connectivity**

Workforce members are responsible for ensuring they use a secure network connection for all remote work.

- **VPN Mandate:** All access to internal company systems, applications, and data repositories shall be established through the company-approved Virtual Private Network (VPN). The VPN client shall be active for the entire duration of the remote work session.
    
- **Prohibition of Unsecured Networks:** The use of public or untrusted Wi-Fi networks (e.g., in cafes, airports, hotels) for accessing or transmitting ePHI or other data classified as Confidential is strictly prohibited. If such a network shall be used for general tasks, the VPN is mandatory.
    
- **Home Network Security:** Workforce members shall secure their home wireless networks with strong encryption (WPA2 or better) and a complex, unique password. As part of their annual security attestation, all workforce members shall formally attest that their primary remote work network is secured in accordance with this policy.
    

**3.2 Device Security Requirements**

Any device used to access company resources remotely, whether company-provided or personally-owned, shall meet the following minimum security standards. Compliance with these requirements is enforced through the company's security software (such as Mobile Device Management (MDM) or Endpoint Detection and Response (EDR) solutions). Devices that do not meet these minimum standards may be blocked from accessing corporate resources.

- **Encryption:** Full-disk encryption shall be enabled.
    
- **Access Control:** The device shall be protected by a strong password or biometric control, compliant with the Password Policy (SEC-POL-002), and shall be configured to automatically lock after **[Number, e.g., 15]** minutes of inactivity.
    
- **Malware Protection:** Company-approved anti-malware software shall be installed, active, and configured to receive automatic updates.
    
- **Patch Management:** The operating system and all applications shall be kept up-to-date with the latest security patches.
    

**3.3 Data Handling and Physical Security**

Workforce members shall take precautions to protect the physical and digital privacy of information when working remotely.

- **ePHI Storage:** Storing ePHI or other Confidential data on the local hard drive of a personally-owned device is strictly prohibited. All sensitive data shall be accessed and stored exclusively on company-managed cloud platforms or network shares.
    
- **Physical Privacy:** Workforce members shall take reasonable measures to prevent unauthorized viewing of their screens in public or shared spaces. This includes the use of privacy screens where appropriate and positioning screens away from public view.
    
- **Verbal Privacy:** Confidential or sensitive information shall not be discussed in public areas where conversations can be overheard.
    
- **Secure Document Handling:** Any printed documents containing sensitive information shall be handled securely and physically destroyed (e.g., via shredding) when no longer needed. Documents shall not be left unattended in unsecured locations.
    
- **Asset Protection:** Workforce members are responsible for the physical security of company-provided equipment. Devices shall never be left unattended in vehicles or unsecured public locations. Any loss or theft of a device used for company business shall be reported immediately to the IT Department and the Security Officer, and in no case later than **[Number, e.g., 24]** hours after discovery.
    
- **Data Removal After Employment:** Upon termination, workforce members shall cooperate with the IT Department to ensure the secure removal of all company data, applications, and access credentials from any personally-owned devices used for work.
    

**3.4 Use of Personal Equipment (BYOD)**

The use of personally-owned devices to access company resources is a privilege and is contingent upon adherence to specific security requirements. As a condition of using a personal device for work, workforce members shall provide formal consent to the installation of required security software and acknowledge **[Company Name]**'s right to remotely wipe corporate data (a process that targets only company information and applications, not personal data like photos, texts, or contacts). All personal devices shall be formally registered with the IT Department and may be required to have company-managed security software installed before access is granted, as further defined in the Bring Your Own Device (BYOD) Policy.

### 4. Standards Compliance

This policy is designed to comply with and support the following industry standards and regulations.

| **Policy Section** | **Standard/Framework**        | **Control Reference**                                                                                                            |
| ------------------ | ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **All**            | HIPAA Security Rule           | 45 CFR § 164.308(a)(1)(ii)(B) - Authorization and/or supervision                                                                 |
| **3.1, 3.2**       | HIPAA Security Rule           | 45 CFR § 164.312(e)(1) - Transmission Security                                                                                   |
| **3.2, 3.3**       | HIPAA Security Rule           | 45 CFR § 164.310(d)(1) - Device and Media Controls                                                                               |
| **All**            | SOC 2 Trust Services Criteria | CC6.1 - Logical Access Security                                                                                                  |
| **3.2, 3.3**       | SOC 2 Trust Services Criteria | CC6.6 - The entity implements logical access security measures for assets...                                                     |
| **3.3**            | SOC 2 Trust Services Criteria | CC6.8 - The entity implements controls to prevent or detect and act upon the introduction of unauthorized or malicious software. |

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