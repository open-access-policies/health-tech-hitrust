---
title: Physical Security Policy (SEC-POL-006)
parent: Security Policies
nav_order: 6
---
### 1. Objective

The objective of this policy is to establish comprehensive physical security requirements for **[Company Name]**'s facilities, equipment, and workforce in a cloud-first environment. This policy ensures that appropriate physical safeguards are implemented to protect against unauthorized access to facilities, equipment theft, environmental hazards, and physical threats while maintaining the confidentiality, integrity, and availability of information assets and electronic Protected Health Information (ePHI) in compliance with HIPAA, HITECH, and SOC 2 requirements. Given **[Company Name]**'s cloud-based infrastructure, this policy focuses on corporate facilities, endpoint devices, and the oversight of cloud provider physical security controls.

### 2. Scope

This policy applies to all **[Company Name]** workforce members, contractors, visitors, and third parties who access company facilities or handle company equipment. It encompasses all physical locations including corporate offices, remote work environments, temporary workspaces, and any location where company information is accessed or processed. This policy covers all physical assets including workstations, laptops, mobile devices, printed materials, storage media, networking equipment, and any other tangible assets containing or providing access to company information. While **[Company Name]** operates with cloud-based infrastructure, this policy also addresses the oversight and validation of cloud provider physical security controls.

### 3. Policy

- **[Company Name]** shall implement layered physical security controls appropriate to the cloud-based operating model while ensuring comprehensive protection of all physical assets and facilities.

#### 3.1 Facility Security and Access Control

Physical access to all **[Company Name]** facilities shall be controlled and monitored to prevent unauthorized entry and protect information assets.

##### 3.1.1 Office Facility Security

- **Access Control Systems:**
- Electronic badge access systems shall be implemented for all corporate facilities
- Multi-factor authentication required for access to areas containing sensitive information
- Visitor management system with registration, identification verification, and escort requirements
- Access permissions based on role and business need with quarterly access reviews
- Emergency access procedures and override capabilities for authorized personnel

- **Physical Security Zones:**
- **Public Areas:** Reception, common areas - basic access controls and monitoring
- **General Office:** Standard work areas - badge access required, visitor escort beyond this point
- **Restricted Areas:** IT equipment rooms, executive offices, records storage - enhanced access controls
- **Highly Restricted:** Server rooms, telecommunications closets - maximum security controls with biometric access

- **Facility Monitoring:**
- CCTV surveillance systems covering all entry/exit points and sensitive areas
- Motion detection systems for after-hours monitoring
- 24/7 monitoring service or security personnel for critical facilities
- Video retention for minimum **[Duration, e.g., 90 days]** with secure storage
- Integration with local law enforcement and emergency services

##### 3.1.2 Remote Work Environment Security

- **Home Office Security Requirements:**
- Dedicated workspace with physical security measures to prevent unauthorized access
- Locking mechanisms for desks, filing cabinets, and storage areas containing company information
- Privacy screens or positioning to prevent visual access to company information
- Secure storage for company equipment when not in use
- Environmental protections against theft, damage, and unauthorized access

- **Co-working and Public Space Restrictions:**
- Prohibition of accessing ePHI or Restricted information in public spaces
- Privacy screens required when working on Confidential information in shared spaces
- Secure Wi-Fi requirements and VPN usage for all company system access
- Physical security of devices and materials in temporary work environments
- Clean desk practices and secure storage of sensitive materials

#### 3.2 Equipment and Asset Protection

All company equipment and physical assets shall be protected against theft, damage, and unauthorized access throughout their lifecycle.

##### 3.2.1 Endpoint Device Security

- **Physical Device Protection:**
- Cable locks or security devices required for desktop computers in office environments
- Laptop encryption and remote wipe capabilities for all mobile devices
- Asset tagging and inventory tracking for all company equipment
- Secure storage requirements for devices containing sensitive information
- Insurance coverage for high-value equipment and mobile devices

- **Device Lifecycle Management:**
- Secure provisioning process with pre-configured security settings
- Regular physical inventory audits (quarterly for mobile devices, annually for fixed assets)
- Maintenance and repair procedures that protect data confidentiality
- Secure decommissioning with verified data destruction
- Return procedures for workforce member separation or equipment refresh

##### 3.2.2 Removable Media and Storage Security

- **Media Handling Requirements:**
- Encrypted storage required for all removable media containing company information
- Locked storage for backup media, USB drives, and optical media
- Chain of custody procedures for media transportation
- Inventory management system for tracking media location and usage
- Environmental protection for media storage (temperature, humidity, magnetic fields)

- **Secure Disposal Procedures:**
- Physical destruction required for all media containing ePHI or Restricted information
- Certified disposal vendors with appropriate security clearances and insurance
- Witnessed destruction for high-sensitivity media with certificates of completion
- Degaussing or physical destruction for magnetic media
- Secure overwriting followed by physical destruction for solid-state media

