---
title: Network Security Monitoring Procedures (ENG-PROC-007)
parent: Engineering Procedures
nav_order: 7
---

### 1. Purpose

This procedure establishes processes for network security monitoring using cloud-native tools and managed security services to detect and respond to network-based security threats. These procedures support the Infrastructure Security Policy (ENG-POL-003) and ensure effective implementation of HITRUST CSF v11.2.0 Domain 08 - Network Protection controls while being practical for a growing health tech organization.

### 2. Scope

This procedure applies to the Security Officer, Platform Engineers, DevOps Engineers, and designated on-call engineering staff responsible for managing network security monitoring through cloud-native tools and coordinating with external managed security service providers across **[Company Name]**'s cloud infrastructure.

### 3. Overview

Network security monitoring leverages cloud-native security tools, automated threat detection, and managed security service providers to provide continuous visibility into network traffic patterns and security threats. This approach eliminates the need for dedicated internal SOC operations while maintaining comprehensive security monitoring capabilities appropriate for a **[Number, e.g., 120]**-person organization.

### 4. Procedure

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Platform Engineer | **Cloud-Native Monitoring Setup**: Configure cloud security monitoring services (AWS GuardDuty, Azure Sentinel, GCP Security Command Center) to automatically monitor VPC flow logs, DNS logs, and network traffic for suspicious activities. Enable automated threat detection with default rule sets. |
| **2** | Security Officer | **Managed Security Service Selection**: Evaluate and select a managed security service provider (MSSP) to provide 24/7 network security monitoring, threat analysis, and incident response capabilities. Ensure MSSP supports HIPAA/HITECH compliance requirements and HITRUST CSF controls. |
| **3** | Platform Engineer | **Security Tool Integration**: Integrate cloud security monitoring tools with the selected MSSP's security information and event management (SIEM) platform. Configure automated log forwarding and ensure proper data retention in compliance with policy requirements. |
| **4** | DevOps Engineer | **Baseline Configuration**: Configure automatic baseline learning for normal network traffic patterns using cloud-native machine learning capabilities. Enable automated alerting for significant deviations from established baselines. |
| **5** | MSSP SOC Analyst | **Continuous Monitoring**: MSSP provides 24/7 monitoring of network security events through cloud security tools and SIEM platforms. Responds to security alerts within agreed service level agreements (typically **[Timeframe, e.g., 15 minutes]** for critical alerts). |
| **6** | MSSP SOC Analyst | **Threat Analysis and Triage**: MSSP security analysts perform initial threat analysis, correlation with threat intelligence, and classification of security events. Escalate confirmed threats to internal security team according to defined escalation procedures. |
| **7** | Security Officer | **Internal Escalation Response**: For escalated security incidents, coordinate internal response using established incident response procedures (RES-PROC-001). Serve as primary liaison with MSSP during active security incidents. |
| **8** | Platform Engineer | **Automated Response Actions**: Configure automated response capabilities for common security events including: automatic blocking of malicious IP addresses, isolation of compromised resources, and scaling of security controls during attacks. |
| **9** | MSSP Security Engineer | **Threat Intelligence Integration**: MSSP maintains and updates threat intelligence feeds, malicious IP databases, and security signatures. Provides regular threat landscape updates and recommendations for security posture improvements. |
| **10** | DevOps Engineer | **Performance and Availability Monitoring**: Monitor cloud security service availability and performance. Ensure security monitoring tools maintain **[Percentage, e.g., 99.5%]** uptime and respond to service degradations that could impact security visibility. |
| **11** | Security Officer | **Weekly Security Review**: Conduct weekly review of MSSP-provided security reports, threat trends, and incident summaries. Assess security posture and coordinate any necessary improvements to monitoring coverage or response procedures. |
| **12** | MSSP Account Manager | **Monthly Service Review**: MSSP provides monthly executive summary reports including: security events overview, threat landscape analysis, service performance metrics, and recommendations for security program improvements. |

### 5. Managed Security Service Requirements

#### 5.1 Service Provider Qualifications

**Required Certifications and Compliance:**
- SOC 2 Type II certified security operations center
- HIPAA Business Associate Agreement (BAA) executed
- HITRUST CSF v11.2.0 certification preferred
- 24/7/365 security operations center coverage
- Incident response capabilities and procedures

