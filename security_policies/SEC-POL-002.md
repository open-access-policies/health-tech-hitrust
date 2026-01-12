---
title: Password Policy (SEC-POL-002)
parent: Security Policies
nav_order: 2
---
### 1. Objective

The objective of this policy is to establish and enforce minimum standards for the creation, management, and protection of passwords. Strong password management is a critical control for safeguarding the confidentiality, integrity, and availability of **[Company Name]**'s information assets, particularly electronic Protected Health Information (ePHI), and for preventing unauthorized access to systems and data.

### 2. Scope

This policy applies to all **[Company Name]** workforce members (including employees, contractors, and temporary staff) and any third party that requires access to corporate systems, applications, network devices, and data. It governs all passwords used to access company resources, whether managed internally or by external service providers.

### 3. Policy

All systems and applications must be configured to enforce the following password parameters. Exceptions must be formally documented and approved by the Security Officer through the risk management process.

#### 3.1 Password Construction Requirements

To ensure passwords are resistant to common attack vectors, all user-created passwords must adhere to the following complexity standards:

- **Length:** The minimum acceptable length for any password is twelve (12) characters. For accounts with elevated privileges (e.g., system administrators), the minimum length is sixteen (16) characters.
    
- **Complexity:** Passwords must contain characters from at least three (3) of the following four categories:
    
    - Uppercase letters (A-Z)
        
    - Lowercase letters (a-z)
        
    - Numbers (0-9)
        
    - Special characters (e.g., `!@#$%^&*()`)
        
- **Prohibited Content:** Passwords must not contain common or easily guessable information. Systems shall be configured to check new passwords against a blocklist of common passwords and previously breached credentials. This includes, but is not limited to:
    
    - Company names (e.g., `[Company Name]`) or variations.
        
    - Usernames, personal names, family names, or pet names.
        
    - Dictionary words or common keyboard patterns (e.g., "password", "qwerty").
        
    - Consecutive or repeating characters (e.g., "111111", "abcdefg").
        

#### 3.2 Password Lifecycle Management

Passwords must be actively managed throughout their lifecycle to limit the window of opportunity should a credential be compromised.

- **Password Age:** All user passwords must be changed at least every **[Number, e.g., 90]** days. This requirement may be waived for specific systems where strong MFA is enforced and breached password screening is active, subject to a documented risk assessment approved by the Security Officer.
    
- **Password History:** Systems must be configured to prevent the reuse of the previous **[Number, e.g., 5]** passwords for a given account.
    
- **Account Lockout:** User accounts must be automatically locked for a minimum of **[Duration, e.g., 30 minutes]** after **[Number, e.g., 5]** consecutive failed login attempts. The lockout must only be reversible by an authorized administrator or after the lockout duration has expired.
    

#### 3.3 Multi-Factor Authentication (MFA)

MFA is required to provide an additional layer of security and shall be enforced for all workforce members across all company systems where the feature is supported.

- MFA must be enabled for all remote access to the corporate network (e.g., VPN).
    
- MFA is mandatory for accessing any system, application, or service that stores, processes, or transmits data classified as Confidential or Restricted, including ePHI.
    
- Approved MFA methods include authenticator applications (TOTP), hardware tokens, or biometric identifiers. SMS-based MFA is prohibited for accessing systems containing Restricted data.
    

#### 3.4 Password Protection and Storage

Workforce members are responsible for the protection of their credentials.

- Passwords must never be written down, stored in plain text files, or shared with any other individual, including managers or IT staff. Passwords must not be transmitted via insecure channels such as email or instant messaging.
    
- The use of a company-approved and encrypted password manager is strongly encouraged for managing credentials.
    
- Systems must store passwords in a secure, salted, and hashed format using a strong, industry-recognized cryptographic algorithm (e.g., bcrypt, Argon2).
    

#### 3.5 Initial Password Management and Resets

The process for establishing and resetting passwords must be secure.

- All new user accounts must be assigned a randomly generated, single-use temporary password.
    
- Users must be required to change their temporary password upon their first login.
    
- The identity of a user requesting a password reset must be verified by an authorized administrator through a secure, pre-defined process before the reset is performed.
    

#### 3.6 System and Service Accounts

Non-interactive accounts (e.g., service accounts, API keys) must be securely managed.

- Service account credentials must be unique to that service and must not be shared between systems.
    
- Default vendor-supplied passwords for any application or device must be changed before the system is connected to the production network.
    
- Service account passwords must be rotated at least annually or immediately upon the departure of any workforce member who had access to them.
    

### 4. Standards Compliance

See [Annex: Control Mapping](../_annexes/control_mapping.md)

### 5. Definitions

See [Annex: Glossary](../_annexes/glossary.md)

### 6. Responsibilities

|**Role**|**Responsibility**|
|---|---|
|**Security Officer / Team**|Own, review, and update this policy annually. Monitor for compliance and report on password-related security metrics.|
|**IT Department**|Implement and maintain the technical controls required to enforce this policy across all systems and applications. Manage the password reset process.|
|**All Workforce Members**|Adhere to this policy for all company-related accounts. Protect their credentials and immediately report any suspected compromise.|