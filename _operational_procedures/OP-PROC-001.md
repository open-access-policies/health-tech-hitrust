---
title: Cloud-Native Key Management Procedure (OP-PROC-001)
parent: Operational Procedures
nav_order: 1
---

### 1. Purpose

To provide practical steps for implementing and managing cryptographic keys using cloud-native key management services, eliminating the need for dedicated cryptographic security engineers while maintaining HIPAA, HITRUST, and SOC 2 compliance.

### 2. Scope

This procedure applies to cryptographic keys managed through cloud provider key management services (AWS KMS, Azure Key Vault, GCP Cloud KMS) for protecting company and customer data. It applies to Platform Engineers, DevOps Engineers, and the Security Officer responsible for cloud key management configuration.

### 3. Overview

This procedure leverages cloud provider managed key services to automate key lifecycle management while providing the security controls and audit capabilities required for regulatory compliance. The approach eliminates operational complexity while maintaining enterprise-grade security through cloud provider infrastructure.

### 4. Procedure

#### 4.1 Cloud Key Management Service Setup

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Platform Engineer | **AWS KMS Configuration**: Configure AWS Key Management Service for the primary cloud environment. Create customer-managed keys (CMK) for ePHI and sensitive data encryption. Enable automatic key rotation for applicable key types. |
| **2** | Platform Engineer | **Azure Key Vault Setup**: Configure Azure Key Vault for multi-cloud environments or Azure-specific workloads. Create customer-managed keys with appropriate access policies and enable soft-delete protection. |
| **3** | Platform Engineer | **GCP Cloud KMS Setup**: Configure Google Cloud Key Management Service for GCP workloads. Create customer-managed encryption keys (CMEK) with appropriate IAM bindings and enable automatic rotation schedules. |
| **4** | Security Officer | **Key Policy Definition**: Define and approve key usage policies, access controls, and rotation schedules. Ensure policies meet HIPAA and HITRUST requirements for ePHI protection. |

#### 4.2 Automated Key Generation and Management

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Platform Engineer | **Infrastructure as Code (IaC) Implementation**: Define key management resources using Terraform, CloudFormation, or ARM templates. Include key policies, rotation schedules, and access controls in version-controlled infrastructure code. |
| **2** | DevOps Engineer | **Application Integration**: Configure applications to use cloud key management APIs for encryption operations. Implement proper error handling and fallback mechanisms for key management service unavailability. |
| **3** | Platform Engineer | **Cross-Region Key Replication**: Configure key replication across multiple regions for disaster recovery. Ensure replicated keys maintain the same access policies and rotation schedules as primary keys. |
| **4** | DevOps Engineer | **Automated Key Rotation**: Enable and configure automatic key rotation for supported key types. Implement application logic to handle key rotation events without service interruption. |

#### 4.3 Application-Level Encryption Implementation

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Development Team | **Cloud SDK Integration**: Integrate cloud provider SDKs and APIs for encryption operations within applications. Use envelope encryption patterns for large data objects and direct encryption for smaller data elements. |
| **2** | Development Team | **Database Encryption Configuration**: Configure database systems to use cloud-managed transparent data encryption (TDE) with customer-managed keys. Ensure ePHI database fields use appropriate encryption methods. |
| **3** | DevOps Engineer | **Storage Encryption Setup**: Configure cloud storage services (S3, Azure Blob, GCS) to use customer-managed keys for automatic encryption at rest. Enable encryption for all storage tiers including backup and archive storage. |
| **4** | Platform Engineer | **Secret Management Integration**: Configure applications to retrieve encryption keys and secrets from cloud secret management services (AWS Secrets Manager, Azure Key Vault, GCP Secret Manager) rather than embedded credentials. |

