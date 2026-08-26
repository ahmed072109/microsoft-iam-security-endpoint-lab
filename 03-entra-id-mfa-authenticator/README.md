# Project 3 – Microsoft Entra ID MFA & Microsoft Authenticator

## Objective

Configure and test Multi-Factor Authentication (MFA) in Microsoft Entra ID using Microsoft Authenticator.

The purpose of this lab was to demonstrate how MFA strengthens identity security by requiring an additional authentication factor beyond a user's password.

## Lab Environment

- Microsoft Entra ID
- Microsoft Entra Admin Center
- Microsoft Authenticator
- Security Defaults
- Test user: Adam Wilson (IT Support Engineer)

## Tasks Completed

- Enabled Microsoft Authenticator as an authentication method
- Targeted Microsoft Authenticator to users
- Enabled number matching for push notifications
- Enabled application name display in authentication notifications
- Enabled geographic location display
- Registered Microsoft Authenticator for a test user
- Configured Microsoft Authenticator as the user's default sign-in method
- Performed an MFA sign-in using number matching
- Reviewed Microsoft Entra ID sign-in logs
- Verified that the MFA requirement was satisfied

## MFA Registration

The test user registered Microsoft Authenticator by scanning the Entra ID registration QR code.

After registration, Microsoft Authenticator appeared as a usable authentication method and was configured as the default sign-in method.

## MFA Testing

A new authentication attempt was performed using the test account.

Microsoft Entra ID generated a number-matching challenge that required approval through Microsoft Authenticator.

The authentication request was successfully approved from the registered mobile device.

## Sign-in Log Validation

Microsoft Entra ID sign-in logs were reviewed after testing.

The logs showed successful sign-in activity and confirmed that the MFA requirement had been satisfied.

Subsequent authentication events displayed **Previously satisfied**, demonstrating reuse of the existing authenticated session rather than requiring another MFA challenge.

## Security Concepts Demonstrated

- Multi-Factor Authentication (MFA)
- Microsoft Authenticator
- Number matching
- Authentication method policies
- Identity verification
- Security Defaults
- Authentication logging and monitoring
- MFA session behaviour

## Skills Demonstrated

Microsoft Entra ID | IAM | MFA | Microsoft Authenticator | Identity Security | Authentication Policies | Security Defaults | Sign-in Logs
