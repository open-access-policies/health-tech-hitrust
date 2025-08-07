---
title: Intrusion Detection and Prevention System Procedures (ENG-PROC-008)
parent: Engineering Procedures
nav_order: 8
---

### 1. Purpose

This procedure establishes comprehensive processes for deploying, configuring, maintaining, and operating Intrusion Detection and Prevention Systems (IDS/IPS) to detect and prevent network-based security attacks. These procedures support the Infrastructure Security Policy (ENG-POL-003) and ensure effective implementation of HITRUST CSF v11.2.0 Domain 08 - Network Protection controls.

### 2. Scope

This procedure applies to all Network Security Engineers, SOC Analysts, and Infrastructure Security team members responsible for deploying, configuring, and monitoring IDS/IPS systems across **[Company Name]**'s network infrastructure, including cloud environments, on-premises networks, and hybrid architectures.

### 3. Overview

Intrusion Detection and Prevention Systems provide automated monitoring, detection, and response capabilities to identify and block network-based security threats in real-time. This procedure defines the technical implementation, operational processes, and maintenance requirements for maintaining effective IDS/IPS coverage across the organization's network infrastructure.

### 4. Procedure

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Network Security Engineer | **IDS/IPS Architecture Design**: Design IDS/IPS deployment architecture to provide comprehensive coverage of network segments including: perimeter defense, internal network monitoring, cloud workload protection, and critical asset protection. Document sensor placement and coverage areas. |
| **2** | Network Security Engineer | **System Deployment**: Deploy IDS/IPS sensors at strategic network locations including: internet gateway, DMZ segments, internal network choke points, data center ingress/egress, and cloud virtual network perimeters. Configure sensors for appropriate network segments and traffic volumes. |
| **3** | Network Security Engineer | **Initial Configuration**: Configure IDS/IPS systems with baseline security policies including: signature-based detection rules, anomaly detection thresholds, protocol analysis settings, and geographic IP filtering. Import vendor-provided rule sets and customize for organizational requirements. |
| **4** | Network Security Engineer | **Signature Management**: Implement automated signature update processes to ensure IDS/IPS systems receive the latest threat detection signatures within **[Timeframe, e.g., 24 hours]** of release. Configure update scheduling to minimize impact on network operations. |
| **5** | SOC Analyst | **Rule Tuning and Optimization**: Perform initial rule tuning to reduce false positives while maintaining detection effectiveness. Analyze **[Duration, e.g., 2 weeks]** of baseline traffic to adjust thresholds and customize detection rules for the environment. |
| **6** | SOC Analyst | **Alert Monitoring**: Monitor IDS/IPS alerts continuously through centralized management console and SIEM integration. Acknowledge and investigate alerts within **[Timeframe, e.g., 5 minutes]** for Critical severity and **[Timeframe, e.g., 15 minutes]** for High severity events. |
| **7** | SOC Analyst | **Alert Analysis and Classification**: For each IDS/IPS alert, perform analysis to determine attack type, severity, and potential impact. Classify alerts as: **Critical** (active exploitation), **High** (reconnaissance/probing), **Medium** (policy violations), **Low** (informational), or **False Positive**. |
| **8** | SOC Analyst | **Threat Investigation**: For valid security alerts, conduct detailed investigation including: analysis of attack signatures, review of source IP reputation, examination of target systems, and correlation with other security events. Document findings in incident tracking system. |
| **9** | SOC Analyst | **Automated Response Actions**: Configure and monitor automated response actions including: blocking malicious IP addresses, resetting suspicious connections, quarantining affected systems, and generating high-priority alerts for incident response team. |
| **10** | Network Security Engineer | **Prevention Policy Management**: Manage IPS prevention policies to balance security protection with network availability. Configure blocking actions for confirmed threats while implementing monitoring-only mode for new or untested signatures. |
| **11** | Network Security Engineer | **Performance Monitoring**: Monitor IDS/IPS system performance including: throughput capacity, latency impact, CPU and memory utilization, and signature processing rates. Ensure systems maintain **[Percentage, e.g., 99%]** availability and minimal network impact. |
| **12** | SOC Analyst | **Incident Escalation**: For confirmed attacks or critical security events, escalate to Incident Response Team per RES-PROC-001. Provide IDS/IPS evidence including alert details, packet captures, and attack analysis to support incident investigation. |
| **13** | Network Security Engineer | **Log Management and Retention**: Configure IDS/IPS systems to forward security events to centralized SIEM system in real-time. Ensure local log retention for **[Duration, e.g., 30 days]** and compliance with SEC-POL-009 retention requirements. |
| **14** | Network Security Engineer | **Custom Rule Development**: Develop custom detection rules for organization-specific threats, applications, and attack patterns not covered by vendor signatures. Test custom rules in monitoring mode before deploying prevention actions. |
| **15** | SOC Analyst | **False Positive Management**: Investigate and document false positive alerts. Coordinate with Network Security Engineer to tune detection rules, adjust thresholds, or create exception rules to reduce false positives while maintaining security coverage. |
| **16** | Network Security Engineer | **System Maintenance**: Perform regular maintenance activities including: software updates, signature database updates, configuration backups, hardware health checks, and capacity planning. Schedule maintenance during approved change windows. |
| **17** | Network Security Engineer | **Monthly Effectiveness Review**: Conduct monthly review of IDS/IPS effectiveness including: detection rates, false positive trends, blocked attack statistics, and system performance metrics. Generate reports for security management and identify improvement opportunities. |