#### 4.4 Monitoring and Compliance Automation

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Security Officer | **Audit Logging Configuration**: Enable comprehensive audit logging for all key management operations using cloud provider audit services (CloudTrail, Azure Monitor, Cloud Audit Logs). Configure log retention according to compliance requirements. |
| **2** | Platform Engineer | **Automated Monitoring Setup**: Configure automated monitoring and alerting for key usage anomalies, failed encryption operations, and unauthorized access attempts. Integrate alerts with existing security monitoring systems. |
| **3** | Security Officer | **Compliance Reporting Automation**: Set up automated compliance reporting for key management activities. Generate monthly reports on key usage, rotation status, and access patterns for audit and compliance purposes. |
| **4** | DevOps Engineer | **Performance Monitoring**: Monitor key management service performance and latency impact on applications. Set up automated scaling and failover mechanisms for high-availability key management operations. |

#### 4.5 Key Recovery and Disaster Response

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Platform Engineer | **Backup Key Management**: Configure automated backup of key metadata and access policies to secure storage. Ensure backup procedures include cross-region replication for disaster recovery scenarios. |
| **2** | Security Officer | **Key Recovery Procedures**: Document and test key recovery procedures for disaster scenarios. Ensure recovery procedures can restore key access within **[Timeframe, e.g., 4 hours]** to meet business continuity requirements. |
| **3** | DevOps Engineer | **Emergency Access Procedures**: Configure emergency access procedures for key management services during outages or emergencies. Implement break-glass access controls that maintain audit trails and security controls. |
| **4** | Platform Engineer | **Service Failover Testing**: Conduct quarterly testing of key management service failover and recovery procedures. Document test results and update procedures based on findings. |

#### 4.6 Cost Optimization and Management

| **Step** | **Who** | **What** |
| -------- | ------- | -------- |
| **1** | Platform Engineer | **Usage Monitoring**: Monitor key management service usage and costs through cloud billing and cost management tools. Identify opportunities for cost optimization through efficient key usage patterns. |
| **2** | DevOps Engineer | **Caching Strategies**: Implement appropriate caching strategies for key operations to reduce API call costs while maintaining security. Use data encryption keys (DEK) caching where appropriate for high-volume operations. |
| **3** | Security Officer | **Service Tier Optimization**: Review and optimize key management service tiers and features based on actual usage patterns and security requirements. Eliminate unused or redundant key management features. |
| **4** | Platform Engineer | **Lifecycle Management**: Implement automated lifecycle management for unused or expired keys. Configure automatic key deletion schedules for development and testing environments while preserving production keys according to retention policies. |

### 5. Cloud Provider Specific Implementations

#### 5.1 AWS Key Management Service (KMS)

**Customer-Managed Keys (CMK) Setup:**
- Create CMK for ePHI encryption with appropriate key policies
- Enable automatic key rotation for symmetric keys (annual rotation)
- Configure cross-region key replication for disaster recovery
- Set up key usage monitoring through CloudWatch metrics

**Integration Examples:**
```bash
# Create customer-managed key via AWS CLI
aws kms create-key --description "ePHI Encryption Key" --key-usage ENCRYPT_DECRYPT

# Enable automatic rotation
aws kms enable-key-rotation --key-id [key-id]

# Configure S3 bucket encryption with CMK
aws s3api put-bucket-encryption --bucket [bucket-name] --server-side-encryption-configuration
```

#### 5.2 Azure Key Vault

**Key Vault Configuration:**
- Create Key Vault with soft-delete and purge protection enabled
- Configure customer-managed keys with appropriate access policies
- Enable Key Vault logging and monitoring through Azure Monitor
- Set up automatic key rotation schedules

**Integration Examples:**
```bash
# Create Key Vault and customer-managed key
az keyvault create --name [vault-name] --resource-group [rg-name] --enable-soft-delete --enable-purge-protection

# Create key with automatic rotation
az keyvault key create --vault-name [vault-name] --name [key-name] --size 2048 --kty RSA
```

#### 5.3 Google Cloud Key Management Service

**Cloud KMS Setup:**
- Create key rings and customer-managed encryption keys (CMEK)
- Configure automatic key rotation for supported key types
- Set up IAM bindings for proper access control
- Enable audit logging through Cloud Audit Logs

