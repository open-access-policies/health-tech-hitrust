# Secure Media Disposal and Sanitization Procedure (OP-PROC-004)

### 1. Purpose

To provide step-by-step instructions for securely destroying or sanitizing different types of electronic media and physical documents to prevent the unauthorized disclosure of sensitive information.

### 2. Scope

This procedure applies to all company-owned and managed media, both electronic and physical, that contains company or customer data. This includes, but is not limited to, hard drives, solid-state drives (SSDs), USB drives, backup tapes, mobile devices, and paper documents.

### 3. Overview

This procedure outlines the mandated methods for disposing of or sanitizing media based on the classification level of the data it contains. It ensures that all sensitive information is rendered unrecoverable, in compliance with regulatory and industry standards.

### 4. Procedure

#### 4.1 Electronic Media (Hard Drives, SSDs)

| **Step** | **Who**                      | **What**                                                                                                                                                              |
| -------- | ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1**    | Asset Custodian / IT Team    | Identify media that is at the end of its lifecycle or is being decommissioned.                                                                                        |
| **2**    | IT Team                      | For media containing **Confidential** or **Restricted** data, perform cryptographic erasure according to NIST SP 800-88 guidelines.                                     |
| **3**    | IT Team                      | For media that cannot be cryptographically erased, or for media containing the most sensitive **Restricted** data, physically destroy the media (e.g., shredding, degaussing). |
| **4**    | IT Team                      | Document the disposal method, date, and personnel involved in the asset management system. If a third-party vendor is used, obtain and file a certificate of destruction. |

#### 4.2 Paper Documents

| **Step** | **Who**                      | **What**                                                                                                                                                              |
| -------- | ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1**    | All Employees                | Identify paper documents containing **Confidential** or **Restricted** information that are no longer required.                                                           |
| **2**    | All Employees                | Place documents in designated secure shredding bins provided throughout the office.                                                                                   |
| **3**    | Approved Disposal Vendor     | The approved vendor collects the contents of the shredding bins on a scheduled basis for secure, off-site destruction.                                                |
| **4**    | Facilities / IT Team         | Obtain and file the certificate of destruction provided by the vendor.                                                                                                |

### 5. Standards Compliance

See [Annex: Control Mapping](../_annexes/control_mapping.md)

### 6. Artifact(s)

A completed disposal record in the asset management system or a certificate of destruction from a third-party vendor.

### 7. Definitions

See [Annex: Glossary](../_annexes/glossary.md)

### 8. Responsibilities

| **Role**                 | **Responsibility**                                                                                             |
| ------------------------ | -------------------------------------------------------------------------------------------------------------- |
| **IT Team**              | Responsible for the secure sanitization and destruction of electronic media and for managing disposal vendors. |
| **All Employees**        | Responsible for properly disposing of sensitive paper documents in the provided secure shred bins.             |
| **Approved Disposal Vendor** | Responsible for the secure collection and destruction of media and providing certificates of destruction.    |