### 5. IDS/IPS Deployment Architecture

#### 5.1 Network-Based IDS/IPS (NIDS/NIPS)

**Perimeter Deployment:**
- Internet gateway and firewall ingress/egress points
- DMZ network segments and external-facing services
- VPN termination points and remote access gateways
- Cloud internet gateway and NAT gateway monitoring

**Internal Network Deployment:**
- Core network switches and router choke points
- Inter-VLAN communication monitoring points
- Critical server network segments
- Database and application tier networks

#### 5.2 Host-Based IDS/IPS (HIDS/HIPS)

**Critical System Protection:**
- Database servers and application servers
- Domain controllers and authentication systems
- Management and administrative workstations
- Cloud virtual machines and containers

**Endpoint Integration:**
- Integration with endpoint detection and response (EDR) systems
- Centralized management and policy distribution
- Real-time threat detection and automated response
- Compliance monitoring and reporting

### 6. Detection and Prevention Capabilities

#### 6.1 Signature-Based Detection

**Attack Signatures:**
- Known exploit patterns and vulnerability signatures
- Malware communication and command-and-control patterns
- Web application attack signatures (SQL injection, XSS)
- Network protocol violations and anomalies

**Signature Management:**
- Automated signature updates from vendor threat intelligence
- Custom signature development for organization-specific threats
- Signature testing and validation before production deployment
- Performance impact assessment for new signatures

#### 6.2 Anomaly-Based Detection

**Behavioral Analysis:**
- Network traffic pattern analysis and baseline deviation
- Protocol behavior monitoring and anomaly detection
- Geographic location analysis and suspicious source detection
- Time-based analysis for off-hours activity monitoring

**Machine Learning Integration:**
- Advanced analytics for unknown threat detection
- User and entity behavior analytics (UEBA) integration
- Adaptive learning from network traffic patterns
- Continuous model training and accuracy improvement

### 7. Alert Management and Response

#### 7.1 Alert Severity Classification

| **Severity Level** | **Definition** | **Response Time** | **Automated Actions** |
| ------------------ | -------------- | ----------------- | -------------------- |
| **Critical** | Active exploitation or data breach | Immediate (5 minutes) | Block source IP, alert SOC, isolate systems |
| **High** | Reconnaissance or attack attempts | 15 minutes | Monitor closely, alert security team |
| **Medium** | Policy violations or suspicious activity | 2 hours | Log and analyze, investigate patterns |
| **Low** | Informational events or minor anomalies | 24 hours | Document and trend analysis |
| **False Positive** | Confirmed benign activity | Best effort | Tune rules, create exceptions |

#### 7.2 Response Procedures

**Immediate Response (Critical):**
1. Automatically block malicious source IP addresses
2. Alert SOC analysts and incident response team
3. Isolate affected systems from network if necessary
4. Preserve network traffic captures for forensic analysis
5. Initiate incident response procedures per RES-PROC-001

**Investigation Response (High/Medium):**
1. Analyze attack patterns and indicators of compromise
2. Review source IP reputation and geographic location
3. Examine target systems for signs of compromise
4. Correlate with other security events and threat intelligence
5. Document findings and recommendations for action

### 8. Performance and Capacity Management

#### 8.1 System Performance Metrics

| **Metric** | **Target** | **Monitoring Frequency** |
| ---------- | ---------- | ------------------------ |
| System Availability | >99% uptime | Continuous |
| Processing Latency | <10ms additional delay | Real-time |
| Throughput Capacity | Handle peak traffic without drops | Daily |
| Alert Response Time | <5 minutes for Critical | Real-time |
| False Positive Rate | <5% of total alerts | Weekly |

#### 8.2 Capacity Planning

**Traffic Volume Analysis:**
- Daily, weekly, and monthly traffic pattern analysis
- Peak capacity planning and system scaling requirements
- Signature processing capacity and performance impact
- Storage requirements for logs and packet captures