**Integration Examples:**
```bash
# Create key ring and encryption key
gcloud kms keyrings create [keyring-name] --location [location]
gcloud kms keys create [key-name] --location [location] --keyring [keyring-name] --purpose encryption

# Enable automatic rotation
gcloud kms keys update [key-name] --location [location] --keyring [keyring-name] --rotation-period 8760h
```

### 6. Standards Compliance

This procedure is designed to comply with and support the following industry standards and regulations.

| **Procedure Section** | **Standard/Framework** | **Control Reference** |
| --------------------- | ---------------------- | --------------------- |
| **4.1, 4.2** | HITRUST CSF v11.2.0 | 01.k - Cryptographic Key Management |
| **4.4** | HITRUST CSF v11.2.0 | 12.c - Audit Logging and Monitoring |
| **4.3** | HITRUST CSF v11.2.0 | 01.c - Encryption Implementation |
| **All** | SOC 2 Trust Services Criteria | CC6.1 - Logical Access Security |
| **4.4** | SOC 2 Trust Services Criteria | CC6.8 - Data Encryption |
| **4.1-4.6** | HIPAA Security Rule | 45 CFR § 164.312(a)(2)(iv) - Encryption |
| **4.1-4.6** | HIPAA Security Rule | 45 CFR § 164.312(e)(2)(ii) - Encryption of ePHI |
| **4.5** | NIST Cybersecurity Framework | PR.DS-1 - Data-at-rest Protection |
| **4.4** | NIST Cybersecurity Framework | DE.AE-3 - Event Data Analysis |

### 7. Artifact(s)

- Cloud provider audit logs for all key management operations
- Infrastructure as Code (IaC) templates for key management configuration
- Monthly compliance reports on key usage and rotation status
- Automated monitoring dashboards for key management services
- Emergency access procedures and break-glass documentation

### 8. Definitions

**Customer-Managed Encryption Key (CMEK):** Encryption key created and managed by the customer using cloud provider key management services, providing control over key lifecycle while leveraging cloud infrastructure.

**Envelope Encryption:** Encryption method where data is encrypted with a data encryption key (DEK), and the DEK is encrypted with a key encryption key (KEK) managed by cloud services.

**Infrastructure as Code (IaC):** Practice of managing infrastructure through code and automation, enabling version control and repeatable deployments of key management configurations.

**Key Rotation:** Automated process of replacing encryption keys with new keys on a scheduled basis to maintain security while preserving access to encrypted data.

**Cloud-Native Key Management:** Key management approach that leverages cloud provider managed services rather than on-premises hardware security modules or custom key management systems.

### 9. Responsibilities

| **Role** | **Responsibility** |
| -------- | ---------------- |
| **Security Officer** | Define key management policies, approve cloud key configurations, oversee compliance monitoring, and coordinate key recovery procedures. |
| **Platform Engineer** | Configure and maintain cloud key management services, implement infrastructure as code for key management, and manage cross-region key replication. |
| **DevOps Engineer** | Integrate key management into CI/CD pipelines, monitor service performance, implement automated key rotation, and optimize costs. |
| **Development Team** | Implement application-level encryption using cloud key management APIs, handle key rotation events in application code, and follow secure coding practices. |
| **IT Operations** | Monitor key management service availability, coordinate disaster recovery testing, manage emergency access procedures, and support incident response. |

### 10. Related Procedures

This procedure shall be implemented in conjunction with the following organizational procedures:

- **Encryption and Key Management Policy (OP-POL-001)**: Provides policy framework for cloud-native encryption implementation
- **Cloud Infrastructure Security Procedure (ENG-PROC-005)**: Covers broader cloud security configuration including key management integration
- **Disaster Recovery Procedure (RES-PROC-006)**: Addresses key recovery and business continuity requirements
- **Security Monitoring Procedure (SEC-PROC-010)**: Covers monitoring and alerting for key management operations
