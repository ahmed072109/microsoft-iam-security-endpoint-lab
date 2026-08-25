# Project 01 - Microsoft Entra User & Group Management

## Overview

This project demonstrates the implementation of user and group management within Microsoft Entra ID for a simulated organisation.

The lab forms part of my wider Microsoft IAM, Security & Endpoint portfolio and focuses on developing practical Identity and Access Management (IAM) administration skills.

## Scenario

Falcon Tech is a simulated organisation with employees across multiple departments.

The organisation requires a structured identity management solution to securely manage employee identities and provide a scalable foundation for controlling access to company resources.

The following departments are represented:

- IT
- Finance
- Human Resources
- Sales
- Management

## Objectives

The objectives of this lab are to:

- Create and manage Microsoft Entra user identities
- Configure user attributes such as department and job title
- Create departmental security groups
- Assign users to appropriate security groups
- Understand group-based access management
- Review user identity properties
- Review sign-in and audit information
- Apply IAM administration best practices

## Environment

- Microsoft Entra ID
- Microsoft Entra Admin Center
- Microsoft Entra Free
- GitHub for project documentation

## Implementation

### 1. User Creation

Five test users will be created to represent employees from different departments within Falcon Tech.

| User | Department | Job Title |
|---|---|---|
| Adam Wilson | IT | IT Support Engineer |
| Sarah Khan | Finance | Finance Analyst |
| James Smith | HR | HR Specialist |
| Emma Taylor | Sales | Sales Executive |
| David Brown | Management | Operations Manager |

User attributes such as department and job title will be configured to provide structured identity information.

### 2. Security Group Creation

Departmental security groups will be created to provide a scalable method of managing access.

The following security groups will be configured:

- SG-IT
- SG-Finance
- SG-HR
- SG-Sales
- SG-Management

### 3. Group Membership

Each employee will be assigned to the security group corresponding to their department.

This demonstrates the principle of managing access through groups rather than assigning permissions individually to every user.

## IAM Concepts Demonstrated

This project demonstrates several fundamental IAM concepts:

- Identity lifecycle management
- User provisioning
- Group-based access management
- Security groups
- User attributes
- Role-Based Access Control foundations
- Principle of least privilege
- Centralised identity administration

## Screenshots

Screenshots demonstrating the implementation will be added as the lab progresses.

Sensitive information including passwords, tenant IDs, subscription IDs, authentication tokens and personal account information will not be published.

## Key Learnings

This section will be updated after completing the lab to document the practical skills, challenges and IAM concepts learned during implementation.

## Next Steps

Following completion of this project, the lab environment will be expanded to include:

- Role-Based Access Control (RBAC)
- Least Privilege Administration
- Multi-Factor Authentication (MFA)
- Self-Service Password Reset (SSPR)
- Conditional Access
- Privileged Identity Management (PIM)
- Identity Governance
- Microsoft Intune
- Endpoint Security
- Microsoft Defender
- Zero Trust access controls

- 
- Endpoint Security
- Microsoft Defender
- Zero Trust access controls
