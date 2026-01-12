---
title: Vendor and Third-Party Risk Management Policy (SEC-POL-005)
parent: Security Policies
nav_order: 5
---
### 1. Objective

The objective of this policy is to establish practical, risk-based requirements for managing security risks associated with vendors and third-party service providers, with focus on regulatory compliance for electronic Protected Health Information (ePHI) while maintaining operational efficiency.

### 2. Scope

This policy applies to all **[Company Name]** workforce members involved in vendor selection and management. It covers external parties that access company data or systems, with streamlined procedures based on actual risk levels rather than comprehensive assessment requirements for all vendors.

### 3. Policy

- **[Company Name]** shall implement a streamlined, risk-based vendor management approach that focuses resources on high-risk vendors while maintaining regulatory compliance through practical assessment and monitoring procedures.

#### 3.1 Simplified Vendor Risk Tiers

Vendors shall be classified into three practical risk tiers with appropriate assessment requirements for each tier.

##### 3.1.1 Risk-Based Vendor Classification

- **Tier 1 - Critical Risk (ePHI and Core Infrastructure):**
    - Cloud service providers (AWS, Azure, GCP)
    - Vendors with direct ePHI access (healthcare APIs, patient communication tools)
    - Core infrastructure providers (identity management, security tools)
    - Development and deployment platform providers

- **Tier 2 - Business Risk (Internal Data and Business-Critical Services):**
    - Business applications with internal data access (CRM, HR systems, financial tools) shall be included in this risk tier.
    - Communication and collaboration platforms (Slack, email providers) shall be classified as business risk tier.
    - Backup and disaster recovery services shall be evaluated under business risk assessment requirements.
    - Legal and professional services with confidential data access shall be subject to business risk tier controls.

- **Tier 3 - Standard Risk (Limited Access and Commodity Services):**
    - Marketing and analytics tools with minimal data access shall be included in the standard risk tier.
    - Development tools and services without production data shall be classified as standard risk.
    - Office productivity tools and subscriptions shall be subject to standard risk assessment requirements.
    - Professional services without data access shall be evaluated under standard risk tier controls.

##### 3.1.2 Streamlined Assessment Requirements

- **Tier 1 - Critical Risk Assessment:**
- **Security Certification**: SOC 2 Type II, ISO 27001, or equivalent certification required
- **Business Associate Agreement**: Required for any ePHI access
- **Financial Stability**: Basic financial stability verification
- **Security Contact**: Established security contact and incident notification procedures
- **Insurance**: Cyber liability insurance verification ($**[Amount, e.g., 5-10 million]** minimum)

- **Tier 2 - Business Risk Assessment:**
- **Basic Security Review**: Security questionnaire or self-attestation shall be conducted to assess basic security posture.
- **Contract Terms**: Standard security clauses shall be included in service agreement to establish security expectations.
- **Data Protection**: Basic data protection and incident notification requirements shall be documented in contractual terms.
- **Insurance**: General liability and professional insurance verification shall be performed to ensure adequate coverage.

- **Tier 3 - Standard Risk Assessment:**
- **Service Agreement**: Standard terms of service with basic security provisions shall be reviewed and accepted.
- **Privacy Policy**: Review of vendor privacy policy and data handling practices shall be conducted to ensure alignment with organizational requirements.
- **Minimal Due Diligence**: Basic vendor legitimacy and reputation verification shall be performed through public sources and references.

#### 3.2 Automated Vendor Risk Assessment

Leverage automated tools and vendor risk assessment platforms to streamline the evaluation process.

##### 3.2.1 Third-Party Risk Assessment Platforms

- **Vendor Risk Management Tools**: Platforms like SecurityScorecard, BitSight, or UpGuard shall be used for automated vendor security ratings.
- **Questionnaire Automation**: Shared security questionnaire databases and automated assessment tools shall be leveraged to streamline evaluation processes.
- **Continuous Monitoring**: Automated monitoring of vendor security posture and incident notifications shall be implemented for ongoing risk visibility.
- **Compliance Databases**: Compliance databases shall be used to verify vendor certifications and attestations.

##### 3.2.2 Cloud Provider Security Posture

- **Shared Responsibility Model**: Cloud provider vs. customer security responsibilities shall be understood and documented.
- **Compliance Center**: Regular review of cloud provider compliance center documentation and certifications shall be conducted.
- **Service Health**: Cloud provider service health dashboards and security advisories shall be monitored continuously.
- **Configuration Reviews**: Quarterly review of cloud service security configurations and settings shall be performed.

