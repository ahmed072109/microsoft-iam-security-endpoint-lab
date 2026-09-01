# Project 4 – Microsoft Entra ID Enterprise Application Access & Microsoft Graph

## Objective

Configure and test enterprise application access in Microsoft Entra ID, progressing from basic user assignment and auditing to application registration, role-based application access, Microsoft Graph permissions, and OAuth 2.0 app-only authentication.

This lab demonstrates how Microsoft Entra ID can be used to manage application identities, control user access, implement application roles, grant API permissions using least privilege, and authenticate an application to Microsoft Graph.

---

## Lab Environment

- Microsoft Entra ID
- Microsoft Entra Admin Center
- Enterprise Applications
- App Registrations
- Microsoft Graph
- PowerShell
- OAuth 2.0
- Test Enterprise Application: Falcon Tech Service Desk
- Test App Registration: Falcon Tech Employee Portal
- Test users created within the lab tenant

---

## Part 1 – Enterprise Application Access Management

I created and configured the **Falcon Tech Service Desk** Enterprise Application in Microsoft Entra ID.

The application was used to demonstrate how Entra ID represents applications through service principals and how administrators can control which identities are assigned access.

### Tasks Completed

- Created a non-gallery Enterprise Application
- Reviewed the Enterprise Application/service principal
- Configured application access properties
- Assigned a test user to the application
- Verified the application assignment against the user account
- Reviewed Microsoft Entra audit logs for application access changes

This demonstrated how Entra ID can centrally manage access to enterprise applications and provide an audit trail of administrative changes.

---

## Part 2 – Falcon Tech Employee Portal App Registration

I created a second application called **Falcon Tech Employee Portal** using Microsoft Entra App Registrations.

The application was configured as a single-tenant application, meaning authentication is restricted to identities within the Falcon Tech lab tenant.

### Configuration

- Registered Falcon Tech Employee Portal in Microsoft Entra ID
- Configured the application as single tenant
- Configured a web redirect URI
- Created application credentials using a client secret
- Assigned an application owner
- Reviewed the relationship between the App Registration and Enterprise Application/service principal

The client secret value was never stored in the GitHub repository.

---

## Part 3 – Application Roles

Custom application roles were created to simulate role-based access to the Falcon Tech Employee Portal.

### Employee

Provides standard employee access to the application.

### Portal Administrator

Provides administrative access to the Falcon Tech Employee Portal.

### Role Assignments

- Adam Wilson → Employee
- David Brown → Portal Administrator

These roles demonstrate how application roles can be assigned through Microsoft Entra ID and included as role claims in authentication tokens.

The application itself would be responsible for reading these claims and enforcing the appropriate authorization.

---

## Part 4 – Microsoft Graph API Permissions

Microsoft Graph permissions were configured for the Falcon Tech Employee Portal.

### Delegated Permissions

- `User.Read`
- `User.ReadBasic.All`

### Application Permission

- `User.Read.All`

The `User.Read.All` application permission requires administrator consent because it allows the application to read user profiles without an interactive user being signed in.

Administrative consent was granted within the lab tenant.

This permission was later validated by performing an app-only Microsoft Graph request.

---

## Part 5 – Client Credential Configuration

A client secret was created for the Falcon Tech Employee Portal.

The credential allows the application to prove its identity to Microsoft Entra ID when requesting an OAuth access token.

The client secret value is treated as a sensitive credential and is not included in this repository.

During testing, an exposed test credential was revoked and rotated, demonstrating appropriate credential management and incident-response practice.

---

## Part 6 – OAuth 2.0 Client Credentials Flow

To test the application identity, I used the **OAuth 2.0 Client Credentials Flow**.

Unlike delegated authentication, this flow does not require a user to interactively sign in.

The application authenticated using:

- Directory (Tenant) ID
- Application (Client) ID
- Client credential
- Microsoft Entra OAuth 2.0 token endpoint

The application requested its configured Microsoft Graph application permissions using:

`https://graph.microsoft.com/.default`

Microsoft Entra ID successfully authenticated the application and issued an OAuth access token.

The returned token type was:

`Bearer`

No client secrets or access tokens are included in this repository.

---

## Part 7 – Microsoft Graph API Test

After obtaining an OAuth access token, I used PowerShell to send an authenticated request to Microsoft Graph.

The application queried:

`GET /v1.0/users`

The request selected only the `displayName` property for the portfolio evidence.

Microsoft Graph successfully returned the test users from the Microsoft Entra tenant.

This confirmed that:

1. The Falcon Tech Employee Portal could authenticate as an application.
2. OAuth 2.0 Client Credentials authentication was functioning.
3. Microsoft Entra ID successfully issued an access token.
4. The admin-consented `User.Read.All` application permission was effective.
5. The application could access Microsoft Graph without an interactive user sign-in.

---

## Authentication Flow

```text
Falcon Tech Employee Portal
        |
        | Client ID + Client Credential
        v
Microsoft Entra ID
        |
        | OAuth 2.0 Client Credentials Flow
        v
OAuth Access Token
        |
        | Bearer Token
        v
Microsoft Graph
        |
        | User.Read.All
        v
Entra ID User Data