#### 3.3 Cloud Provider Physical Security Oversight

- **[Company Name]** shall validate and monitor the physical security controls implemented by cloud service providers to ensure appropriate protection of company data and systems. This oversight is the responsibility of the designated Cloud Security Team or Security Officer.

##### 3.3.1 Cloud Provider Assessment

- **Physical Security Requirements:**
- SOC 2 Type II certification or equivalent demonstrating physical security controls
- Multi-factor authentication and biometric access controls for data center facilities
- 24/7 physical security monitoring and surveillance systems
- Environmental controls including fire suppression, climate control, and power management
- Geographic separation of data centers for disaster recovery and business continuity

- **Compliance Validation:**
- The Cloud Security Team shall conduct and document an annual review of all critical cloud providers' security certifications (e.g., SOC 2 Type II, ISO 27001) and audit reports.
- Validation of physical security controls through review of third-party assessments.
- Contractual agreements must include requirements for physical security standards and incident notification within a defined timeframe.
- Right-to-audit clauses shall be included in contracts for critical cloud services where feasible.
- Geographic data location controls shall be configured to align with legal and regulatory requirements.

##### 3.3.2 Cloud Security Monitoring

- **Ongoing Oversight:**
- The Cloud Security Team shall conduct and document a quarterly review of cloud provider security incident reports and notifications.
- Continuous monitoring of cloud provider security advisories and documentation for significant control changes.
- An annual assessment of cloud provider business continuity and disaster recovery test results shall be conducted and documented.
- The Cloud Security Team shall validate that data center certifications and compliance status remain active and in good standing.
- Coordination with cloud providers for security investigations and incident response shall be managed by the Security Officer and Incident Response Team.

#### 3.4 Physical Document and Information Security

Physical documents and printed materials containing sensitive information shall be protected throughout their lifecycle.

##### 3.4.1 Document Handling Requirements

- **Secure Document Management:**
- Classification and marking of all physical documents based on sensitivity levels
- Locked storage for documents containing Confidential or Restricted information
- Clean desk policy requiring secure storage of sensitive documents when unattended
- Controlled access to document storage areas with access logging
- Regular inventory and review of stored documents

- **Document Transportation:**
- Secure transportation methods for sensitive documents between facilities
- Chain of custody documentation for document transfers
- Encrypted digital alternatives preferred over physical document transportation
- Approval requirements for removing sensitive documents from secure facilities
- Insurance coverage for valuable or sensitive document shipments

##### 3.4.2 Printing and Output Security

- **Secure Printing Controls:**
- Follow-me printing or secure print release for sensitive documents
- Physical presence required at printer for document retrieval
- Automatic deletion of print jobs after specified time periods
- Monitoring and logging of all print activities for sensitive information
- Secure disposal of misprints and unwanted printouts

- **Print Environment Security:**
- Printers located in secure areas with appropriate access controls
- Network printing security with authentication and encryption
- Regular maintenance and service with data protection requirements
- Secure disposal of printer components containing data (hard drives, memory)
- Vendor agreements for secure printer maintenance and support

#### 3.5 Environmental and Infrastructure Security

Environmental controls and infrastructure security measures shall protect against natural disasters, power failures, and other environmental threats.

##### 3.5.1 Environmental Controls

- **Climate and Power Management:**
- Uninterruptible Power Supply (UPS) systems for critical equipment and systems
- Surge protection and power conditioning for all electronic equipment
- Emergency lighting and communication systems for facility emergencies
- Temperature and humidity monitoring for equipment areas
- Backup power systems for extended outages

- **Fire and Safety Protection:**
- Fire detection and suppression systems appropriate for electronic equipment
- Emergency evacuation procedures and regular drills
- First aid and emergency response equipment and training
- Safety equipment and procedures for equipment maintenance
- Integration with local emergency services and authorities

##### 3.5.2 Physical Infrastructure Security

- **Building and Perimeter Security:**
- Secure building construction with reinforced entry points
- Perimeter fencing and lighting for standalone facilities
- Vehicle access controls and parking security measures
- Landscape design that supports security monitoring and access control
- Regular security assessments and penetration testing of physical controls

- **Utility and Service Protection:**
- Secure access to utility rooms and service areas
- Protection of telecommunications and network infrastructure
- Backup communication systems for emergency situations
- Service provider security requirements and background checks
- Regular inspection and maintenance of physical infrastructure

#### 3.6 Workplace Security and Safety

Comprehensive workplace security measures shall protect workforce members and maintain a secure working environment.

##### 3.6.1 Personnel Security

