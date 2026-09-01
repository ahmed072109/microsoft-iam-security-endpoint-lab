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
- Reviewed the relationship between the App Registration and Enterprise Application/service principal

The client secret value was never stored in the GitHub repository.

---

## Part 3 – Application Roles

Custom application roles were created to simulate role-based access to the Falcon Tech Employee Portal.

### Roles Created

**Employee**

Standard employee access to the application.

**Portal Administrator**

Administrative access to the Falcon Tech Employee Portal.

The following test assignments were configured:

- Adam Wilson → Employee
- David Brown → Portal Administrator

These roles demonstrate how application roles can be assigned through Microsoft Entra ID and included as role claims in authentication tokens.

The application itself would be responsible for reading these claims and enforcing the appropriate authorization within the application.

---

## Part 4 – Microsoft Graph API Permissions

Microsoft Graph permissions were configured for the Falcon Tech Employee Portal.

Permissions included:

- `User.Read` – Delegated
- `User.ReadBasic.All` – Delegated
- `User.Read.All` – Application

Administrative consent was granted for the required Microsoft Graph application permission.

The `User.Read.All` application permission was used later in the lab to demonstrate app-only access to Microsoft Graph.

---

## Part 5 – OAuth 2.0 Client Credentials Flow

To test the application identity, I used the **OAuth 2.0 Client Credentials Flow**.

Unlike delegated authentication, this flow does not require a user to sign in.

The application authenticated using:

- Tenant ID
- Application (Client) ID
- Client credential
- OAuth 2.0 token endpoint

The application requested access to Microsoft Graph using:

`https://graph.microsoft.com/.default`

Microsoft Entra ID successfully authenticated the application and issued an OAuth access token.

The returned token type was:

`Bearer`

No client secrets or access tokens are included in this repository.

---

## Part 6 – Microsoft Graph API Test

After obtaining the OAuth access token, I used PowerShell to send an authenticated request to Microsoft Graph.

The request queried:

`GET /v1.0/users`

Only the `displayName` property was displayed as evidence to avoid unnecessarily exposing tenant information.

Microsoft Graph successfully returned the test users from the Entra tenant.

This confirmed that:

1. The application could authenticate to Microsoft Entra ID.
2. OAuth 2.0 Client Credentials authentication was functioning.
3. The application received an access token.
4. The admin-consented `User.Read.All` application permission was effective.
5. The application could successfully access Microsoft Graph without an interactive user sign-in.

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
