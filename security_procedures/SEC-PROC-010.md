# Business Associate Agreement Management Procedure (SEC-PROC-010)

### 1. Purpose

To establish the process for reviewing, executing, monitoring, and maintaining Business Associate Agreements (BAAs) with Covered Entity customers and subcontractors. As a Business Associate processing electronic Protected Health Information (ePHI) on behalf of Covered Entities, **[Company Name]** shall maintain comprehensive BAA management to ensure HIPAA compliance and meet customer contractual obligations.

### 2. Scope

This procedure applies to all BAAs between **[Company Name]** and its Covered Entity customers, as well as BAAs with subcontractors and third parties that access, process, store, or transmit ePHI on behalf of **[Company Name]** or its customers.

### 3. Overview

This procedure outlines the steps for BAA lifecycle management including initial review and execution, ongoing compliance monitoring, amendment processing, subcontractor flow-down requirements, and customer offboarding with data return or destruction. The procedure ensures that all ePHI processing activities are governed by appropriate agreements and that compliance obligations are tracked and fulfilled.

### 4. Procedure

#### 4.1 BAA Review and Execution

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Customer Success/Sales | Initiates BAA request when customer requires ePHI processing services. Documents the scope of ePHI access and processing requirements. |
| **2** | Legal Team | Reviews customer-provided BAA or prepares **[Company Name]** standard BAA template. Identifies non-standard terms requiring security or compliance review. |
| **3** | Security Officer | Reviews BAA security requirements and confirms **[Company Name]** can meet all technical and administrative safeguards required. |
| **4** | Privacy Officer | Reviews privacy provisions including permitted uses, disclosures, and data subject rights requirements. |
| **5** | Legal Team | Negotiates any required modifications with customer legal team. Documents all agreed-upon terms and amendments. |
| **6** | Executive Leadership | Approves final BAA terms for agreements with non-standard provisions or significant liability exposure. |
| **7** | Legal Team | Executes BAA and maintains signed copy in the BAA register. Notifies relevant teams of execution and effective date. |
| **8** | Compliance Team | Creates compliance tracking entry for the BAA including key obligations, reporting requirements, and renewal dates. |

#### 4.2 BAA Compliance Monitoring

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Compliance Team | Maintains BAA register with all active agreements, key terms, and compliance obligations. |
| **2** | Security Officer | Conducts quarterly review of security controls against BAA requirements. Documents any gaps and remediation plans. |
| **3** | Privacy Officer | Reviews data handling practices against BAA-specified permitted uses and disclosures at least annually. |
| **4** | Operations Team | Ensures operational procedures align with BAA service level commitments and reporting requirements. |
| **5** | Compliance Team | Tracks and coordinates required compliance reports, attestations, and audit responses per BAA terms. |
| **6** | Security Officer | Coordinates incident response and breach notification per BAA-specified timelines when incidents occur. |

#### 4.3 Subcontractor Flow-Down Requirements

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Security Officer | Identifies subcontractors requiring BAAs based on ePHI access or processing activities. |
| **2** | Legal Team | Prepares subcontractor BAA ensuring terms mirror or exceed protections in applicable customer BAAs. |
| **3** | Security Team | Conducts security assessment of subcontractor per SEC-PROC-005 with enhanced focus on ePHI handling. |
| **4** | Privacy Officer | Reviews subcontractor data handling practices and privacy controls for BAA compliance. |
| **5** | Legal Team | Executes subcontractor BAA and documents relationship in subcontractor register. |
| **6** | Customer Success | Notifies applicable Covered Entity customers of subcontractor engagement as required by their BAAs. |
| **7** | Compliance Team | Adds subcontractor to compliance monitoring program with appropriate review cadence. |

#### 4.4 BAA Amendment Process

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Customer Success/Legal | Identifies need for BAA amendment due to scope changes, service modifications, or regulatory updates. |
| **2** | Legal Team | Drafts amendment language and reviews impact on existing obligations and security requirements. |
| **3** | Security Officer | Reviews amended terms for security control implications and confirms continued compliance capability. |
| **4** | Legal Team | Negotiates and executes amendment. Updates BAA register with amended terms and effective date. |
| **5** | Compliance Team | Updates compliance tracking to reflect amended obligations and any new reporting requirements. |
| **6** | Operations Team | Implements any operational changes required by amended BAA terms. |

#### 4.5 Customer Offboarding and Data Return/Destruction

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Customer Success | Initiates offboarding process when BAA terminates or customer requests service discontinuation. |
| **2** | Legal Team | Reviews BAA data return and destruction requirements. Documents customer's elected option (return vs. destruction). |
| **3** | Data Engineering | Identifies all locations containing customer ePHI including primary stores, backups, caches, and logs. |
| **4** | Operations Team | Executes data export in customer-requested format if data return is selected. Securely transmits data to customer. |
| **5** | Data Engineering | Performs data destruction per NIST SP 800-88 guidelines if destruction is selected. Documents destruction method and verification. |
| **6** | Security Officer | Verifies completeness of data return or destruction across all identified data locations. |
| **7** | Legal Team | Prepares and provides certificate of data return or destruction to customer. |
| **8** | IT Operations | Revokes all customer access credentials, API keys, and integration configurations. |
| **9** | Compliance Team | Archives BAA and compliance records according to retention requirements. Updates BAA register to reflect terminated status. |

### 5. Standards Compliance

| **Procedure Section** | **Standard/Framework** | **Control Reference** |
| --------------------- | ---------------------- | --------------------- |
| **4.1** | HIPAA Security Rule | 45 CFR § 164.314(a)(1) - Business Associate Contracts |
| **4.1** | HIPAA Security Rule | 45 CFR § 164.314(a)(2) - Business Associate Safeguards |
| **4.3** | HIPAA Security Rule | 45 CFR § 164.314(a)(2)(i) - Subcontractor Requirements |
| **4.5** | HIPAA Security Rule | 45 CFR § 164.310(d)(2) - Disposal |
| **All** | HITRUST CSF v11.2.0 | 14.c - Third Party Service Agreements |
| **All** | SOC 2 Trust Services Criteria | CC9.3 - Vendor Agreements |

### 6. Artifact(s)

- Executed Business Associate Agreement
- BAA Register (inventory of all active and terminated BAAs)
- Subcontractor Register (inventory of subcontractors with BAAs)
- BAA Compliance Tracking Log
- Data Return/Destruction Certificate
- Customer Notification Records (for subcontractor disclosures)

### 7. Definitions

See [Annex: Glossary](../annexes/glossary.md)

### 8. Responsibilities

| **Role** | **Responsibility** |
| -------- | ------------------ |
| **Legal Team** | Drafts, reviews, negotiates, and executes BAAs. Maintains BAA register and provides certificates of data return/destruction. |
| **Security Officer** | Reviews BAA security requirements, monitors compliance with security obligations, coordinates incident response and breach notification. |
| **Privacy Officer** | Reviews privacy provisions, monitors data handling compliance, coordinates data subject request responses. |
| **Compliance Team** | Maintains compliance tracking, coordinates audits and attestations, archives records per retention requirements. |
| **Customer Success** | Initiates BAA requests, coordinates customer communications, manages onboarding and offboarding processes. |
| **Data Engineering** | Identifies ePHI locations, executes data exports and destruction, verifies data handling compliance. |
| **Operations Team** | Implements operational procedures per BAA terms, maintains service level compliance, supports data return processes. |
| **Executive Leadership** | Approves non-standard BAA terms and significant liability exposure. |
