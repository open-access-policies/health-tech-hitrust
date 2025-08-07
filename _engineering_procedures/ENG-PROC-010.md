---
title: Media Security Management Procedures (ENG-PROC-010)
parent: Engineering Procedures
nav_order: 10
---

# Media Security Management Procedures (ENG-PROC-010)

**Document Classification**: Internal Use Only  
**Version**: 1.0  
**Effective Date**: **[Date]**  
**Review Date**: **[Annual Review Date]**  
**Document Owner**: **[Information Security Officer]**

## 1. Purpose

This procedure establishes standardized processes for the secure handling, labeling, transportation, and disposal of portable media and digital storage devices containing or potentially containing electronic Protected Health Information (ePHI) and other sensitive data. This procedure ensures compliance with regulatory requirements and organizational security policies for media protection throughout its lifecycle.

## 2. Scope

This procedure applies to all **[Company Name]** personnel, contractors, business associates, and third parties who handle, transport, store, or dispose of any portable media including but not limited to:
- USB drives, external hard drives, and portable storage devices
- Optical media (CDs, DVDs, Blu-ray discs)
- Magnetic tape media and backup cartridges
- Removable solid-state drives and memory cards
- Paper records and printouts containing sensitive information
- Mobile devices and laptops when used as portable storage

## 3. Overview

Media security management requires comprehensive tracking and protection from creation through disposal. This includes proper labeling, encryption requirements, transportation security, and certified destruction methods. All media handling activities must be documented and auditable to ensure regulatory compliance and prevent unauthorized disclosure of sensitive information.

## 4. Procedure

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | **Media Owner/Creator** | Create media inventory entry in **[Asset Management System]** with unique identifier, content classification, encryption status, and assigned custodian |
| **2** | **Media Owner/Creator** | Apply appropriate security label indicating classification level (Public, Internal, Confidential, Restricted) and handling requirements |
| **3** | **Media Owner/Creator** | Encrypt all media containing Confidential or Restricted data using **[Approved Encryption Standards, e.g., AES-256]** with organization-managed keys |
| **4** | **Media Custodian** | Verify encryption implementation and test data accessibility before initial use or distribution |
| **5** | **Media Custodian** | Store media in appropriate secure location based on classification: locked cabinet (Internal), safe (Confidential), or vault (Restricted) |
| **6** | **Transportation Personnel** | For media transportation, use tamper-evident packaging with chain of custody documentation and pre-approved courier services |
| **7** | **Transportation Personnel** | Maintain continuous custody during transport or use bonded courier services with tracking and signature confirmation |
| **8** | **Receiving Personnel** | Upon receipt, verify package integrity, validate chain of custody documentation, and test media accessibility |
| **9** | **Media Custodian** | Conduct monthly physical inventory verification comparing actual media location with inventory system records |
| **10** | **Media Custodian** | Report any missing, damaged, or compromised media immediately to **[Information Security Officer]** and initiate incident response |
| **11** | **Media Custodian** | For media reuse, perform secure data sanitization using **[NIST SP 800-88]** compliant methods before reassignment |
| **12** | **Media Custodian** | Document sanitization method used, verification of data removal, and approval for reuse in asset management system |
| **13** | **Disposal Personnel** | For end-of-life media, use certified destruction services with certificate of destruction for all Confidential and Restricted media |
| **14** | **Disposal Personnel** | For media containing ePHI, ensure destruction method meets HIPAA requirements and obtain detailed destruction certificate |
| **15** | **Information Security Officer** | Review monthly media inventory reports and investigate any discrepancies or unauthorized media usage |
| **16** | **Information Security Officer** | Conduct quarterly assessment of media security controls and update procedures based on risk assessment findings |
| **17** | **Compliance Officer** | Maintain destruction certificates and inventory records for minimum **[Retention Period, e.g., 7 years]** for audit and regulatory compliance |

## 5. Standards Compliance

This procedure addresses the following regulatory and compliance requirements:

| **Procedure Section** | **Standard/Framework** | **Control Reference** |
| --------------------- | ---------------------- | --------------------- |
| **4.1, 4.2, 4.3, 4.15** | HITRUST CSF v11.2.0 | 03.a - Portable Media Security |
| **4.5, 4.10, 4.13** | HITRUST CSF v11.2.0 | 03.b - Portable Media Management |
| **4.11, 4.12, 4.13, 4.14** | HITRUST CSF v11.2.0 | 03.c - Information Disposal |
| **4.1, 4.2, 4.3** | SOC 2 Trust Services Criteria | CC6.1 - Logical Access Security |
| **4.3, 4.11, 4.12** | SOC 2 Trust Services Criteria | CC6.7 - Data Transmission and Disposal |
| **4.3, 4.11, 4.14** | HIPAA Security Rule | 45 CFR § 164.310(d)(1) - Device and Media Controls |
| **4.13, 4.14** | HIPAA Security Rule | 45 CFR § 164.310(d)(2) - Data Disposal |
| **4.11, 4.12** | NIST SP 800-88 | Media Sanitization Guidelines |

**Document Control**: This procedure shall be reviewed annually and updated as needed to reflect changes in technology, regulatory requirements, and organizational security posture. All changes must be approved by the **[Information Security Officer]** and **[Chief Technology Officer]**.

**Training Requirements**: All personnel handling portable media must complete media security training within **[Duration, e.g., 30 days]** of role assignment and annually thereafter.

**Related Documents**:
- Infrastructure Security Policy (ENG-POL-003)
- Data Classification and Handling Policy (SEC-POL-004)
- Incident Response Procedures (SEC-PROC-001)
