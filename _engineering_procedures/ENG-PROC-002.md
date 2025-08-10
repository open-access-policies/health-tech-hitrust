---
title: Third-Party Component Security Review Procedure (ENG-PROC-002)
parent: Engineering Procedures
nav_order: 2
---
### 1. Purpose

The purpose of this procedure is to define the steps for scanning, reviewing, and approving the use of new open-source or commercial software components to minimize security and licensing risks.

### 2. Scope

This procedure applies to all new open-source and commercial third-party software components, libraries, and dependencies being considered for inclusion in company software.

### 3. Overview

This procedure describes the process for managing the security of third-party components. It begins with a developer proposing a new component, followed by automated scanning, a formal review of the results by engineering and security teams, and concludes with a documented approval or denial.

### 4. Procedure

| **Step** | **Who**                      | **What**                                                                                                                                                           |
| -------- | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **1**    | Developer                    | Proposes the use of a new third-party component by creating an issue ticket and documenting the component's purpose and source.                                      |
| **2**    | Developer / CI/CD Pipeline   | Uses automated Software Composition Analysis (SCA) tools to scan the component for known vulnerabilities (CVEs) and potential software license compliance issues.      |
| **3**    | Development Team Lead & Security Team | Review the SCA scan results. They assess the severity of any identified vulnerabilities and the implications of the component's license.                     |
| **4**    | Development Team             | If significant vulnerabilities are found, the team shall create a remediation plan (e.g., wait for a patched version) or formally document a risk acceptance rationale. |
| **5**    | Development Team Lead        | Based on the review and any remediation plan, formally approves or denies the use of the component in the project documentation or ticket.                           |

### 5. Standards Compliance

See [Annex: Control Mapping](../_annexes/control_mapping.md)

### 7. Definitions

See [Annex: Glossary](../_annexes/glossary.md)

### 8. Responsibilities

| **Role**                | **Responsibility**                                                                                             |
| ----------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Developer**           | Proposes new components and initiates the SCA scan.                                                            |
| **Development Team Lead** | Reviews scan results, makes the final decision on component use, and ensures proper documentation.             |
| **Security Team**       | Assists in reviewing SCA scan results, provides guidance on vulnerability risk, and reviews risk acceptance cases. |
