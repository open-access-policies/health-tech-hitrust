---
title: Application Security Testing Procedure (ENG-PROC-001)
parent: Engineering Procedures
nav_order: 1
---
### 1. Purpose

The purpose of this procedure is to detail the process for conducting static application security testing (SAST), dynamic application security testing (DAST), and penetration testing to identify and remediate security vulnerabilities in applications.

### 2. Scope

This procedure applies to all company-developed applications, with specific requirements for those that handle electronic Protected Health Information (ePHI) or data classified as Confidential.

### 3. Overview

This procedure outlines the required security testing for applications, including automated SAST and DAST scans integrated into the development lifecycle and annual penetration tests for sensitive applications. It covers the process from testing and triaging findings to tracking remediation.

### 4. Procedure

#### 4.1 Static Application Security Testing (SAST)

| **Step** | **Who**                      | **What**                                                                                                                              |
| -------- | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **1**    | Developer                    | Integrates SAST tooling into the CI/CD pipeline for automated code analysis on every build or pull request.                           |
| **2**    | Developer                    | Reviews SAST reports for security vulnerabilities, focusing on high and critical severity findings.                                   |
| **3**    | Developer                    | Triages identified vulnerabilities, creating tickets to track remediation efforts. False positives are documented and suppressed.       |
| **4**    | Development Team             | Remediates vulnerabilities according to their severity and documents the fixes in the corresponding tickets.                           |

#### 4.2 Dynamic Application Security Testing (DAST)

| **Step** | **Who**                      | **What**                                                                                                                              |
| -------- | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **1**    | Security Team / Developer    | Configures and runs DAST scans against applications in a staging or testing environment before production deployment.                   |
| **2**    | Security Team / Developer    | Analyzes DAST scan results to identify runtime vulnerabilities.                                                                       |
| **3**    | Developer                    | Triages, prioritizes, and remediates identified vulnerabilities based on risk.                                                        |

#### 4.3 Penetration Testing

| **Step** | **Who**                      | **What**                                                                                                                              |
| -------- | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **1**    | Security Team                | Engages a qualified third-party vendor to conduct penetration tests at least annually on all applications that handle ePHI or Confidential data. |
| **2**    | Security Team                | Receives the final penetration test report from the vendor.                                                                           |
| **3**    | Security & Development Teams | Review the report findings, develop a remediation plan for identified vulnerabilities, and create tickets to track the required work.   |
| **4**    | Development Team             | Implements the remediation plan and provides evidence of fixes for re-testing and validation.                                         |

### 5. Standards Compliance

| **Procedure Step(s)** | **Standard/Framework**     | **Control Reference**     |
| --------------------- | -------------------------- | ------------------------- |
| **4.1 - 4.3**         | HITRUST CSF v11.2.0       | 07.a - Secure Development Life Cycle |
| **4.1**               | HITRUST CSF v11.2.0       | 07.b - Security Testing in Development |
| **4.2**               | HITRUST CSF v11.2.0       | 07.c - Production Security Testing |
| **4.3**               | HITRUST CSF v11.2.0       | 07.d - Vulnerability Assessment |
| **4.1 - 4.3**         | SOC 2                      | CC7.1, CC8.1              |
| **4.1 - 4.3**         | HIPAA Security Rule        | 45 CFR § 164.308(a)(8)    |

### 6. Artifact(s)

A test report from the relevant security tool (SAST, DAST) or a final penetration test report with a remediation plan.

### 7. Definitions

**DAST (Dynamic Application Security Testing):** A method of testing an application during its running state to find security vulnerabilities.

**ePHI (electronic Protected Health Information):** Any protected health information that is created, stored, transmitted, or received in any electronic format.

**SAST (Static Application Security Testing):** A method of testing an application's source code, bytecode, or binary code to find security vulnerabilities without executing the application.

### 8. Responsibilities

| **Role**           | **Responsibility**                                                                                             |
| ------------------ | -------------------------------------------------------------------------------------------------------------- |
| **Developer**      | Integrates and runs SAST/DAST tools, reviews findings, and remediates vulnerabilities.                           |
| **Security Team**  | Manages the penetration testing program, assists with DAST, and provides guidance on vulnerability remediation.  |
| **Development Team** | Ensures vulnerabilities are triaged and remediated in a timely manner based on risk.                           |
