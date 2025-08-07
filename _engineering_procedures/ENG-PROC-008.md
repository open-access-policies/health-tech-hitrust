---
title: Intrusion Detection and Prevention System Procedures (ENG-PROC-008)
parent: Engineering Procedures
nav_order: 8
---

### 1. Purpose

This procedure establishes processes for implementing and managing cloud-native intrusion detection and prevention capabilities to detect and respond to network-based security threats. These procedures support the Infrastructure Security Policy (ENG-POL-003) and ensure effective implementation of HITRUST CSF v11.2.0 Domain 08 - Network Protection controls using practical, automated approaches suitable for a growing health tech organization.

### 2. Scope

This procedure applies to the Security Officer, Platform Engineers, DevOps Engineers, and Cloud Infrastructure teams responsible for configuring and managing cloud-native IDS/IPS services and coordinating with managed security service providers across **[Company Name]**'s cloud infrastructure.

### 3. Overview

Intrusion detection and prevention leverages cloud-native security services, managed threat detection platforms, and automated response capabilities to identify and block network-based security threats. This approach eliminates the complexity of managing dedicated IDS/IPS infrastructure while providing enterprise-grade threat detection suitable for a **[Number, e.g., 120]**-person organization.

### 4. Procedure

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Platform Engineer | **Cloud IDS/IPS Service Activation**: Enable cloud-native intrusion detection services (AWS GuardDuty, Azure Defender for Network, GCP Cloud IDS) with default threat detection rule sets. Configure automatic threat intelligence updates and baseline learning. |
| **2** | DevOps Engineer | **Network Security Group Configuration**: Configure cloud security groups and network access control lists (NACLs) to provide basic network-level intrusion prevention. Implement default-deny policies with explicit allow rules for required traffic. |
| **3** | Platform Engineer | **Web Application Firewall (WAF) Deployment**: Deploy cloud WAF services (AWS WAF, Azure Front Door, CloudFlare) on internet-facing applications to detect and block common web attacks including SQL injection, XSS, and DDoS attempts. |
| **4** | Security Officer | **Managed IDS/IPS Service Integration**: Integrate cloud-native IDS services with the managed security service provider's SIEM platform for 24/7 monitoring and analysis. Ensure proper log forwarding and alert escalation procedures. |
| **5** | Platform Engineer | **Automated Threat Response Configuration**: Configure automated response actions including: automatic IP blocking through security groups, traffic inspection escalation, and alert generation for security team review. |
| **6** | DevOps Engineer | **DNS Protection Implementation**: Enable DNS-based threat protection services (AWS Route 53 Resolver DNS Firewall, Azure DNS) to block access to known malicious domains and command & control servers automatically. |
| **7** | MSSP SOC Analyst | **Continuous Threat Monitoring**: MSSP provides 24/7 monitoring of cloud IDS/IPS alerts and events. Performs initial threat analysis and escalates confirmed threats according to established service level agreements. |
| **8** | Platform Engineer | **VPC/Virtual Network Monitoring**: Configure VPC Flow Logs and virtual network monitoring to capture network traffic metadata for analysis. Enable automated analysis for suspicious traffic patterns and geographic anomalies. |
| **9** | Security Officer | **Alert Escalation Coordination**: Coordinate response to escalated threats from MSSP including implementation of recommended containment actions, system isolation, and incident response procedures per RES-PROC-001. |
| **10** | DevOps Engineer | **Performance and Availability Monitoring**: Monitor cloud security service performance and availability. Ensure IDS/IPS services maintain **[Percentage, e.g., 99.5%]** availability and minimal impact on application performance. |
| **11** | Platform Engineer | **Threat Intelligence Integration**: Configure automatic threat intelligence feeds for cloud security services. Enable integration with commercial threat intelligence providers and government threat feeds where available. |
| **12** | Security Officer | **Monthly Security Review**: Review monthly security reports from cloud IDS/IPS services and MSSP including threat trends, blocked attacks, service performance, and recommendations for security posture improvements. |

