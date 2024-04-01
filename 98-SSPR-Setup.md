---
title: Bonus - SSPR
author: hasp

theme: moon
---

## Self Signed Password Reset

![SSPR](https://learn.microsoft.com/en-us/training/achievements/allow-users-reset-their-password.svg)

#### Based on

#### [Self-Service-Password-Reset - Microsoft Entra - Training | Microsoft Learn](https://learn.microsoft.com/de-de/training/modules/allow-users-reset-their-password/)

---

### Why SSPR?

- Reduce admin workload!
- Users can fix password problems themselves.

---

### How SSPR works

1. The user initiates a password reset
   - either by going directly to the password-reset portal or 
   - by selecting the "Can't access your account"-link on a sign-in page.
2. The reset portal takes these steps:
   - **Localization**: The portal checks the browser's locale setting and renders the SSPR page in the appropriate language.
   - **Verification**: The user enters their username and passes a captcha to ensure that it's a user and not a bot.
   - **Authentication**: The user enters the required data to authenticate their identity. They might, for example, enter a code or answer security questions.
   - **Password reset**: If the user passes the authentication tests, they can enter a new password and confirm it.
   - **Notification**: A message is sent to the user to confirm the reset.

---

### Authentication Types

- Mobile app notification (Microsoft Authenticator app) - *recommended*
- Mobile app code (MS and other Authenticator apps) - *recommended*
- Email (2nd eMail address) - *recommended*
- Mobile phone (SMS message or call) - **SMS not recommended!**
- Office phone (call)
- Security questions - **not recommended!**

---

### Todos

- Set minimum number of auth methods to 1 or 2.
- Allow at least both app variants and mail.
- Configure Notifications.

---

## Implementation

> See [Implement SSPR | Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/allow-users-reset-their-password/3-implement-azure-ad-self-service-password-reset)

- Start with one (test)group (`_tst`) - use a security group
- Scope of Rollout: Enabled or Selected

---

### Configuration <small>1/2</small>

1. Go to **Microsoft Entra ID** > **Protection** > **Password reset**.
2. **Properties**:
   - Enable SSPR.
   - You can enable it for all users in the Microsoft Entra organization or for selected users.
   - To enable for selected users, you must specify the security group. Members of this group can use SSPR.
3. **Authentication methods**:
   - Choose whether to require one or two authentication methods.
   - Choose the authentication methods that the users can use.

---

### Configuration <small>2/2</small>

4. **Registration**:
   - Specify whether users are required to register for SSPR when they next sign in.
   - Specify how often users are asked to reconfirm their authentication information. (180 or 360 days?)
5. **Notifications**: Choose whether to notify users and administrators of password resets.
6. **Customization**: Provide an email address or web page URL where your users can get help.

---

### Info-Link for Users (DE)

> [Registrieren der Überprüfungsmethode für die Kennwortzurücksetzung für ein Geschäfts-, Schul- oder Unikonto - Microsoft-Support](https://support.microsoft.com/de-de/account-billing/registrieren-der-überprüfungsmethode-für-die-kennwortzurücksetzung-für-ein-geschäfts-schul-oder-unikonto-47a55d4a-05b0-4f67-9a63-f39a43dbe20a)
