# Project 3 – Microsoft Entra ID MFA & Microsoft Authenticator

## Objective

Configure and test Multi-Factor Authentication (MFA) in Microsoft Entra ID using Microsoft Authenticator.

The purpose of this lab was to demonstrate how MFA strengthens identity security by requiring an additional authentication factor beyond a user's password.

---

## Lab Environment

- Microsoft Entra ID
- Microsoft Entra Admin Center
- Microsoft Authenticator
- Test User: Adam Wilson
- Security Defaults
- Microsoft Entra Sign-in Logs

---

## Tasks Completed

- Reviewed the Microsoft Authenticator authentication method policy
- Configured Microsoft Authenticator security settings
- Enabled application name display in push notifications
- Enabled geographic location display in push notifications
- Required a test user to register Microsoft Authenticator
- Registered Microsoft Authenticator for the test user
- Verified Microsoft Authenticator registration
- Configured Authenticator notifications as the user's default sign-in method
- Tested MFA authentication
- Reviewed authentication and sign-in activity in Microsoft Entra ID

---

## 1. Configure Microsoft Authenticator Security Settings

Microsoft Authenticator was configured through the Microsoft Entra authentication methods policy.

Additional security information was enabled for Authenticator push notifications, including the application name and geographic location.

These features provide users with additional context when receiving authentication requests and can help reduce the risk of users approving fraudulent MFA prompts.

![Microsoft Authenticator Security Settings](01-authenticator-security-settings.png)

---

## 2. Review Microsoft Authenticator Policy

The Microsoft Authenticator authentication method policy was reviewed to confirm that Authenticator was available to users.

Application name and geographic location information were enabled for Authenticator push notifications.

This provides users with additional information when evaluating authentication requests and helps them identify potentially suspicious sign-in attempts.

![Microsoft Authenticator Policy](02-authenticator-security-settings.png)

---

## 3. User MFA Registration

A test account, **Adam Wilson**, was used to validate the MFA configuration.

When the user signed in, Microsoft Entra required additional security information to be configured.

The user was prompted to set up Microsoft Authenticator as an additional authentication method.

![User MFA Registration Prompt](03-user-mfa-registration-prompt.png)

Microsoft Authenticator was then configured for the test account by completing the registration process.

This established the user's mobile device as an additional authentication factor.

---

## 4. Verify Microsoft Authenticator Registration

After registration, the authentication methods assigned to the test user were reviewed in the Microsoft Entra Admin Center.

Microsoft Authenticator was successfully registered to the user's mobile device.

The configuration confirmed:

- Microsoft Authenticator was registered
- A mobile device was successfully associated with the account
- Microsoft Authenticator notification was configured as the default sign-in method
- System-preferred MFA was enabled
- `PhoneAppNotification` was shown as the system-preferred MFA method

![Microsoft Authenticator Registration Verified](04-user-mfa-registration-verified.png)

---

## MFA Authentication Flow

The authentication process demonstrated in this lab was:

**Username + Password**

↓

**Microsoft Entra ID validates credentials**

↓

**MFA requirement evaluated**

↓

**Microsoft Authenticator notification sent**

↓

**User verifies the authentication request**

↓

**Access granted**

This demonstrates how MFA provides an additional security layer beyond password-only authentication.

If a user's password is compromised, an attacker would still need to satisfy the additional authentication requirement before gaining access.

---

## Security Concepts Demonstrated

### Multi-Factor Authentication (MFA)

MFA requires users to provide more than one authentication factor before access is granted.

This significantly reduces the risk associated with stolen or compromised passwords.

### Microsoft Authenticator

Microsoft Authenticator provides an additional authentication factor through a registered mobile device.

Authenticator can be used to approve authentication requests and provide additional verification during the sign-in process.

### Identity Security

Identity is a major security boundary in modern cloud environments.

Strengthening authentication helps protect organisational resources against credential theft and account takeover.

### MFA Prompt Context

Displaying the application name and geographic location provides users with additional context when reviewing an authentication request.

This can help users recognise authentication attempts they did not initiate.

### System-Preferred MFA

System-preferred MFA allows Microsoft Entra ID to determine the most secure authentication method available to a user rather than relying solely on the user's manually selected default method.

---

## Security Benefits

Implementing MFA provides protection against several common identity-based threats:

- Stolen passwords
- Credential stuffing
- Password spraying
- Phishing
- Unauthorized account access
- Account takeover

MFA therefore forms an important component of a Zero Trust identity security strategy.

---

## Skills Demonstrated

- Microsoft Entra ID administration
- Identity and Access Management (IAM)
- Multi-Factor Authentication (MFA)
- Microsoft Authenticator configuration
- Authentication method policies
- User MFA registration
- Authentication troubleshooting
- Identity security
- Security Defaults
- User authentication management
- Microsoft Entra sign-in monitoring

---

## Real-World Application

In an enterprise environment, MFA is a critical identity security control.

Administrators can use Microsoft Entra ID to strengthen authentication for users accessing corporate applications and cloud resources.

Microsoft Authenticator can provide users with an additional authentication factor while also providing contextual information about authentication requests.

MFA can also be combined with additional Microsoft Entra security capabilities such as:

- Conditional Access
- Privileged Identity Management (PIM)
- Identity Protection
- Access Reviews
- Identity Governance

Together, these technologies can provide stronger controls over who can access organisational resources and under what conditions.

---

## Outcome

Successfully configured and tested Microsoft Entra ID Multi-Factor Authentication using Microsoft Authenticator.

The lab demonstrated the process of configuring Authenticator security settings, requiring user MFA registration, registering Microsoft Authenticator and verifying the resulting authentication configuration.

This project provided practical hands-on experience with Microsoft Entra ID identity security controls commonly used within enterprise Identity and Access Management environments.

---

## Portfolio Skills

**Microsoft Entra ID | IAM | MFA | Microsoft Authenticator | Identity Security | Authentication Methods | Security Defaults | Sign-in Monitoring**