### 5. Cloud-Native IDS/IPS Services

#### 5.1 Amazon Web Services (AWS)

- **AWS GuardDuty:**
- Machine learning-based threat detection for AWS environments
- Automatic analysis of VPC Flow Logs, DNS logs, and CloudTrail events
- Built-in threat intelligence from AWS Security, CrowdStrike, and Proofpoint
- Integration with AWS Security Hub for centralized security management

- **AWS Shield and WAF:**
- DDoS protection and web application firewall capabilities
- Automatic blocking of common web attacks and volumetric attacks
- Custom rule creation for application-specific threats
- Integration with CloudFront and Application Load Balancers

- **AWS Network Firewall:**
- Managed network firewall service with intrusion prevention capabilities
- Stateful inspection and automatic threat signature updates
- Custom rule development for organization-specific threats
- Integration with AWS Transit Gateway for centralized management

#### 5.2 Microsoft Azure

- **Azure Defender for Networks:**
- Advanced threat protection for Azure virtual networks
- Network layer attack detection and automatic response
- Integration with Azure Sentinel for centralized security monitoring
- Just-in-time network access controls and adaptive network hardening

- **Azure DDoS Protection:**
- Automatic DDoS attack detection and mitigation
- Real-time attack metrics and alerting
- Integration with Azure Monitor for performance monitoring
- Cost protection and automatic scaling during attacks

- **Azure Firewall:**
- Managed cloud-native network security service
- Application and network-level filtering with threat intelligence
- Outbound traffic filtering and URL filtering capabilities
- Integration with Azure Security Center for policy management

#### 5.3 Google Cloud Platform (GCP)

- **Google Cloud IDS:**
- Managed intrusion detection service for GCP environments
- Network traffic analysis with machine learning-based threat detection
- Integration with Google Cloud Security Command Center
- Automatic threat signature updates and custom rule support

- **Google Cloud Armor:**
- Web application firewall and DDoS protection service
- Edge security policies and geo-based access controls
- Rate limiting and bot protection capabilities
- Integration with Google Load Balancers and CDN services

### 6. Managed Security Service Integration

#### 6.1 MSSP IDS/IPS Monitoring Requirements

- **24/7 Security Operations Center:**
- Continuous monitoring of cloud IDS/IPS alerts and events
- Expert threat analysis and incident classification
- Escalation procedures for confirmed security threats
- Integration with existing incident response workflows

- **Threat Intelligence and Analysis:**
- Access to premium threat intelligence feeds
- Advanced analytics and correlation capabilities
- Custom threat hunting and investigation services
- Regular threat landscape briefings and security advisories

#### 6.2 Service Level Agreements

- **Response Time Requirements:**
- Critical threats: **[Timeframe, e.g., 15 minutes]** acknowledgment, **[Timeframe, e.g., 1 hour]** analysis
- High severity threats: **[Timeframe, e.g., 1 hour]** acknowledgment, **[Timeframe, e.g., 4 hours]** analysis
- Medium severity events: **[Timeframe, e.g., 4 hours]** acknowledgment, **[Timeframe, e.g., 24 hours]** analysis

- **Availability and Performance:**
- MSSP SOC availability: 99.9% uptime
- Cloud service monitoring: 24/7/365 coverage
- Threat analysis accuracy: >95% true positive rate
- Customer notification: Within SLA response times

### 7. Automated Threat Response

#### 7.1 Automatic Response Actions

- **Network-Level Responses:**
- Automatic blocking of malicious IP addresses through security groups
- Traffic redirection through inspection services for suspicious flows
- DNS sinkholing for known malicious domains
- Rate limiting and traffic shaping for potential DDoS attacks

- **Application-Level Responses:**
- WAF rule activation for detected attack patterns
- Automatic scaling of protection services during high-volume attacks
- Session termination for confirmed malicious users
- Geographic blocking for attacks from high-risk regions

