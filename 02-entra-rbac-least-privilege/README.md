# Project 02 – Microsoft Entra ID RBAC & Least Privilege

## Overview

This project demonstrates practical Role-Based Access Control (RBAC) administration using Microsoft Entra ID within the simulated **Falcon Tech Lab** environment.

The objective was to implement the principle of least privilege by assigning specific Microsoft Entra administrative roles to users based on their job responsibilities rather than providing unnecessary Global Administrator access.

Administrative role assignments were then verified using Microsoft Entra audit logs.

---

## Technologies Used

- Microsoft Entra ID
- Microsoft Azure
- Microsoft Entra Admin Center
- Microsoft Entra Administrative Roles
- Role-Based Access Control (RBAC)
- Entra Audit Logs
- GitHub

---

## Lab Scenario

Falcon Tech requires administrative responsibilities to be delegated securely across the IT environment.

Rather than granting administrators unrestricted access through the Global Administrator role, specific built-in Microsoft Entra roles were assigned according to job responsibilities.

Two role assignments were configured:

| User | Administrative Role | Purpose |
|---|---|---|
| David Brown | User Administrator | Manage users and groups |
| Adam Wilson | Helpdesk Administrator | Perform helpdesk-related identity administration |

This approach demonstrates the principle of **least privilege**, where users receive only the permissions required to perform their responsibilities.

---

## Microsoft Entra Administrative Roles

Microsoft Entra ID provides built-in administrative roles that allow organizations to delegate specific administrative permissions.

Using dedicated administrative roles reduces the need to assign highly privileged roles such as Global Administrator.

For this lab, two built-in roles were used:

### User Administrator

The **User Administrator** role was assigned to **David Brown**.

This role provides permissions for managing user and group-related activities within Microsoft Entra ID.

### Helpdesk Administrator

The **Helpdesk Administrator** role was assigned to **Adam Wilson**.

This role provides permissions appropriate for common helpdesk identity administration tasks while avoiding broader administrative privileges.

---

## User Administrator Role Assignment

David Brown was assigned the **User Administrator** role.

The role was assigned through:

**Microsoft Entra ID → Roles and administrators → User Administrator → Assignments**

After the assignment was completed, Microsoft Entra confirmed that David Brown had successfully been added to the role.

### User Administrator Assignment Evidence

![User Administrator role assignment](screenshots/01-user-administrator-assignment.png)

---

## Helpdesk Administrator Role Assignment

Adam Wilson was assigned the **Helpdesk Administrator** role.

This demonstrates how administrative responsibilities can be separated between users rather than providing all administrators with unrestricted privileges.

### Helpdesk Administrator Assignment Evidence

![Helpdesk Administrator role assignment](screenshots/02-helpdesk-administrator-assignment.png)

---

## Role-Based Access Control

Role-Based Access Control allows permissions to be assigned according to an individual's responsibilities.

In this lab:

**David Brown → User Administrator**

**Adam Wilson → Helpdesk Administrator**

This creates a separation of administrative responsibilities.

Instead of giving both users Global Administrator access, each account receives a role appropriate to its intended function.

This reduces unnecessary privileged access and helps limit the potential impact of compromised administrator accounts.

---

## Principle of Least Privilege

The **Principle of Least Privilege (PoLP)** states that users should receive only the permissions required to perform their responsibilities.

Applying least privilege helps organizations:

- Reduce unnecessary administrative access
- Limit the impact of compromised accounts
- Reduce the attack surface
- Improve accountability
- Separate administrative responsibilities
- Strengthen identity security

In this lab, dedicated administrative roles were used instead of assigning Global Administrator privileges.

---

## Audit Log Verification

Microsoft Entra audit logs were used to verify the administrative role assignments.

After the User Administrator role was assigned to David Brown, the audit logs recorded:

- **Category:** RoleManagement
- **Activity:** Add member to role
- **Status:** Success
- **Target:** David Brown
- **Role:** User Administrator

The audit log's **Modified Properties** section confirmed that the role added to the account was **User Administrator**.

### User Administrator Audit Evidence

![User Administrator audit log](screenshots/03-user-administrator-audit-log.png)

---

The Helpdesk Administrator assignment was also recorded within Microsoft Entra audit logs.

The audit evidence confirmed that Adam Wilson was assigned the **Helpdesk Administrator** role.

### Helpdesk Administrator Audit Evidence

![Helpdesk Administrator audit log](screenshots/04-helpdesk-administrator-audit-log.png)

---

## IAM Concepts Demonstrated

This project provided hands-on experience with:

- Microsoft Entra administrative roles
- Role-Based Access Control (RBAC)
- Principle of Least Privilege
- Administrative role assignment
- Privileged access management concepts
- Separation of administrative responsibilities
- Identity security
- Role management
- Administrative auditing
- Microsoft Entra audit logs
- Role assignment verification

---

## Security Considerations

Administrative privileges should be assigned carefully because privileged accounts can make significant changes within an identity environment.

Organizations should avoid assigning Global Administrator access when a more limited administrative role can perform the required task.

Using dedicated roles such as **User Administrator** and **Helpdesk Administrator** helps reduce excessive permissions and supports least-privilege security practices.

Administrative role assignments should also be monitored through audit logs to provide accountability and allow security teams to investigate changes to privileged access.

In larger production environments, additional privileged identity controls such as Microsoft Entra Privileged Identity Management (PIM) can provide further protection for administrative access.

---

## What I Learned

Through this project I gained practical experience with:

- Navigating Microsoft Entra administrative roles
- Understanding the difference between administrative roles
- Assigning built-in roles to users
- Applying least-privilege access principles
- Separating administrative responsibilities
- Reviewing RoleManagement events
- Investigating administrative changes using audit logs
- Identifying the target user of a role assignment
- Reviewing modified properties to determine which role was assigned

This demonstrated how Microsoft Entra ID can be used to securely delegate administrative responsibilities while maintaining visibility and accountability.

---

## Outcome

Successfully implemented and verified Microsoft Entra RBAC within the Falcon Tech Lab environment.

The project included:

- Assignment of the User Administrator role to David Brown
- Assignment of the Helpdesk Administrator role to Adam Wilson
- Implementation of least-privilege administrative access
- Separation of administrative responsibilities
- Verification of role assignments through Microsoft Entra audit logs
- Investigation of RoleManagement audit events
- Verification of assigned roles through audit log modified properties

This project builds upon the identity and group management environment created in Project 01 and provides a foundation for more advanced Microsoft Entra identity security projects.
