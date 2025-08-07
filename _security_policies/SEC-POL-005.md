---
title: Vendor and Third-Party Risk Management Policy (SEC-POL-005)
parent: Security Policies
nav_order: 5
---
### 1. Objective

The objective of this policy is to establish comprehensive requirements for assessing, managing, and monitoring security and compliance risks associated with vendors, third-party service providers, and business associates. This policy ensures that **[Company Name]** maintains appropriate oversight of external parties who access, process, store, or transmit company information, particularly electronic Protected Health Information (ePHI), while maintaining compliance with HIPAA, HITECH, and SOC 2 requirements.

### 2. Scope

This policy applies to all **[Company Name]** workforce members involved in vendor selection, contract negotiation, or ongoing vendor management. It encompasses all external parties including vendors, service providers, consultants, contractors, business associates, and any other third parties that have access to **[Company Name]** information systems, data, or facilities. This policy covers the entire vendor lifecycle from initial assessment through contract termination and data return.

### 3. Policy

**[Company Name]** shall implement a comprehensive vendor risk management program to ensure that all third-party relationships meet security, privacy, and compliance requirements.

**3.1 Vendor Classification and Risk Assessment**

All vendors shall be classified based on their risk level and subject to appropriate due diligence and ongoing monitoring.

**3.1.1 Vendor Risk Classification**

Vendors shall be classified into risk categories based on the following factors:
- Type and sensitivity of data accessed (ePHI, Confidential, Internal, Public)
- Level of system access required (network, applications, databases, privileged access)
- Geographic location and regulatory jurisdiction
- Financial impact and business criticality
- Duration and scope of engagement

**Risk Classifications:**
- **High Risk:** Vendors with access to ePHI, Restricted data, or critical systems; cloud service providers; vendors with privileged access
- **Medium Risk:** Vendors with access to Confidential data or internal systems; vendors providing business-critical services
- **Low Risk:** Vendors with limited access to Internal data or no direct system access; vendors providing non-critical services

**3.1.2 Pre-Engagement Risk Assessment**

Prior to engaging any vendor, the designated Business Owner, in coordination with the Security Officer, shall conduct and document a formal risk assessment appropriate to the vendor's risk classification. The results of this assessment must be formally approved before contracts are executed.

**High-Risk Vendor Requirements:**
- Comprehensive security questionnaire (e.g., SIG Lite, CAIQ, or equivalent)
- Third-party security assessment report (SOC 2 Type II, ISO 27001, or equivalent)
- Financial stability assessment
- Reference checks with existing customers
- On-site security assessment for critical vendors
- Cyber insurance verification
- Background check requirements for vendor personnel

**Medium-Risk Vendor Requirements:**
- Standard security questionnaire
- Third-party assessment report or self-attestation
- Financial stability review
- Reference checks
- Insurance verification

**Low-Risk Vendor Requirements:**
- Basic security questionnaire or self-attestation
- General insurance verification

**3.2 Business Associate Agreements and Contractual Requirements**

All vendor contracts shall include appropriate security, privacy, and compliance provisions based on the vendor's risk level and data access requirements, as approved by the Legal and Security teams.

**3.2.1 Business Associate Agreements (BAAs)**

A signed BAA shall be executed before any vendor is granted access to ePHI.

BAAs shall include:
- Permitted uses and disclosures of ePHI
- Prohibition of unauthorized use or disclosure
- Safeguarding requirements equivalent to the HIPAA Security Rule
- Requirement to report any Security Incident, including any Breach of Unsecured PHI, to **[Company Name]** without unreasonable delay and in no case later than 24 hours after discovery.
- Access, amendment, and accounting of disclosures rights
- Requirement to return or destroy all ePHI upon contract termination, and to provide a certificate of destruction.
- Audit rights and compliance monitoring provisions
- Subcontractor requirements and flow-down of all BAA obligations

**3.2.2 Security Contract Provisions**