#### 7.2 Response Escalation Triggers

- **Immediate Escalation (Critical):**
- Confirmed data exfiltration attempts
- Command and control communications
- Lateral movement indicators
- Privilege escalation attempts
- Multiple attack vectors from same source

- **Standard Escalation (High/Medium):**
- Persistent reconnaissance activities
- Application vulnerability exploitation attempts
- Suspicious outbound communications
- Failed authentication attack patterns
- Policy violation accumulations

### 8. Performance Monitoring and Optimization

#### 8.1 Service Performance Metrics

| **Metric** | **Target** | **Monitoring Frequency** |
| ---------- | ---------- | ------------------------ |
| Service Availability | >99.5% uptime | Real-time |
| Detection Accuracy | >95% true positives | Weekly |
| Response Time | <5ms latency impact | Real-time |
| False Positive Rate | <10% of alerts | Monthly |
| Blocked Threat Volume | Trending and reporting | Daily |

#### 8.2 Cost Optimization

- **Service Right-Sizing:**
- Regular review of cloud security service utilization
- Optimization of traffic inspection and analysis volumes
- Cost-effective threat intelligence feed selection
- Elimination of redundant or overlapping security services

- **Automation Benefits:**
- Reduced manual security operations overhead
- Automatic scaling based on threat volume and traffic patterns
- Self-tuning threat detection with machine learning
- Streamlined incident response through automation

### 9. Standards Compliance

This procedure is designed to comply with and support the following industry standards and regulations.

| **Procedure Section** | **Standard/Framework** | **Control Reference** |
| --------------------- | ---------------------- | --------------------- |
| **All** | HITRUST CSF v11.2.0 | 08.e - Intrusion Detection/Prevention |
| **5** | HITRUST CSF v11.2.0 | 08.c - Network Monitoring |
| **7** | HITRUST CSF v11.2.0 | 08.b - Network Security Controls |
| **7.2** | HITRUST CSF v11.2.0 | 15.a - Incident Response Process |
| **All** | SOC 2 Trust Services Criteria | CC6.6 - Network Security |
| **8** | SOC 2 Trust Services Criteria | CC7.1 - System Monitoring |
| **7** | SOC 2 Trust Services Criteria | CC7.2 - System Monitoring - Detection |
| **All** | NIST Cybersecurity Framework | DE.CM - Security Continuous Monitoring |
| **7** | NIST Cybersecurity Framework | RS.MI - Mitigation |

### 10. Artifact(s)

- Cloud IDS/IPS service configuration documentation
- MSSP service contract and business associate agreement (BAA)
- Monthly threat detection and response reports
- Automated response configuration and testing logs
- Security incident escalation and coordination records

### 11. Definitions

- **Cloud-Native IDS/IPS:** Security services provided by cloud service providers that integrate natively with cloud infrastructure and services.

- **Managed Security Service Provider (MSSP):** Third-party organization providing managed security services including 24/7 monitoring and threat analysis.

- **Automatic Response:** Pre-configured security actions that are triggered automatically upon detection of specific threats or attack patterns.

- **Threat Intelligence:** Real-time information about current and emerging security threats used to enhance detection and prevention capabilities.

- **False Positive:** An alert generated by IDS/IPS that incorrectly identifies benign activity as malicious.

### 12. Responsibilities

| **Role** | **Responsibility** |
| -------- | ---------------- |
| **Security Officer** | MSSP coordination, escalation management, and security program oversight. |
| **Platform Engineer** | Cloud IDS/IPS service configuration, integration, and performance monitoring. |
| **DevOps Engineer** | Security group configuration, automated response implementation, and service availability. |
| **MSSP SOC Analyst** | 24/7 threat monitoring, analysis, and escalation per service agreement. |
| **Cloud Infrastructure Team** | Infrastructure security service deployment and maintenance. |