**Technical Requirements:**
- Cloud security expertise (AWS, Azure, GCP)
- Advanced threat intelligence capabilities
- Machine learning and behavioral analysis tools
- Integration with major cloud security services
- Compliance reporting and documentation capabilities

#### 5.2 Service Level Agreements

**Response Time Requirements:**
- Critical alerts: **[Timeframe, e.g., 15 minutes]** acknowledgment, **[Timeframe, e.g., 1 hour]** analysis
- High severity alerts: **[Timeframe, e.g., 1 hour]** acknowledgment, **[Timeframe, e.g., 4 hours]** analysis  
- Medium severity alerts: **[Timeframe, e.g., 4 hours]** acknowledgment, **[Timeframe, e.g., 24 hours]** analysis
- Low severity alerts: **[Timeframe, e.g., 24 hours]** acknowledgment, **[Timeframe, e.g., 3 days]** analysis

**Availability Requirements:**
- SOC availability: 99.9% uptime
- SIEM platform availability: 99.5% uptime
- Incident escalation capabilities: 24/7/365
- Monthly service reporting and reviews

### 6. Cloud-Native Security Monitoring Tools

#### 6.1 AWS Security Services

**Amazon GuardDuty:**
- Threat detection using machine learning and behavioral analysis
- Integration with AWS VPC Flow Logs and DNS logs
- Automatic detection of cryptocurrency mining, command & control communications
- Built-in threat intelligence from AWS Security, CrowdStrike, and Proofpoint

**AWS Security Hub:**
- Centralized security findings from multiple AWS security services
- Compliance monitoring for HIPAA, PCI DSS, and other frameworks
- Integration with third-party security tools
- Automated remediation workflows

**AWS CloudTrail:**
- API logging and monitoring for AWS account activity
- Detection of unusual administrative activities
- Integration with CloudWatch for real-time alerting
- Long-term log retention for compliance and forensics

#### 6.2 Azure Security Services

**Azure Sentinel:**
- Cloud-native SIEM with machine learning capabilities
- Built-in connectors for Office 365, Azure services, and third-party tools
- Automated investigation and response capabilities
- Threat intelligence integration and hunting queries

**Azure Security Center:**
- Unified security management and advanced threat protection
- Compliance dashboard for regulatory requirements
- Security recommendations and vulnerability assessments
- Integration with Azure Policy for automated compliance

#### 6.3 Google Cloud Security Services

**Google Cloud Security Command Center:**
- Centralized security and risk management platform
- Asset discovery and security findings management
- Integration with Chronicle for security analytics
- Threat intelligence and vulnerability scanning

### 7. Incident Escalation and Response

#### 7.1 MSSP Escalation Triggers

**Immediate Escalation (Critical):**
- Confirmed data exfiltration or breach attempt
- Command and control communications detected
- Active lateral movement or privilege escalation
- Ransomware or destructive malware detection
- Administrative account compromise indicators

**Standard Escalation (High/Medium):**
- Persistent advanced threats or APT indicators
- Multiple security control bypass attempts
- Suspicious insider threat activities
- Compliance violation with regulatory implications
- Multiple related security events indicating campaign

#### 7.2 Internal Response Coordination

**Security Officer Responsibilities:**
- Primary point of contact for MSSP escalations
- Coordination with internal incident response team
- Communication with executive management and legal counsel
- Regulatory notification decisions and execution

**Platform Engineer Responsibilities:**
- Technical response to MSSP recommendations
- Implementation of containment and mitigation measures
- System isolation and forensic evidence preservation
- Coordination with DevOps for service availability

**On-Call Engineer Responsibilities:**
- After-hours response to critical security escalations
- Initial assessment and containment actions
- MSSP coordination until Security Officer availability
- Documentation of response actions and decisions

### 8. Performance Metrics and Service Monitoring

#### 8.1 MSSP Performance Metrics

| **Metric** | **Target** | **Measurement Frequency** |
| ---------- | ---------- | ------------------------- |
| Critical Alert Response Time | <15 minutes | Real-time |
| False Positive Rate | <10% | Monthly |
| Escalation Accuracy | >95% | Monthly |
| Service Availability | >99.9% | Daily |
| Customer Satisfaction | >4.5/5.0 | Quarterly |

#### 8.2 Internal Security Indicators

