---
title: Vendor and Third-Party Risk Management Policy (SEC-POL-005)
parent: Security Policies
nav_order: 5
---
### 1. Objective

The objective of this policy is to establish practical, risk-based requirements for managing security risks associated with vendors and third-party service providers, with focus on regulatory compliance for electronic Protected Health Information (ePHI) while maintaining operational efficiency appropriate for a **[Number, e.g., 120]**-person organization.

### 2. Scope

This policy applies to all **[Company Name]** workforce members involved in vendor selection and management. It covers external parties that access company data or systems, with streamlined procedures based on actual risk levels rather than comprehensive assessment requirements for all vendors.

### 3. Policy

**[Company Name]** shall implement a streamlined, risk-based vendor management approach that focuses resources on high-risk vendors while maintaining regulatory compliance through practical assessment and monitoring procedures.

**3.1 Simplified Vendor Risk Tiers**

Vendors shall be classified into three practical risk tiers with appropriate assessment requirements for each tier.

**3.1.1 Risk-Based Vendor Classification**

**Tier 1 - Critical Risk (ePHI and Core Infrastructure):**
- Cloud service providers (AWS, Azure, GCP)
- Vendors with direct ePHI access (healthcare APIs, patient communication tools)
- Core infrastructure providers (identity management, security tools)
- Development and deployment platform providers

**Tier 2 - Business Risk (Internal Data and Business-Critical Services):**
- Business applications with internal data access (CRM, HR systems, financial tools)
- Communication and collaboration platforms (Slack, email providers)
- Backup and disaster recovery services
- Legal and professional services with confidential data access

**Tier 3 - Standard Risk (Limited Access and Commodity Services):**
- Marketing and analytics tools with minimal data access
- Development tools and services without production data
- Office productivity tools and subscriptions
- Professional services without data access

**3.1.2 Streamlined Assessment Requirements**

**Tier 1 - Critical Risk Assessment:**
- **Security Certification**: SOC 2 Type II, ISO 27001, or equivalent certification required
- **Business Associate Agreement**: Required for any ePHI access
- **Financial Stability**: Basic financial stability verification
- **Security Contact**: Established security contact and incident notification procedures
- **Insurance**: Cyber liability insurance verification ($**[Amount, e.g., 5-10 million]** minimum)

**Tier 2 - Business Risk Assessment:**
- **Basic Security Review**: Security questionnaire or self-attestation
- **Contract Terms**: Standard security clauses in service agreement
- **Data Protection**: Basic data protection and incident notification requirements
- **Insurance**: General liability and professional insurance verification

**Tier 3 - Standard Risk Assessment:**
- **Service Agreement**: Standard terms of service with basic security provisions
- **Privacy Policy**: Review of vendor privacy policy and data handling practices
- **Minimal Due Diligence**: Basic vendor legitimacy and reputation verification

**3.2 Automated Vendor Risk Assessment**

Leverage automated tools and vendor risk assessment platforms to streamline the evaluation process.

**3.2.1 Third-Party Risk Assessment Platforms**

- **Vendor Risk Management Tools**: Use platforms like SecurityScorecard, BitSight, or UpGuard for automated vendor security ratings
- **Questionnaire Automation**: Leverage shared security questionnaire databases and automated assessment tools
- **Continuous Monitoring**: Automated monitoring of vendor security posture and incident notifications
- **Compliance Databases**: Use compliance databases to verify vendor certifications and attestations

**3.2.2 Cloud Provider Security Posture**

- **Shared Responsibility Model**: Understand and document cloud provider vs. customer security responsibilities
- **Compliance Center**: Regular review of cloud provider compliance center documentation and certifications
- **Service Health**: Monitor cloud provider service health dashboards and security advisories
- **Configuration Reviews**: Quarterly review of cloud service security configurations and settings

**3.3 Business Associate Agreements and Practical Contract Terms**

Focus contract negotiations on essential security requirements rather than comprehensive security clauses for all vendors.

