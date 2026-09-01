# Microsoft IAM, Security & Endpoint Lab

A hands-on Microsoft cloud security portfolio focused on **Identity and Access Management (IAM)** using Microsoft Entra ID.

This repository documents practical labs I have built to develop real-world skills in identity administration, authentication, authorization, application identity, Microsoft Graph and security.

The environment is designed to simulate common identity and access scenarios that an **Identity & Access Administrator, IAM Analyst, Cloud Administrator or IT Security professional** may encounter.

---

## 🎯 Objectives

The purpose of this lab environment is to develop and demonstrate practical experience with Microsoft identity and security technologies rather than relying solely on theoretical certification knowledge.

Current areas covered include:

- Microsoft Entra ID
- Identity and Access Management (IAM)
- User and Group Administration
- Role-Based Access Control (RBAC)
- Least Privilege
- Multi-Factor Authentication (MFA)
- Microsoft Authenticator
- Enterprise Applications
- App Registrations
- Application Roles
- Microsoft Graph
- API Permissions
- OAuth 2.0
- Client Credentials Flow
- PowerShell
- Application / Workload Identity

---

# 🧪 Completed Projects

## Project 1 – Microsoft Entra ID User & Group Management

📁 [`01-entra-user-group-management`](01-entra-user-group-management)

Built a test identity environment and performed core Microsoft Entra ID user and group administration.

### Hands-On Tasks

- Created and managed test user accounts
- Configured user profile information
- Created security groups
- Added and managed group membership
- Practised identity administration within Microsoft Entra ID
- Documented configuration with lab evidence

### Skills

`Microsoft Entra ID` `IAM` `User Management` `Group Management` `Identity Administration`

---

## Project 2 – Microsoft Entra ID RBAC & Least Privilege

📁 [`02-entra-rbac-least-privilege`](02-entra-rbac-least-privilege)

Implemented role-based administrative access using Microsoft Entra ID built-in roles.

### Hands-On Tasks

- Reviewed Microsoft Entra administrative roles
- Assigned administrative permissions to test identities
- Implemented least-privilege access
- Verified role assignments
- Reviewed administrative access and role configuration

### Skills

`RBAC` `Least Privilege` `Entra Roles` `IAM` `Access Control`

---

## Project 3 – Microsoft Entra ID MFA & Microsoft Authenticator

📁 [`03-entra-id-mfa-authenticator`](03-entra-id-mfa-authenticator)

Configured and tested Multi-Factor Authentication using Microsoft Authenticator and Microsoft Entra ID Security Defaults.

### Hands-On Tasks

- Enabled and reviewed Security Defaults
- Configured Microsoft Authenticator as an authentication method
- Registered MFA for a test identity
- Tested Microsoft Authenticator number matching
- Verified successful MFA authentication
- Reviewed Entra ID sign-in logs and authentication details
- Troubleshot authentication and password-related sign-in issues

### Skills

`MFA` `Microsoft Authenticator` `Security Defaults` `Authentication` `Sign-in Logs` `Entra ID`

---

## Project 4 – Microsoft Entra ID Application Identity, OAuth 2.0 & Microsoft Graph

📁 [`04-entra-enterprise-application-access`](04-entra-enterprise-application-access)

Built and tested an application identity using Microsoft Entra ID, progressing from App Registration and application roles to OAuth 2.0 app-only authentication and Microsoft Graph API access.

### Hands-On Tasks

- Created the **Falcon Tech Employee Portal** App Registration
- Configured a single-tenant application
- Assigned application ownership
- Configured a web redirect URI
- Created and managed a client credential
- Configured Microsoft Graph delegated permissions
- Added the `User.Read.All` Application permission
- Granted administrator consent
- Created custom application roles
- Assigned Employee and Portal Administrator roles to test identities
- Used OAuth 2.0 Client Credentials Flow
- Authenticated the application using PowerShell
- Obtained a Bearer access token from Microsoft Entra ID
- Queried Microsoft Graph using app-only authentication
- Successfully retrieved directory user data through Microsoft Graph
- Revoked and rotated an exposed test credential
- Protected secrets and access tokens from the public repository

### Skills

`App Registrations` `Enterprise Applications` `Service Principals` `Application Roles` `Microsoft Graph` `OAuth 2.0` `Client Credentials` `API Permissions` `Admin Consent` `PowerShell` `Workload Identity`

---

# 🔐 Security Concepts Demonstrated

Across the projects, the lab demonstrates practical understanding of:

- Authentication vs Authorization
- Identity Lifecycle Administration
- Role-Based Access Control
- Least-Privilege Access
- Multi-Factor Authentication
- Application Identity
- Human Identity vs Workload Identity
- Delegated vs Application Permissions
- Administrator Consent
- OAuth 2.0
- Bearer Access Tokens
- Client Credential Protection
- Credential Rotation
- Microsoft Graph Authorization
- Security Auditing

---

# 🛠 Technologies Used

| Technology | Practical Use |
|---|---|
| Microsoft Entra ID | Identity and access administration |
| Microsoft Authenticator | Multi-factor authentication |
| Microsoft Graph | Microsoft cloud API access |
| PowerShell | OAuth and Graph testing |
| OAuth 2.0 | Application authentication |
| Entra App Registrations | Application identity configuration |
| Enterprise Applications | Service principal and application access |
| GitHub | Lab documentation and portfolio evidence |

---

# 📈 Portfolio Progress

| Project | Area | Status |
|---|---|---|
| 01 | User & Group Management | ✅ Complete |
| 02 | RBAC & Least Privilege | ✅ Complete |
| 03 | MFA & Microsoft Authenticator | ✅ Complete |
| 04 | Application Identity, OAuth & Microsoft Graph | ✅ Complete |

---

# 🚀 Next Steps

This repository will continue to expand with additional Microsoft identity, security and endpoint-management labs.

Planned areas include:

- Conditional Access
- Privileged Identity Management (PIM)
- Identity Governance
- Access Reviews
- Lifecycle Workflows
- Microsoft Intune
- Endpoint Security
- Microsoft Defender
- Additional Microsoft Graph automation

---

## About This Repository

This repository is a personal hands-on learning environment built to complement my Microsoft certification studies and professional IT experience.

All users, applications and scenarios used in the labs are test identities and fictional business scenarios created for learning purposes.

Sensitive credentials, client secrets and access tokens are not intentionally stored within the repository.
