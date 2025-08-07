---
title: Guest Network Isolation and Security Procedures (ENG-PROC-012)
parent: Engineering Procedures
nav_order: 12
---

# Guest Network Isolation and Security Procedures (ENG-PROC-012)

## 1. Purpose

This procedure establishes secure guest network infrastructure with complete isolation from corporate networks containing electronic Protected Health Information (ePHI) and sensitive business data. This procedure ensures guest access does not compromise organizational security while providing appropriate internet access for visitors, contractors, and business partners.

## 2. Scope

This procedure applies to all guest network infrastructure and access within **[Company Name]** facilities, including:
- Visitor wireless network access and authentication systems
- Contractor and temporary worker network access
- Business partner and vendor network connectivity
- Conference room and meeting space guest access
- Guest network monitoring and traffic inspection systems
- Guest device registration and access control processes

## 3. Overview

Guest network security requires complete network isolation, traffic monitoring, and access controls to prevent unauthorized access to corporate resources. This includes dedicated network infrastructure, content filtering, bandwidth management, and comprehensive logging of all guest network activity. Guest access must be time-limited and subject to appropriate use policies.

## 4. Procedure

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | **Network Administrator** | Deploy dedicated guest network infrastructure with complete Layer 2 and Layer 3 isolation from corporate networks |
| **2** | **Network Administrator** | Configure guest network VLAN with no routing to corporate VLANs and dedicated internet gateway with NAT |
| **3** | **Network Administrator** | Implement guest network access controls requiring **[Authentication Method, e.g., sponsored access, SMS verification]** for connection approval |
| **4** | **Reception/Security Staff** | For visitor access, collect visitor information, verify identity, and generate time-limited guest credentials valid for **[Duration, e.g., 8 hours]** |
| **5** | **Sponsor/Host Employee** | Approve guest access requests through **[Guest Management System]** with business justification and access duration specification |
| **6** | **Guest Management System** | Automatically provision guest credentials with specified time limits, bandwidth restrictions, and content filtering policies |
| **7** | **Network Administrator** | Configure guest network content filtering blocking access to malicious websites, social media, streaming services, and inappropriate content |
| **8** | **Network Administrator** | Implement bandwidth limiting for guest users with maximum **[Bandwidth Limit, e.g., 10 Mbps per device]** and total **[Total Bandwidth, e.g., 100 Mbps]** |
| **9** | **Security Operations Center** | Monitor guest network traffic continuously for malicious activity, data exfiltration attempts, and policy violations |
| **10** | **Guest Management System** | Log all guest network connections including device MAC addresses, connection times, data usage, and visited websites |
| **11** | **Network Administrator** | Perform daily review of guest network logs to identify security events, policy violations, and system performance issues |
| **12** | **Security Operations Center** | Investigate and respond to guest network security alerts within **[Duration, e.g., 30 minutes]** including device isolation if necessary |
| **13** | **Network Administrator** | Automatically terminate guest access upon credential expiration and remove device associations from access control systems |
| **14** | **Network Administrator** | Conduct weekly guest network penetration testing to verify isolation effectiveness and identify potential security gaps |
| **15** | **Information Security Officer** | Review monthly guest network security reports including usage statistics, security events, and compliance metrics |
| **16** | **Network Security Manager** | Perform quarterly guest network security assessment and update isolation controls based on risk assessment findings |
| **17** | **Compliance Officer** | Maintain guest network access logs for minimum **[Retention Period, e.g., 1 year]** for security incident investigation and compliance |

## 5. Standards Compliance

This procedure addresses the following regulatory and compliance requirements:

| **Procedure Section** | **Standard/Framework** | **Control Reference** |
| --------------------- | ---------------------- | --------------------- |
| **4.1, 4.2, 4.3** | HITRUST CSF v11.2.0 | 08.a - Network Controls |
| **4.1, 4.2, 4.14** | HITRUST CSF v11.2.0 | 08.f - Network Segregation |
| **4.7, 4.8, 4.9** | HITRUST CSF v11.2.0 | 08.h - Network Connection Control |
| **4.4, 4.5, 4.6** | HITRUST CSF v11.2.0 | 11.a - User Access Provisioning |
| **4.10, 4.11, 4.15** | HITRUST CSF v11.2.0 | 12.a - Audit Logging and Monitoring |
| **4.1, 4.2** | SOC 2 Trust Services Criteria | CC6.1 - Logical Access Security |
| **4.9, 4.10, 4.12** | SOC 2 Trust Services Criteria | CC7.2 - System Monitoring |
| **4.1, 4.2, 4.14** | HIPAA Security Rule | 45 CFR § 164.312(e)(1) - Transmission Security |
| **4.4, 4.13** | HIPAA Security Rule | 45 CFR § 164.308(a)(4) - Access Management |