All vendor contracts shall include security provisions appropriate to the risk level:

**Mandatory Security Clauses:**
- Data protection and confidentiality requirements
- Incident notification and response procedures, including a maximum notification timeframe.
- Right to audit and conduct security assessments
- Personnel security and background check requirements
- Data location restrictions and cross-border transfer limitations
- Insurance and liability provisions
- Compliance with applicable laws and regulations
- Requirement for secure data return or destruction upon contract termination, with verification.

**Additional High-Risk Vendor Clauses:**
- Specific security control requirements (encryption, access controls, logging)
- Regular security reporting and metrics
- Breach notification timelines and procedures
- Limitation of data retention and use
- Subcontractor approval and oversight requirements
- Business continuity and disaster recovery provisions
- Right to terminate for security violations

**3.3 Vendor Security Monitoring and Ongoing Assessment**

Ongoing monitoring shall be conducted to ensure vendors maintain appropriate security posture throughout the engagement lifecycle.

**3.3.1 Continuous Monitoring Requirements**

- Annual security questionnaire updates for High and Medium-risk vendors
- Review of updated security certifications and assessment reports
- Monitoring of vendor security incidents and breach notifications
- Financial stability monitoring for critical vendors
- Performance and service level monitoring
- Compliance with contractual security requirements

**3.3.2 Periodic Assessments**

- High-Risk vendors: Annual comprehensive security assessment
- Medium-Risk vendors: Biennial security assessment
- Low-Risk vendors: Assessment upon contract renewal

**3.3.3 Vendor Security Incident Management**

- Vendors shall notify **[Company Name]** of security incidents within contractually specified timeframes
- **[Company Name]** shall assess the impact of vendor incidents on company operations and data
- Incident response coordination with vendors shall follow documented procedures
- Lessons learned from vendor incidents shall be incorporated into future risk assessments

**3.4 Vendor Access Management**

Access granted to vendors shall be controlled and monitored in accordance with the principle of least privilege.

**3.4.1 Access Provisioning**

- Vendor access requests shall be formally approved by the business owner and security team
- Access shall be limited to the minimum necessary to perform contracted services
- Vendor personnel shall be individually identified and authenticated
- Shared or generic accounts shall not be used for vendor access
- Multi-factor authentication shall be required for all High-risk vendor access

**3.4.2 Access Monitoring and Review**

- All vendor access shall be logged and monitored for inappropriate activity
- Quarterly access reviews shall be conducted for High-risk vendors
- Annual access reviews shall be conducted for Medium and Low-risk vendors
- Access shall be promptly revoked upon contract termination or personnel changes

**3.5 Vendor Onboarding and Offboarding**

Formal processes shall be established for vendor onboarding and offboarding to ensure security requirements are met.

**3.5.1 Vendor Onboarding Process**

1. Risk assessment and classification
2. Security questionnaire and documentation review
3. Contract negotiation including security provisions
4. BAA execution (if handling ePHI)
5. Security orientation and training (if required)
6. Access provisioning and testing
7. Ongoing monitoring setup

**3.5.2 Vendor Offboarding Process**

1. Access revocation and account deactivation
2. Data return or secure destruction verification
3. Equipment and credential return
4. Final security assessment and documentation
5. Contract closure and relationship termination
6. Lessons learned documentation

**3.6 Cloud Service Provider Management**

Cloud service providers shall be subject to enhanced security requirements due to the sensitivity of data and critical nature of services.

**3.6.1 Cloud Provider Requirements**

- SOC 2 Type II certification or equivalent (ISO 27001, FedRAMP)
- Compliance with relevant industry standards (HIPAA, PCI-DSS if applicable)
- Data encryption at rest and in transit
- Geographic data location controls and restrictions
- Incident response and breach notification procedures
- Business continuity and disaster recovery capabilities
- Regular penetration testing and vulnerability assessments

**3.6.2 Cloud Service Monitoring**

