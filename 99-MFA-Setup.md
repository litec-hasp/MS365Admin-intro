---
title: Bonus - MFA
author: hasp

theme: moon
---

## Multi Factor Authentication - MFA

![MFA](https://learn.microsoft.com/en-us/training/achievements/secure-aad-users-with-mfa.svg)

#### Based on

#### [Secure Microsoft Entra users with multifactor authentication | Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/secure-aad-users-with-mfa/)

> Use multifactor authentication with Microsoft Entra ID to harden your user accounts.

---

## What is MS Entra MFA?

- MFA supplies added security for your identities by requiring - two or more elements for full authentication. 3 categories:
  - **Something you know**, a password or the answer to a security question.
  - **Something you possess**, a mobile app that receives a notification or a token-generating device.
  - **Something you are**,  typically a biometric property (fingerprint or face scan)
- Needs Entra ID  P1 or P2.

<img src="https://learn.microsoft.com/en-us/training/modules/secure-aad-users-with-mfa/media/2-mfa-example.png" alt="MFA Overview" style="zoom:67%;" />

---

## Microsoft Entra MFA Policies

- MFA is enforced with *Conditional Access policies* (IF-THEN Rules).

- Examples:
  - IF a specific cloud application is accessed
  - IF a user is accessing a specific network
  - IF a user is accessing a specific client application
  - IF a user is registering a new device 

- Auth Methods: see [SSPR-Setup](./98-SSPR-Setup.md)

---

### Planning - Deployment

<small>See: [Deployment considerations for Microsoft Entra MFA | Microsoft Learn](https://learn.microsoft.com/en-us/entra/identity/authentication/howto-mfa-getstarted#enforcing-registration)</small>

![Conceptual Conditional Access process flow](https://learn.microsoft.com/en-us/entra/identity/authentication/media/howto-mfa-getstarted/conditional-access-overview-how-it-works.png)

### Common Policies

- For administrators
- For Azure Management

---

### Configure MFA Options

1. Sign in to the [Azure portal](https://portal.azure.com/) using a Global administrator account.
2. Navigate to the Microsoft Entra dashboard using the **Microsoft Entra ID** option in the side menu.
3. Select **Security** in the left-hand menu.
4. Select **multifactor authentication** under the **Manage** heading in the menu. Here, you find options for multifactor authentication.
5. Under **Configure**, select **Additional cloud-based multifactor authentication settings**. A new browser page opens where you can see all the MFA options for Azure.

---

### Setup Conditional Access rule for MFA <small>1/2</small>

1. Switch back to the Azure portal and select **Microsoft Entra ID** > **Security** > **Conditional Access**.
2. Select **Create new policy** from the top menu.
3. Name your policy, for example, *All guests*.
4. Under **Users**, select **0 users and groups selected**.
   1. Under **Include**, choose **Select users and groups**.
   2. Select users and groups and then choose **Select**.
5. Under **Target resources**, select **No target resources selected**.
   1. Select **Cloud apps**.
   2. Under **Include**, choose **Select apps**.
   3. Under **Select**, choose **None**. Select apps from the options on the right and then choose **Select**.

---

### Setup Conditional Access rule for MFA <small>2/2</small>

6. Under **Conditions**, select **0 conditions selected**.
   1. Under **Locations**, select **Not configured**.
   2. Under **Configure**, select **Yes**, then select **Any location**.
7. Under **Grant**, select **0 controls selected**.
   1. Make sure that **Grant access** is selected.
   2. Select **Require multifactor authentication** and choose **Select**. This option enforces MFA.
8. Set **Enable policy** to **On**, and then **Create**.
9. MFA is now enabled for your selected applications. The next time a user or guest tries to sign into that app, they're prompted to register for MFA.

---

### Info-Link for Users (DE)

> [Einrichten von Sicherheitsinformationen über eine Anmeldeseite - Microsoft-Support](https://support.microsoft.com/de-de/account-billing/einrichten-von-sicherheitsinformationen-über-eine-anmeldeseite-28180870-c256-4ebf-8bd7-5335571bf9a8)