**3.3.1 ePHI Business Associate Agreements**

For Tier 1 vendors with ePHI access:
- **Standard BAA Template**: Use standardized BAA template covering HIPAA requirements
- **Incident Notification**: **[Timeframe, e.g., 24-hour]** incident notification requirement
- **Data Return**: Secure data return or destruction upon contract termination
- **Audit Rights**: Right to review security practices and compliance evidence
- **Subcontractor Requirements**: Flow-down of BAA requirements to subcontractors

**3.3.2 Standard Security Contract Provisions**

For Tier 2 vendors:
- **Data Protection**: Basic data protection and confidentiality requirements
- **Incident Notification**: **[Timeframe, e.g., 72-hour]** security incident notification
- **Insurance**: Professional liability and cyber insurance requirements
- **Data Location**: Geographic data storage and processing restrictions
- **Termination**: Data return requirements upon contract termination

**3.3.3 Commodity Service Agreements**

For Tier 3 vendors:
- **Terms of Service**: Accept standard vendor terms of service with privacy policy review
- **Data Minimization**: Limit data shared to necessary business purposes only
- **Account Security**: Require multi-factor authentication and strong password policies
- **Access Controls**: Implement role-based access controls within vendor systems

**3.4 Ongoing Vendor Monitoring**

Implement practical, automated monitoring focused on high-risk vendors while maintaining awareness of vendor security posture.

**3.4.1 Tier 1 Vendor Monitoring**

- **Annual Certification Review**: Review updated SOC 2 reports and security certifications
- **Security Scorecard Monitoring**: Continuous monitoring through vendor risk assessment platforms
- **Incident Notifications**: Active monitoring of vendor security incidents and advisories
- **Contract Performance**: Annual review of contract compliance and service performance
- **Access Review**: Quarterly review of vendor access and permissions

**3.4.2 Tier 2 and 3 Vendor Monitoring**

- **Contract Renewal Review**: Security assessment during contract renewal cycle
- **Incident Awareness**: Monitor for significant security incidents affecting vendor services
- **Access Management**: Annual review of vendor access and account permissions
- **Cost and Performance**: Monitor vendor performance and cost optimization opportunities

**3.5 Vendor Access Management**

Implement practical access controls that balance security with operational efficiency.

**3.5.1 Access Provisioning**

- **Business Justification**: Clear business justification required for vendor access requests
- **Least Privilege**: Limit vendor access to minimum necessary for contracted services
- **Time-Limited Access**: Implement time-limited access for temporary or project-based vendors
- **Multi-Factor Authentication**: Require MFA for all vendor access to critical systems
- **Single Sign-On**: Use SSO integration where available to centralize access management

**3.5.2 Access Monitoring and Review**

- **Automated Logging**: Log vendor access activities through existing security monitoring tools
- **Regular Access Review**: **[Frequency, e.g., Quarterly]** review of active vendor accounts and permissions
- **Prompt Deprovisioning**: Immediate access revocation upon contract termination or project completion
- **Exception Reporting**: Automated alerts for unusual vendor access patterns or failed authentication attempts

**3.6 Cloud-Native Vendor Security**

Leverage cloud provider security capabilities to monitor and control vendor access to cloud resources.

**3.6.1 Cloud Provider Selection**

- **Major Cloud Providers**: Prefer major cloud providers (AWS, Azure, GCP) with comprehensive compliance certifications
- **Shared Responsibility**: Clearly understand and document shared responsibility model
- **Security Center**: Use cloud provider security centers for continuous compliance monitoring
- **Cost Optimization**: Balance security requirements with cost-effective service selection

**3.6.2 Cloud Service Monitoring**

- **Service Health Monitoring**: Monitor cloud provider service health and security advisory notifications
- **Configuration Management**: Use cloud-native tools to monitor and enforce security configurations
- **Access Analytics**: Leverage cloud provider access analytics and unusual activity detection
- **Compliance Dashboards**: Use cloud provider compliance dashboards for ongoing attestation evidence

