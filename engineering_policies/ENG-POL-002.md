---
title: Change Control Policy (ENG-POL-002)
parent: Engineering Policies
nav_order: 2
---

### 1. Objective

The objective of this policy is to establish a formal process for managing all changes to **[Company Name]**'s production systems, applications, and infrastructure. This policy ensures that all modifications are properly authorized, tested, documented, and reviewed to maintain system stability, security, and integrity, thereby protecting sensitive data, including electronic Protected Health Information (ePHI).

### 2. Scope

This policy applies to all workforce members involved in the development, testing, approval, and deployment of changes to any production environment. This includes all applications, source code, infrastructure-as-code configurations, and databases that support **[Company Name]**'s services.

### 3. Policy

All changes to the production environment shall adhere to a structured and auditable lifecycle, from initiation to deployment and post-implementation review. GitHub is the designated system of record for tracking all code and configuration changes.

#### 3.1 Standard Change Process

All non-emergency changes shall follow this standard process:

- **Initiation:** Every change shall begin with a ticket in the company's issue tracking system, which shall detail the business justification and technical requirements.
    
- **Development:** All code and configuration changes shall be developed in a separate feature branch within the designated GitHub repository.
    
- **Peer Code Review:** Before a change can be promoted for testing, it shall be submitted as a pull request in GitHub and shall receive a formal, documented approval from at least one other qualified engineer who was not an author of the change. A qualified reviewer shall be defined as an engineer with equivalent or greater seniority or subject-matter expertise. The review shall assess code quality, functionality, and adherence to secure coding standards.
    
- **Security Review:** All pull request templates shall include a mandatory security checklist. If the developer indicates the change touches sensitive data, authentication, authorization, encryption, ePHI, or external integrations, a security review shall be required and shall be completed by the Security Officer or designated security team member before merging. For low-risk changes (documentation, minor UI updates, configuration updates with no security implications), the security checklist shall be completed by the developer without additional review.
    
- **Testing:** All changes shall pass a full suite of automated tests. Evidence of successful test runs (e.g., a link to the CI/CD build results) shall be included in the pull request. Quality Assurance (QA) involvement shall be risk-based: **High-risk changes** (new features, database schema changes, authentication/authorization modifications, ePHI handling) shall require formal QA sign-off. **Medium-risk changes** (bug fixes, configuration updates, UI improvements) shall require QA review only if the change affects user-facing functionality. **Low-risk changes** (documentation, internal tooling, minor refactoring) shall not require QA sign-off but shall pass automated testing.
    
- **Deployment Approval:** Final approval to merge the change into the production release branch shall be granted by authorized personnel (e.g., Engineering Lead or Manager) within the GitHub pull request. This approval shall signify that the approver has verified that all required steps, including peer review, security review, and QA sign-off, have been successfully completed and documented. All approved production release branches shall be tagged to ensure traceability and that the exact code deployed to production can be identified.
    

#### 3.2 Emergency Changes

An emergency change is defined as a modification required to resolve a critical production outage, a severe service degradation, or to patch a critical security vulnerability that requires immediate remediation.

- **Authorization:** An emergency change shall require documented approval from at least one Engineering Lead or the CTO. For security-related emergency changes, the Security Officer shall be notified immediately, but approval may proceed without waiting for Security Officer availability to prevent business disruption.
    
- **Expedited Review:** Peer code review shall remain mandatory but may be expedited. For critical outages, the review shall be performed during or immediately after deployment to restore service quickly. Security review requirements shall follow the same risk-based approach as standard changes but with expedited timelines.
    
- **Post-Implementation Review:** All emergency changes shall be followed by a formal post-implementation review within **[Number, e.g., 5]** business days (extended from 3 days to allow for proper analysis). This review shall analyze the root cause, validate the emergency response, and identify opportunities for process improvement. The standard change documentation shall be completed retroactively within **[Number, e.g., 2]** business days.
    