#### 3.3 Business Associate Agreements and Practical Contract Terms

Focus contract negotiations on essential security requirements rather than comprehensive security clauses for all vendors.

##### 3.3.1 ePHI Business Associate Agreements

For Tier 1 vendors with ePHI access:
- **Standard BAA Template**: Use standardized BAA template covering HIPAA requirements
- **Incident Notification**: **[Timeframe, e.g., 24-hour]** incident notification requirement
- **Data Return**: Secure data return or destruction upon contract termination
- **Audit Rights**: Right to review security practices and compliance evidence
- **Subcontractor Requirements**: Flow-down of BAA requirements to subcontractors

##### 3.3.2 Standard Security Contract Provisions

For Tier 2 vendors:
- **Data Protection**: Basic data protection and confidentiality requirements
- **Incident Notification**: **[Timeframe, e.g., 72-hour]** security incident notification
- **Insurance**: Professional liability and cyber insurance requirements
- **Data Location**: Geographic data storage and processing restrictions
- **Termination**: Data return requirements upon contract termination

##### 3.3.3 Commodity Service Agreements

For Tier 3 vendors:
- **Terms of Service**: Accept standard vendor terms of service with privacy policy review
- **Data Minimization**: Limit data shared to necessary business purposes only
- **Account Security**: Require multi-factor authentication and strong password policies
- **Access Controls**: Implement role-based access controls within vendor systems

#### 3.4 Ongoing Vendor Monitoring

Implement practical, automated monitoring focused on high-risk vendors while maintaining awareness of vendor security posture.

##### 3.4.1 Tier 1 Vendor Monitoring

- **Annual Certification Review**: Review updated SOC 2 reports and security certifications
- **Security Scorecard Monitoring**: Continuous monitoring through vendor risk assessment platforms
- **Incident Notifications**: Active monitoring of vendor security incidents and advisories
- **Contract Performance**: Annual review of contract compliance and service performance
- **Access Review**: Quarterly review of vendor access and permissions

##### 3.4.2 Tier 2 and 3 Vendor Monitoring

- **Contract Renewal Review**: Security assessment during contract renewal cycle
- **Incident Awareness**: Monitor for significant security incidents affecting vendor services
- **Access Management**: Annual review of vendor access and account permissions
- **Cost and Performance**: Monitor vendor performance and cost optimization opportunities

#### 3.5 Vendor Access Management

Implement practical access controls that balance security with operational efficiency.

##### 3.5.1 Access Provisioning

- **Business Justification**: Clear business justification required for vendor access requests
- **Least Privilege**: Limit vendor access to minimum necessary for contracted services
- **Time-Limited Access**: Implement time-limited access for temporary or project-based vendors
- **Multi-Factor Authentication**: Require MFA for all vendor access to critical systems
- **Single Sign-On**: Use SSO integration where available to centralize access management

##### 3.5.2 Access Monitoring and Review

- **Automated Logging**: Log vendor access activities through existing security monitoring tools
- **Regular Access Review**: **[Frequency, e.g., Quarterly]** review of active vendor accounts and permissions
- **Prompt Deprovisioning**: Immediate access revocation upon contract termination or project completion
- **Exception Reporting**: Automated alerts for unusual vendor access patterns or failed authentication attempts

#### 3.6 Cloud-Native Vendor Security

Leverage cloud provider security capabilities to monitor and control vendor access to cloud resources.

##### 3.6.1 Cloud Provider Selection

- **Major Cloud Providers**: Prefer major cloud providers (AWS, Azure, GCP) with comprehensive compliance certifications
- **Shared Responsibility**: Clearly understand and document shared responsibility model
- **Security Center**: Use cloud provider security centers for continuous compliance monitoring
- **Cost Optimization**: Balance security requirements with cost-effective service selection

##### 3.6.2 Cloud Service Monitoring

- **Service Health Monitoring**: Monitor cloud provider service health and security advisory notifications
- **Configuration Management**: Use cloud-native tools to monitor and enforce security configurations
- **Access Analytics**: Leverage cloud provider access analytics and unusual activity detection
- **Compliance Dashboards**: Use cloud provider compliance dashboards for ongoing attestation evidence

#### 3.7 Incident Response and Vendor Coordination