**3.7 Incident Response and Vendor Coordination**

Establish practical procedures for coordinating security incidents involving vendor services.

**3.7.1 Vendor Incident Notification**

- **Notification Procedures**: Clear procedures for vendors to report security incidents affecting **[Company Name]** data
- **Response Coordination**: Designated Security Officer as primary contact for vendor incident coordination
- **Impact Assessment**: Rapid assessment of vendor incident impact on company operations and data
- **Communication**: Internal communication procedures for vendor-related security incidents

**3.7.2 Vendor Support During Incidents**

- **Technical Coordination**: Coordinate with vendors during security incidents affecting their services
- **Evidence Collection**: Coordinate evidence collection and forensic activities with vendor support
- **Recovery Planning**: Coordinate service recovery and business continuity with vendor teams
- **Lessons Learned**: Document lessons learned from vendor incidents for future risk assessment

### 4. Responsibilities

**4.1 Security Officer**

- **Vendor Risk Classification**: Classify vendors into appropriate risk tiers and approve assessment requirements
- **Tier 1 Vendor Oversight**: Manage relationships with critical risk vendors including cloud providers and ePHI processors
- **BAA Management**: Ensure Business Associate Agreements are executed for all ePHI access vendors
- **Incident Coordination**: Serve as primary contact for vendor security incidents and coordinate internal response
- **Automated Monitoring**: Implement and monitor automated vendor risk assessment tools and platforms

**4.2 Business Owners**

- **Vendor Selection**: Select appropriate vendors based on business requirements and approved risk tiers
- **Business Justification**: Provide clear business justification for vendor engagement and data access requirements
- **Contract Performance**: Monitor vendor service delivery and performance against business requirements
- **Access Management**: Approve and manage vendor access requirements for their business areas
- **Budget Management**: Manage vendor costs and contract terms within approved budgets

**4.3 IT Operations Team**

- **Technical Integration**: Implement technical integrations with vendor systems and services
- **Access Provisioning**: Provision and manage vendor access through SSO and identity management systems
- **Security Configuration**: Configure vendor systems according to security requirements and best practices
- **Access Monitoring**: Monitor vendor access activities through existing security monitoring tools
- **Incident Support**: Provide technical support during vendor-related security incidents

**4.4 Legal/Contracts Team**

- **Contract Negotiation**: Negotiate contract terms and security provisions with vendors
- **BAA Execution**: Execute Business Associate Agreements and ensure HIPAA compliance terms
- **Risk Review**: Review vendor contracts for legal and regulatory compliance issues
- **Termination Management**: Manage contract termination procedures and data return requirements
- **Regulatory Updates**: Monitor regulatory changes affecting vendor management requirements

**4.5 Finance Team**

- **Vendor Financial Assessment**: Conduct basic financial stability assessment for Tier 1 vendors
- **Insurance Verification**: Verify vendor insurance coverage and liability requirements
- **Cost Management**: Monitor vendor costs and identify optimization opportunities
- **Payment Processing**: Manage vendor payment processes and contract billing requirements
- **Budget Planning**: Include vendor management costs in annual budget planning

**4.6 Development Team**

- **API Integration**: Implement secure API integrations with vendor services
- **Data Minimization**: Ensure only necessary data is shared with vendor systems
- **Security Controls**: Implement application-level security controls for vendor data access
- **Testing and Validation**: Test vendor integrations for security and performance requirements
- **Documentation**: Document vendor integrations and security implementations

### 5. Implementation Guidelines

**5.1 Practical Implementation Approach**

**Phase 1: Vendor Inventory and Classification (Month 1)**
- Create inventory of current vendors and classify into risk tiers
- Identify vendors requiring immediate BAA execution (ePHI access)
- Implement automated vendor risk assessment platform
- Establish vendor management procedures and templates