- Regular review of service provider security posture and certifications
- Monitoring of provider security advisories and incident notifications
- Assessment of configuration changes and security updates
- Periodic review of data access logs and administrative activities

**3.7 Subcontractor and Fourth-Party Risk Management**

Vendors shall be required to manage risks associated with their subcontractors and ensure equivalent security standards.

- Vendors shall obtain written approval before engaging subcontractors for services involving **[Company Name]** data
- Subcontractors shall be subject to the same security requirements as primary vendors
- Vendors shall maintain oversight of subcontractor security practices
- Flow-down of security requirements through the entire supply chain
- Notification requirements for subcontractor changes or incidents

### 4. Standards Compliance

This policy is designed to comply with and support the following industry standards and regulations.

|**Policy Section**|**Standard/Framework**|**Control Reference**|
|---|---|---|
|**3.2.1**|HIPAA Security Rule|45 CFR § 164.314(a)(1) - Business Associate Contracts|
|**3.2.1**|HIPAA Security Rule|45 CFR § 164.314(a)(2) - Business Associate Safeguards|
|**3.1, 3.3**|HIPAA Security Rule|45 CFR § 164.308(a)(1)(ii)(A) - Risk Assessment|
|**3.4**|HIPAA Security Rule|45 CFR § 164.308(a)(4) - Information Access Management|
|**3.3.3**|HIPAA Security Rule|45 CFR § 164.308(a)(6) - Security Incident Procedures|
|**All**|SOC 2 Trust Services Criteria|CC9.1 - Vendor Management|
|**3.1, 3.3**|SOC 2 Trust Services Criteria|CC9.2 - Vendor Risk Assessment|
|**3.2**|SOC 2 Trust Services Criteria|CC9.3 - Vendor Agreements|
|**3.6**|SOC 2 Trust Services Criteria|A1.2 - System Capacity|
|**All**|ISO/IEC 27001:2022|A.5.19 - Information security in supplier relationships|

### 5. Definitions

**Business Associate:** A person or entity that performs functions or activities on behalf of a covered entity that involve access to ePHI.

**Business Associate Agreement (BAA):** A written contract between a covered entity and a business associate required by HIPAA.

**Cloud Service Provider:** A company that offers network services, infrastructure, or business applications in the cloud.

**Due Diligence:** The investigation or exercise of care that a reasonable business or person is expected to take before entering into an agreement or contract.

**Fourth Party:** A subcontractor or service provider used by a third-party vendor.

**Service Level Agreement (SLA):** A contract between a service provider and customer that defines the level of service expected.

**Subcontractor:** An entity engaged by a business associate to perform functions or activities on behalf of the business associate.

**Vendor Risk Assessment:** The process of evaluating the potential risks associated with engaging a third-party vendor.

### 6. Responsibilities

|**Role**|**Responsibility**|
|---|---|
|**Procurement Team**|Coordinate vendor selection process, ensure security requirements are included in RFPs, and facilitate contract negotiations.|
|**Security Officer**|Develop vendor security requirements, conduct risk assessments, and monitor vendor security compliance.|
|**Privacy Officer**|Ensure BAA requirements are met, oversee ePHI handling by vendors, and manage privacy impact assessments.|
|**Legal/Contracts Team**|Negotiate security contract provisions, ensure legal compliance, and manage contract lifecycle.|
|**Business Owners**|Define business requirements, approve vendor selections, and monitor service delivery performance.|
|**IT Department**|Implement technical controls for vendor access, monitor vendor system activity, and manage vendor integrations.|
|**Risk Management Team**|Assess vendor-related risks, maintain vendor risk register, and coordinate risk treatment activities.|
|**Finance Team**|Assess vendor financial stability, manage vendor insurance requirements, and oversee payment processes.|
|**All Workforce Members**|Report vendor security concerns, comply with vendor interaction policies, and protect company information shared with vendors.|