- **Oversight:** A log of all emergency changes shall be maintained and reviewed on a quarterly basis by Engineering Management to identify trends and ensure the emergency process is not being misused to bypass standard change controls.
    

#### 3.3 Data-Only Changes

Data-only changes, such as manual database updates that are not part of a standard code release, shall follow a streamlined but secure process appropriate for a growing organization.

- **Formal Request:** All data-only changes shall require a formal request ticket that includes the script to be run, the business justification, the expected impact, and a rollback plan. For routine operational changes (e.g., updating configuration values, correcting data entry errors), a simplified approval process may be used.
    
- **Risk-Based Approval:** **High-risk changes** affecting ePHI, financial data, or critical business operations shall require approval from both the data/system owner and the Security Officer. **Medium-risk changes** affecting operational data shall require approval from the data/system owner only. **Low-risk changes** (configuration updates, non-sensitive data corrections) shall require approval from the requesting team lead.
    
- **Execution:** Changes shall be executed using approved, peer-reviewed scripts by authorized personnel with privileged database access. For routine changes, a qualified Database Administrator or DevOps Engineer may execute the change. The execution output shall be captured and appended to the original request ticket. Direct production database access for developers shall be prohibited except for emergency troubleshooting under supervision.
    

#### 3.4 Change Documentation and Tracking

- **System of Record:** GitHub pull requests shall serve as the auditable record for all code and configuration changes.
    
- **Traceability:** Every pull request shall be linked to its corresponding issue tracking ticket. The pull request description shall summarize the change, the testing performed, and the outcome of all required reviews. Approvals shall be captured via the native review and approval features within GitHub.
    
- **Technical Enforcement:** The `main` and any `production` or `release` branches in all repositories within the scope of this policy shall be technically protected to prevent direct commits. All changes shall be enforced through the pull request workflow.

- **Pull Request Template:** All pull requests shall use a standardized template that includes sections for the change description, testing performed, security checklist, and links to related tickets. This template shall be enforced via GitHub repository settings.
    

#### 3.5 Change Notifications

- **Internal Notification:** The engineering team shall notify relevant internal stakeholders (e.g., Customer Support, Operations) of all upcoming production deployments via designated communication channels (e.g., Slack, email).
    
- **External Notification:** For changes that will have a noticeable impact on customers or partners, the Product Management team shall be responsible for providing advance notification with sufficient lead time.
    

#### 3.6 Branch Protection

To enforce the change control process described in this policy, all `main`, `production`, and `release` branches in repositories within the scope of this policy shall have GitHub branch protection rules configured. At a minimum, these rules shall be enabled to:

- **Require a pull request before merging:** Direct pushes to protected branches shall be disabled. All changes shall be made via a pull request.
- **Require approvals:** The peer review and deployment approval requirements outlined in section 3.1 shall be enforced.
- **Require status checks to pass before merging:** All required CI/CD checks (e.g., automated tests, security scans) shall pass successfully before a change can be merged.

### 4. Standards Compliance

See [Annex: Control Mapping](../_annexes/control_mapping.md)

### 5. Definitions

See [Annex: Glossary](../_annexes/glossary.md)

### 6. Responsibilities

| **Role**                        | **Responsibility**                                                                                                 |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Engineering Team**            | Changes shall be developed, tested, and documented in accordance with this policy. Peer code reviews shall be conducted.                     |
| **Security Team**               | Changes shall be reviewed for security implications and approved or rejected based on risk assessment.                                 |
| **Quality Assurance (QA) Team** | Changes shall be verified to meet functional requirements and not introduce defects. Formal testing sign-off shall be provided.    |
| **Engineering Management**      | Final approval for changes to be deployed to production shall be provided. Emergency changes shall be authorized.                      |
| **System / Data Owners**        | Approval for changes affecting their specific systems or data domains shall be provided, particularly for Data-Only Changes. |