| **KPI** | **Target** | **Review Frequency** |
| ------- | ---------- | -------------------- |
| Mean Time to Containment | <2 hours | Monthly |
| Security Event Volume | Trending analysis | Weekly |
| Compliance Coverage | 100% of requirements | Monthly |
| Cost per Security Event | Optimize quarterly | Quarterly |

### 9. Data Protection and Compliance

#### 9.1 HIPAA/HITECH Compliance

**Business Associate Agreement (BAA):**
- MSSP executes comprehensive BAA covering ePHI handling
- Detailed data processing and security requirements
- Incident notification and reporting procedures
- Regular compliance auditing and assessment requirements

**Data Handling Requirements:**
- ePHI access limited to necessary MSSP personnel
- Encryption in transit and at rest for all security data
- Geographic data residency requirements (US-based SOCs)
- Secure data destruction upon contract termination

#### 9.2 HITRUST CSF Integration

**Control Mapping:**
- MSSP services mapped to specific HITRUST CSF v11.2.0 controls
- Regular assessment of control effectiveness
- Evidence collection for HITRUST certification requirements
- Continuous monitoring of control implementation

### 10. Cost Management and Optimization

#### 10.1 Service Cost Structure

**Fixed Costs:**
- Base MSSP monitoring service fee: $**[Amount, e.g., 15,000-25,000]** monthly
- Cloud security service fees: $**[Amount, e.g., 5,000-10,000]** monthly
- Additional integrations and customizations as needed

**Variable Costs:**
- Security incident investigation fees (per incident)
- Advanced threat hunting services (as requested)
- Additional log ingestion beyond baseline volumes
- Custom report generation and compliance consulting

#### 10.2 Cost Optimization Strategies

**Service Right-Sizing:**
- Regular review of monitoring scope and log volumes
- Optimization of cloud security service configurations
- Elimination of duplicate or redundant monitoring capabilities
- Focus on high-value security events and threat indicators

**Automation and Self-Service:**
- Automated response to common security events
- Self-service access to security dashboards and reports
- Reduced dependency on MSSP for routine activities
- Internal capability development for tier-1 activities

### 11. Standards Compliance

This procedure is designed to comply with and support the following industry standards and regulations.

| **Procedure Section** | **Standard/Framework** | **Control Reference** |
| --------------------- | ---------------------- | --------------------- |
| **All** | HITRUST CSF v11.2.0 | 08.c - Network Monitoring |
| **5.1, 7.1** | HITRUST CSF v11.2.0 | 08.e - Intrusion Detection/Prevention |
| **6** | HITRUST CSF v11.2.0 | 08.b - Network Security Controls |
| **All** | SOC 2 Trust Services Criteria | CC6.6 - Network Security |
| **8** | SOC 2 Trust Services Criteria | CC7.1 - System Monitoring |
| **7** | SOC 2 Trust Services Criteria | CC7.2 - System Monitoring - Detection |
| **All** | NIST Cybersecurity Framework | DE.CM - Security Continuous Monitoring |
| **7.1** | NIST Cybersecurity Framework | DE.AE - Anomalies and Events |

### 12. Artifact(s)

- MSSP service contract and business associate agreement (BAA)
- Cloud security monitoring service configuration documentation
- Monthly MSSP security reports and executive summaries
- Security incident escalation logs and response documentation
- Quarterly security posture assessment reports

### 13. Definitions

**Managed Security Service Provider (MSSP):** Third-party organization providing 24/7 security monitoring, threat detection, and incident response services.

**Security Operations Center (SOC):** Centralized facility where security professionals monitor, analyze, and respond to security events.

**Cloud-Native Security:** Security tools and services built specifically for cloud infrastructure and provided by cloud service providers.

**Security Information and Event Management (SIEM):** Technology that provides real-time analysis of security alerts and events.

**Mean Time to Containment:** Average time between security threat detection and successful containment or mitigation.

### 14. Responsibilities

| **Role** | **Responsibility** |
| -------- | ---------------- |
| **Security Officer** | MSSP relationship management, escalation coordination, and security program oversight. |
| **Platform Engineer** | Cloud security service configuration, integration, and technical response coordination. |
| **DevOps Engineer** | Security tool availability monitoring, automated response implementation, and service optimization. |
| **On-Call Engineer** | After-hours security incident response and MSSP coordination until business hours. |
| **MSSP SOC Analyst** | 24/7 security monitoring, threat analysis, and incident escalation per service agreement. |