- **Workplace Safety:**
- Background check requirements for personnel with physical access to sensitive areas
- Security awareness training including physical security procedures
- Identification badge requirements for all workforce members and visitors
- Reporting procedures for suspicious activities and security incidents
- Security escort requirements for unauthorized individuals

- **Emergency Procedures:**
- Emergency contact information and notification procedures
- Evacuation plans and assembly points for different emergency scenarios
- Emergency communication systems and backup procedures
- Business continuity procedures for facility unavailability
- Coordination with law enforcement and emergency services

##### 3.6.2 Visitor and Contractor Management

- **Visitor Control Procedures:**
- Advance registration and approval for all visitors
- Photo identification verification and temporary badge issuance
- Continuous escort requirements for visitors in sensitive areas
- Visitor activity logging and monitoring
- Background check requirements for contractors with extended facility access

- **Contractor Security Requirements:**
- Security agreements and confidentiality requirements for all contractors
- Equipment and tool inspection procedures for maintenance personnel
- Supervised access for contractors working on sensitive systems
- Verification of contractor personnel authorization and identification
- Secure disposal of any materials generated during contractor activities

### 4. Standards Compliance

This policy is designed to comply with and support the following industry standards and regulations.

|**Policy Section**|**Standard/Framework**|**Control Reference**|
|---|---|---|
|**All**|HITRUST CSF v11.2.0|18.a - Physical and Environmental Security Policy|
|**3.1**|HITRUST CSF v11.2.0|18.b - Physical Access Controls|
|**3.2**|HITRUST CSF v11.2.0|18.c - Workstation Security|
|**3.3**|HITRUST CSF v11.2.0|18.d - Equipment Protection|
|**3.4**|HITRUST CSF v11.2.0|18.e - Secure Disposal|
|**3.5**|HITRUST CSF v11.2.0|18.f - Environmental Controls|
|**3.6**|HITRUST CSF v11.2.0|18.g - Facility Security|
|**All**|HIPAA Security Rule|45 CFR § 164.310(a)(1) - Facility Access Controls|
|**3.1**|HIPAA Security Rule|45 CFR § 164.310(a)(2)(i) - Authorized Access Procedures|
|**3.2**|HIPAA Security Rule|45 CFR § 164.310(b) - Workstation Use|
|**3.2, 3.4**|HIPAA Security Rule|45 CFR § 164.310(d)(1) - Device and Media Controls|
|**3.2.2**|HIPAA Security Rule|45 CFR § 164.310(d)(2)(i) - Media Disposal|
|**All**|SOC 2 Trust Services Criteria|CC6.4 - Physical Access Controls|
|**3.5**|SOC 2 Trust Services Criteria|A1.1 - System Availability|
|**3.3**|SOC 2 Trust Services Criteria|CC9.1 - Vendor Management|

### 5. Definitions

- **Clean Desk Policy:** Security practice requiring sensitive materials to be secured when workspaces are unattended.

- **Cloud Service Provider:** Third-party organization providing cloud computing services including infrastructure, platforms, or software.

- **Environmental Controls:** Systems and procedures designed to protect against environmental hazards such as fire, flood, temperature extremes, and power failures.

- **Follow-Me Printing:** Secure printing system requiring user authentication at the printer before documents are released.

- **Multi-Factor Authentication:** Security process requiring two or more authentication factors for access verification.

- **Physical Security Perimeter:** Physical boundary around facilities, systems, or areas requiring protection.

- **Tailgating:** Unauthorized access gained by following an authorized person through a controlled access point.

- **Visitor Management System:** Automated system for registering, tracking, and managing facility visitors.

### 6. Responsibilities

|**Role**|**Responsibility**|
|---|---|
|**Security Officer**|Develop physical security policies, oversee security system implementation, coordinate with facilities management, and ensure compliance with security standards.|
|**Facilities Management**|Maintain physical security systems, manage environmental controls, coordinate building security, and ensure compliance with safety regulations.|
|**IT Security Team**|Secure IT equipment and infrastructure, coordinate physical and logical security measures, and monitor security events.|
|**Human Resources**|Manage badge access provisioning, conduct background checks, coordinate visitor management, and integrate security into HR processes.|
|**Reception/Administrative Staff**|Manage visitor registration and badging, monitor lobby areas, enforce visitor policies, and coordinate with security team.|
|**Cloud Security Team**|Assess cloud provider physical security controls, monitor cloud security compliance, and coordinate cloud security requirements.|
|**All Workforce Members**|Comply with physical security policies, secure workspaces and equipment, challenge unauthorized individuals, and report security incidents.|
|**Managers/Supervisors**|Ensure team compliance with physical security policies, approve visitor access, support emergency procedures, and manage physical asset inventory.|
|**Remote Workers**|Implement home office security measures, protect company equipment, follow secure work practices, and report security concerns.|