**System Scaling:**
- Horizontal scaling capabilities for increased traffic volumes
- Load balancing across multiple IDS/IPS sensors
- Cloud-based auto-scaling for variable workloads
- Performance optimization and hardware upgrade planning

### 9. Integration and Interoperability

#### 9.1 SIEM Integration

**Event Forwarding:**
- Real-time forwarding of IDS/IPS alerts to SIEM system
- Structured log format for automated correlation and analysis
- Event enrichment with network context and threat intelligence
- Custom parsing rules for vendor-specific log formats

**Correlation Rules:**
- Cross-system event correlation for advanced threat detection
- Integration with endpoint, application, and infrastructure logs
- Automated incident creation and escalation workflows
- Threat intelligence integration for enhanced context

#### 9.2 Security Orchestration Integration

**Automated Response:**
- Integration with security orchestration platforms (SOAR)
- Automated containment and remediation actions
- Workflow automation for common incident response tasks
- Integration with network security tools for coordinated response

### 10. Maintenance and Updates

#### 10.1 Regular Maintenance Activities

**Daily Tasks:**
- Monitor system health and performance dashboards
- Review and investigate high-priority alerts
- Verify signature update success and system status
- Check system capacity and resource utilization

**Weekly Tasks:**
- Analyze false positive trends and tune detection rules
- Review blocked attack statistics and threat patterns
- Update custom signatures and detection rules
- Conduct system performance optimization

**Monthly Tasks:**
- Comprehensive effectiveness review and reporting
- Signature database cleanup and optimization
- System capacity planning and hardware assessment
- Security policy review and update recommendations

#### 10.2 Emergency Procedures

**System Failure Response:**
- Immediate notification of security team and management
- Failover to backup IDS/IPS systems where available
- Network traffic bypass procedures for critical business operations
- Accelerated repair and restoration procedures

**Security Incident Response:**
- Preservation of IDS/IPS logs and evidence for investigation
- Coordination with incident response team for forensic analysis
- Emergency signature updates for active threats
- Temporary prevention rule deployment for immediate protection

### 11. Standards Compliance

This procedure is designed to comply with and support the following industry standards and regulations.

| **Procedure Section** | **Standard/Framework** | **Control Reference** |
| --------------------- | ---------------------- | --------------------- |
| **All** | HITRUST CSF v11.2.0 | 08.e - Intrusion Detection/Prevention |
| **4.6-4.8** | HITRUST CSF v11.2.0 | 08.c - Network Monitoring |
| **4.9** | HITRUST CSF v11.2.0 | 08.b - Network Security Controls |
| **7** | HITRUST CSF v11.2.0 | 15.a - Incident Response Process |
| **All** | SOC 2 Trust Services Criteria | CC6.6 - Network Security |
| **4.12** | SOC 2 Trust Services Criteria | CC7.1 - System Monitoring |
| **7** | SOC 2 Trust Services Criteria | CC7.2 - System Monitoring - Detection |
| **All** | NIST Cybersecurity Framework | DE.CM - Security Continuous Monitoring |
| **7** | NIST Cybersecurity Framework | RS.MI - Mitigation |

### 12. Artifact(s)

- IDS/IPS deployment architecture documentation
- System configuration and rule management procedures
- Daily operational reports and alert summaries
- Monthly effectiveness review reports
- Incident investigation reports with IDS/IPS evidence

### 13. Definitions

**False Positive:** An alert generated by IDS/IPS that incorrectly identifies benign activity as malicious.

**Intrusion Detection System (IDS):** Security system that monitors network traffic and system activities for malicious activities.

**Intrusion Prevention System (IPS):** Security system that monitors network traffic and can take automated actions to block detected threats.

**Signature:** Predefined pattern or rule used to identify known attack methods or malicious activities.

**Threat Intelligence:** Information about current and emerging security threats used to enhance detection capabilities.

**Tuning:** Process of adjusting IDS/IPS rules and thresholds to optimize detection accuracy and reduce false positives.

### 14. Responsibilities

| **Role** | **Responsibility** |
| -------- | ---------------- |
| **Network Security Engineer** | IDS/IPS deployment, configuration, maintenance, and performance optimization. |
| **SOC Analyst** | Real-time monitoring, alert investigation, and incident escalation for IDS/IPS events. |
| **Security Officer** | Program oversight, policy compliance, and resource allocation for IDS/IPS capabilities. |
| **Incident Response Team** | Investigation of confirmed security incidents and coordination with IDS/IPS evidence. |
| **System Administrator** | Network infrastructure support and coordination for IDS/IPS deployment. |