Establish practical procedures for coordinating security incidents involving vendor services.

##### 3.7.1 Vendor Incident Notification

- **Notification Procedures**: Clear procedures for vendors to report security incidents affecting **[Company Name]** data
- **Response Coordination**: Designated Security Officer as primary contact for vendor incident coordination
- **Impact Assessment**: Rapid assessment of vendor incident impact on company operations and data
- **Communication**: Internal communication procedures for vendor-related security incidents

##### 3.7.2 Vendor Support During Incidents

- **Technical Coordination**: Coordinate with vendors during security incidents affecting their services
- **Evidence Collection**: Coordinate evidence collection and forensic activities with vendor support
- **Recovery Planning**: Coordinate service recovery and business continuity with vendor teams
- **Lessons Learned**: Document lessons learned from vendor incidents for future risk assessment

### 4. Standards Compliance

This policy is designed to comply with and support the following industry standards and regulations.

| **Policy Section** | **Standard/Framework** | **Control Reference** |
| ------------------ | ---------------------- | --------------------- |
| **3.1, 3.4** | HITRUST CSF v11.2.0 | 14.a - Third Party Assurance Policy |
| **3.1, 3.4** | HITRUST CSF v11.2.0 | 14.b - Third Party Risk Assessment |
| **3.3** | HITRUST CSF v11.2.0 | 14.c - Third Party Service Agreements |
| **3.5** | HITRUST CSF v11.2.0 | 14.d - Third Party Access Management |
| **3.4** | HITRUST CSF v11.2.0 | 14.e - Third Party Monitoring |
| **3.3.1** | HIPAA Security Rule | 45 CFR § 164.314(a)(1) - Business Associate Contracts |
| **3.3.1** | HIPAA Security Rule | 45 CFR § 164.314(a)(2) - Business Associate Safeguards |
| **3.1** | HIPAA Security Rule | 45 CFR § 164.308(a)(1)(ii)(A) - Risk Assessment |
| **3.5** | HIPAA Security Rule | 45 CFR § 164.308(a)(4) - Information Access Management |
| **3.7** | HIPAA Security Rule | 45 CFR § 164.308(a)(6) - Security Incident Procedures |
| **All** | SOC 2 Trust Services Criteria | CC9.1 - Vendor Management |
| **3.1, 3.4** | SOC 2 Trust Services Criteria | CC9.2 - Vendor Risk Assessment |
| **3.3** | SOC 2 Trust Services Criteria | CC9.3 - Vendor Agreements |

### 5. Definitions

- **Business Associate Agreement (BAA):** A written contract between a covered entity and a business associate required by HIPAA for any ePHI access.

- **Cloud Service Provider:** A company that offers network services, infrastructure, or business applications in the cloud (e.g., AWS, Azure, GCP).

- **Risk Tier:** Classification system for vendors based on data access and business criticality (Tier 1-Critical, Tier 2-Business, Tier 3-Standard).

- **Security Scorecard:** Automated security rating system that continuously monitors vendor security posture using external security indicators.

- **Single Sign-On (SSO):** Authentication system that allows users to access multiple vendor systems with one set of credentials.

- **Vendor Risk Assessment:** Streamlined evaluation process appropriate to vendor risk tier and data access requirements.

### 6. Responsibilities

|**Role**|**Responsibility**|
|---|---|
|**Security Officer**|Classify vendors into appropriate risk tiers, manage relationships with critical risk vendors, ensure BAA execution for ePHI access vendors, and serve as primary contact for vendor security incidents.|
|**Business Owners**|Select appropriate vendors based on business requirements, provide business justification for vendor engagement, monitor vendor service delivery, and manage vendor costs within approved budgets.|
|**IT Operations Team**|Implement technical integrations with vendor systems, provision and manage vendor access through SSO systems, configure vendor systems according to security requirements, and provide technical support during vendor incidents.|
|**Legal/Contracts Team**|Negotiate contract terms and security provisions, execute Business Associate Agreements, review vendor contracts for compliance issues, and manage contract termination procedures.|
|**Finance Team**|Conduct financial stability assessments for Tier 1 vendors, verify vendor insurance coverage, monitor vendor costs and optimization opportunities, and include vendor management costs in budget planning.|
|**Development Team**|Implement secure API integrations with vendor services, ensure data minimization in vendor integrations, implement application-level security controls, and document vendor integrations and security implementations.|