**Phase 2: Critical Vendor Assessment (Months 2-3)**
- Complete comprehensive assessment of Tier 1 vendors
- Execute required Business Associate Agreements
- Implement enhanced monitoring for critical vendors
- Review and optimize high-cost vendor relationships

**Phase 3: Automation and Monitoring (Months 3-6)**
- Deploy automated vendor security monitoring tools
- Establish regular review cycles for vendor relationships
- Optimize vendor access management through SSO integration
- Implement cost optimization and contract management processes

**5.2 Vendor Management Tools and Automation**

**Automated Risk Assessment Platforms**
- **SecurityScorecard** or **BitSight**: Continuous vendor security rating and monitoring
- **UpGuard** or **RiskRecon**: Automated security questionnaires and vendor assessment
- **ServiceNow Vendor Risk Management**: Integrated vendor lifecycle management
- **Shared Assessments SIG**: Standardized security questionnaire automation

**Contract and Compliance Management**
- **DocuSign** or **PandaDoc**: Electronic contract execution and BAA management
- **ContractWorks** or **Ironclad**: Contract lifecycle management and automated renewals
- **LogicGate** or **Resolver**: Risk management and compliance tracking
- **Google Workspace** or **Microsoft 365**: Document collaboration and approval workflows

**Access and Identity Management**
- **Okta** or **Azure AD**: Single sign-on and vendor access management
- **LastPass** or **1Password**: Shared credential management for vendor systems
- **AWS IAM** or **Azure RBAC**: Cloud vendor access controls and monitoring
- **Privileged Access Management**: Just-in-time access for vendor support activities

**5.3 Cost-Effective Vendor Management**

**Vendor Consolidation Opportunities**
- Identify overlapping vendor capabilities and consolidation opportunities
- Negotiate volume discounts for multi-service vendor relationships
- Standardize on major cloud platforms to simplify compliance management
- Eliminate redundant or underutilized vendor services

**Contract Optimization Strategies**
- Use standard contract templates to reduce legal review costs
- Negotiate standardized security terms across similar vendor types
- Implement automatic renewal with security review checkpoints
- Focus contract negotiations on business terms rather than security boilerplate

**Compliance Efficiency**
- Accept major cloud provider compliance certifications as sufficient for most use cases
- Use vendor compliance databases and shared assessment results
- Implement automated compliance monitoring rather than manual audits
- Focus on outcome-based security requirements rather than prescriptive controls

### 6. Standards Compliance

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

### 7. Definitions

**Business Associate Agreement (BAA):** A written contract between a covered entity and a business associate required by HIPAA for any ePHI access.

**Cloud Service Provider:** A company that offers network services, infrastructure, or business applications in the cloud (e.g., AWS, Azure, GCP).

**Risk Tier:** Classification system for vendors based on data access and business criticality (Tier 1-Critical, Tier 2-Business, Tier 3-Standard).

**Security Scorecard:** Automated security rating system that continuously monitors vendor security posture using external security indicators.

**Single Sign-On (SSO):** Authentication system that allows users to access multiple vendor systems with one set of credentials.

**Vendor Risk Assessment:** Streamlined evaluation process appropriate to vendor risk tier and data access requirements.

### 8. Related Policies and Procedures

This policy shall be implemented in conjunction with the following organizational policies:

- **Data Classification and Handling Policy (SEC-POL-001)**: Defines data sensitivity levels for vendor risk classification
- **Access Control Policy (AC-POL-001)**: Establishes access control requirements for vendor systems
- **Incident Response Policy (SEC-POL-006)**: Addresses vendor-related security incident procedures
- **Encryption and Key Management Policy (OP-POL-001)**: Covers encryption requirements for vendor data protection

**Supporting Procedures:**
- **Vendor Risk Assessment Procedure (SEC-PROC-013)**: Detailed procedures for vendor risk assessment and classification
- **Business Associate Agreement Management Procedure (SEC-PROC-014)**: BAA execution and management procedures
- **Vendor Access Management Procedure (AC-PROC-006)**: Technical procedures for vendor access provisioning and management
