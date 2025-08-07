---
title: Data Classification and Handling Policy (SEC-POL-004)
parent: Security Policies
nav_order: 4
---
### 1. Objective

The objective of this policy is to establish a comprehensive framework for classifying, handling, and protecting **[Company Name]**'s information assets based on their sensitivity, value, and regulatory requirements. This policy ensures that appropriate security controls are applied consistently across all information types, with particular emphasis on protecting electronic Protected Health Information (ePHI) and other sensitive data in accordance with HIPAA, HITECH, and SOC 2 requirements.

### 2. Scope

This policy applies to all **[Company Name]** workforce members, including employees, contractors, temporary staff, and third parties who create, access, process, store, transmit, or dispose of company information. It encompasses all information in any format (electronic, physical, or verbal) and at any location (on-premises, cloud, mobile devices, or third-party facilities). This policy covers the entire information lifecycle from creation to secure disposal.

### 3. Policy

All **[Company Name]** information shall be classified according to its sensitivity level and handled in accordance with established security controls that protect confidentiality, integrity, and availability.

**3.1 Information Classification Framework**

**[Company Name]** shall use a four-tier classification system to categorize all information assets:

**Public:** Information that can be freely shared with the general public without risk to **[Company Name]** or its stakeholders.
- Examples: Marketing materials, public website content, published research, press releases
- No special handling requirements beyond standard business practices

**Internal:** Information intended for use within **[Company Name]** that should not be disclosed to external parties without authorization.
- Examples: Internal policies, organizational charts, general business communications, non-sensitive system documentation
- Requires basic access controls and confidentiality agreements

**Confidential:** Sensitive information that could cause significant harm to **[Company Name]**, its customers, or business partners if disclosed without authorization.
- Examples: Financial records, strategic plans, customer lists, proprietary technology, employee personal information
- Requires enhanced security controls, encryption for transmission, and formal access approval

**Restricted:** Highly sensitive information that could cause severe harm if disclosed and is subject to regulatory protection requirements.
- Examples: ePHI, payment card data, social security numbers, authentication credentials, encryption keys
- Requires maximum security controls, encryption at rest and in transit, audit logging, and compliance with specific regulations

**3.2 Information Classification Responsibilities**

Information classification shall be assigned by designated information owners and applied consistently throughout the information lifecycle. The Security Officer shall maintain an Information Asset Inventory that documents all major information assets, their designated Information Owner, and their classification level.

- Information owners are responsible for the initial classification of data for which they are responsible, approving access requests, and ensuring data is handled according to this policy.

- Classification shall be assigned at the time of creation or acquisition and documented in the Information Asset Inventory.

- When information of different classification levels is combined, the resulting information shall be classified at the highest level of any component.

- Information owners shall review the classification of their information assets at least annually. This review shall be documented to provide an audit trail.

**3.3 Handling Requirements by Classification Level**

Specific security controls shall be implemented based on information classification levels.

**3.3.1 Public Information**
- No special access restrictions required
- Standard backup and archival procedures apply
- May be stored on standard business systems
- Can be transmitted via standard email or file sharing

**3.3.2 Internal Information**
- Access restricted to authorized **[Company Name]** workforce members
- Password-protected when stored on portable devices
- Transmitted via secure channels (encrypted email, secure file transfer)
- Stored on company-approved systems with appropriate access controls
- Covered by confidentiality agreements for third-party access

**3.3.3 Confidential Information**
- Access granted only on a need-to-know basis with formal approval
- Encrypted when stored on laptops, mobile devices, or removable media
- Transmitted only via encrypted channels (secure email, VPN, HTTPS)
- Stored on hardened systems with enhanced access controls and audit logging
- Protected by multi-factor authentication for system access
- Requires Non-Disclosure Agreements (NDAs) for third-party access
- Must be clearly labeled or marked to indicate classification level

**3.3.4 Restricted Information**
- Access granted only to specifically authorized individuals with business justification
- Encrypted at rest using **[Encryption Standard, e.g., AES-256]** or equivalent
- Encrypted in transit using **[Protocol, e.g., TLS 1.3]** or equivalent
- Stored only on systems specifically approved for Restricted data
- Protected by multi-factor authentication and privileged access controls
- All access logged and monitored for unauthorized activity
- Requires Business Associate Agreements (BAAs) for third-party handling
- Must be clearly labeled and handled according to regulatory requirements
- Subject to data loss prevention (DLP) monitoring and controls

**3.4 Electronic Protected Health Information (ePHI) Handling**

ePHI represents a subset of Restricted information requiring special handling under HIPAA regulations.

- ePHI shall be classified as Restricted and subject to all applicable controls
- Access limited to workforce members whose job functions require ePHI to perform their duties
- Minimum necessary standard applied to all ePHI access, use, and disclosure
- All ePHI access logged with user identification, date/time, and specific information accessed
- ePHI transmitted only via HIPAA-compliant secure methods
- Regular audits conducted to verify appropriate ePHI access and usage
- Breach notification procedures followed for any suspected ePHI compromise

**3.5 Data Labeling and Marking**

Information classification shall be clearly indicated through appropriate labeling mechanisms.

- Electronic documents shall include classification markings in headers, footers, or metadata
- Email communications containing Confidential or Restricted information shall include classification in subject lines
- Physical documents shall be marked with classification levels on each page
- Storage media shall be labeled with the highest classification level of contained information
- System interfaces shall display classification levels for data being accessed
- Classification labels shall remain with information throughout its lifecycle

**3.6 Information Storage and Access Controls**

Storage requirements shall be implemented based on information classification levels.

