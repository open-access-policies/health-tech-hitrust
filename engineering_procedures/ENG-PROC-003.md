# Standard Change Management Procedure (ENG-PROC-003)

### 1. Purpose

The purpose of this procedure is to detail the end-to-end process for a standard, non-emergency change to a production application or its configuration, ensuring that all changes are properly developed, tested, reviewed, and approved.

### 2. Scope

This procedure applies to all standard, non-emergency changes to production applications, infrastructure, and related system configurations.

### 3. Overview

This procedure outlines the standard workflow for managing changes. It begins with a developer creating a ticket and a feature branch, followed by code development, a peer and security review via a pull request, QA testing, and final approval from an Engineering Lead before being merged for deployment.

### 4. Procedure

| **Step** | **Who**                      | **What**                                                                                                                            |
| -------- | ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **1**    | Developer                    | Creates an issue ticket in the tracking system to document the planned change and creates a new feature branch in the source code repository. |
| **2**    | Developer                    | Submits a pull request when development is complete, filling out the required pull request template, including a security checklist.      |
| **3**    | Peer Reviewer                | A qualified peer reviews the code for correctness, quality, and adherence to coding standards, and provides approval on the pull request. |
| **4**    | Security Team                | Reviews the pull request for any security implications. Approval is required for changes impacting security controls or sensitive data. |
| **5**    | QA Team                      | Tests the changes in a dedicated staging environment to verify functionality and ensure no regressions are introduced. Provides sign-off. |
| **6**    | Engineering Lead             | Provides the final review and approval to merge the pull request into the main branch, authorizing its deployment to production.      |

### 5. Standards Compliance

See [Annex: Control Mapping](../_annexes/control_mapping.md)

### 7. Definitions

See [Annex: Glossary](../_annexes/glossary.md)

### 8. Responsibilities

| **Role**           | **Responsibility**                                                              |
| ------------------ | ------------------------------------------------------------------------------- |
| **Developer**      | Implements the change, creates the pull request, and responds to feedback.      |
| **Peer Reviewer**  | Conducts a thorough review of the code changes.                                 |
| **Security Team**  | Assesses the security impact of the change and provides approval.               |
| **QA Team**        | Validates the functionality and quality of the change before release.           |
| **Engineering Lead** | Provides final authorization for the change to be deployed to production.       |