- All information systems shall maintain access control lists (ACLs) restricting access based on classification and business need
- Confidential and Restricted information shall be stored only on systems with appropriate security controls
- Cloud storage of Confidential and Restricted information requires encryption and compliance with security standards
- Regular access reviews shall be conducted quarterly for Restricted information and annually for Confidential information
- Automated tools shall be used where possible to enforce classification-based access controls

**3.7 Information Transmission and Sharing**

Information transmission methods shall align with classification requirements and recipient authorization levels.

- Public and Internal information may be transmitted via standard business communication channels
- Confidential information shall be encrypted during transmission using approved encryption methods
- Restricted information shall only be transmitted via secure, encrypted channels with confirmed recipient authorization
- File sharing services shall be approved for specific classification levels and configured with appropriate security settings
- Email systems shall include data loss prevention capabilities to prevent unauthorized transmission of sensitive information

**3.8 Information Retention and Disposal**

Information shall be retained according to business requirements and regulatory obligations, then securely disposed of when no longer needed.

- Retention schedules shall be established for each information type considering business, legal, and regulatory requirements
- ePHI shall be retained in accordance with HIPAA requirements and state regulations
- Secure disposal methods shall be used for all Confidential and Restricted information:
  - Electronic media: Cryptographic erasure, degaussing, or physical destruction
  - Physical documents: Cross-cut shredding or incineration
  - Optical media: Physical destruction
- Disposal activities shall be documented and verified for Restricted information
- Third-party disposal services shall provide certificates of destruction and maintain appropriate insurance coverage

**3.9 Data Loss Prevention (DLP)**

Technical controls shall be implemented to prevent unauthorized disclosure of sensitive information.

- DLP systems shall monitor network traffic, email, and endpoint devices for sensitive data patterns
- Automatic blocking or quarantine shall be implemented for attempted unauthorized transmission of Restricted information
- User education and warnings shall be provided when DLP systems detect potential policy violations
- DLP policies shall be regularly updated to address new data types and transmission methods
- Incident response procedures shall address DLP alerts and potential data loss events

**3.10 Mobile Device and Remote Access**

Special considerations shall apply to information access via mobile devices and remote locations.

- Mobile devices accessing Confidential or Restricted information shall be enrolled in mobile device management (MDM) systems
- Remote access to sensitive information shall require VPN connections and multi-factor authentication
- Personal devices used for business purposes shall comply with bring-your-own-device (BYOD) security requirements
- Cloud synchronization services shall be approved and configured appropriately for each classification level
- Lost or stolen devices shall be reported immediately and remotely wiped if containing sensitive information

### 4. Standards Compliance

This policy is designed to comply with and support the following industry standards and regulations.

|**Policy Section**|**Standard/Framework**|**Control Reference**|
|---|---|---|
|**All**|HIPAA Security Rule|45 CFR § 164.308(a)(4) - Information Access Management|
|**3.4**|HIPAA Security Rule|45 CFR § 164.502(b) - Minimum Necessary|
|**3.4, 3.8**|HIPAA Security Rule|45 CFR § 164.312(a)(1) - Access Control|
|**3.3.4, 3.7**|HIPAA Security Rule|45 CFR § 164.312(e)(1) - Transmission Security|
|**3.3.4, 3.6**|HIPAA Security Rule|45 CFR § 164.312(a)(2)(iv) - Encryption|
|**3.4**|HIPAA Security Rule|45 CFR § 164.312(b) - Audit Controls|
|**All**|SOC 2 Trust Services Criteria|CC6.1 - Logical Access Security|
|**3.6, 3.7**|SOC 2 Trust Services Criteria|CC6.7 - Data Transmission|
|**3.8**|SOC 2 Trust Services Criteria|CC6.5 - Data Disposal|
|**3.9**|SOC 2 Trust Services Criteria|CC7.2 - System Monitoring|
|**All**|ISO/IEC 27001:2022|A.5.12 - Classification of Information|

### 5. Definitions

**Business Associate Agreement (BAA):** A written contract between a covered entity and a business associate establishing permitted uses and disclosures of ePHI.

**Data Loss Prevention (DLP):** Technology and processes designed to detect and prevent unauthorized transmission of sensitive information.

**Electronic Protected Health Information (ePHI):** Protected health information that is created, stored, transmitted, or maintained electronically.

**Information Owner:** The person responsible for the business content and context of information, including classification and access decisions.

**Minimum Necessary:** The HIPAA principle requiring that uses and disclosures of ePHI be limited to the smallest amount necessary to accomplish the intended purpose.

**Non-Disclosure Agreement (NDA):** A legal contract establishing confidential relationships and restricting information sharing.

### 6. Responsibilities

|**Role**|**Responsibility**|
|---|---|
|**Information Owners**|Classify information assets, approve access requests, conduct periodic classification reviews, and ensure appropriate handling.|
|**Security Officer**|Develop and maintain classification policies, monitor compliance, and investigate classification violations.|
|**IT Department**|Implement technical controls for each classification level, maintain DLP systems, and provide secure storage and transmission capabilities.|
|**Data Stewards**|Ensure day-to-day compliance with classification requirements, assist with labeling, and report classification issues.|
|**Privacy Officer**|Oversee ePHI classification and handling, ensure HIPAA compliance, and manage privacy impact assessments.|
|**All Workforce Members**|Follow classification and handling requirements, properly label information, and report suspected violations or data loss.|
|**Managers/Supervisors**|Ensure their teams understand and comply with classification requirements, approve access requests within their authority.|
|**Records Management**|Maintain retention schedules, coordinate secure disposal activities, and ensure compliance with legal hold requirements.|
