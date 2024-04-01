---
title: MS365 - App Registration
author: hasp

theme: league
---

<!-- .slide: data-background-image="./_img/AppRegistration.png" data-background-opacity="0.2" data-background-size="20%" data-background-position="right 3% top 3%" -->

# App Registrations

### Microsoft Entra App Registration

### An Introduction to Identity and Access Control

For external authentication and authorization.

---

## What Is App Registration?

- **Creates an Identity:**
  - App registration gives your app an identity within Microsoft Entra.
- **Defines Permissions:**
  - Specifies the data and actions your app can access within Microsoft Entra and other connected services.
- **Manages Authentication & Authorization:**
  - Controls how users sign in to your app and what level of access they are granted.
  - Example: Enable single sign-on (SSO) on external apps.

---

### Identity Platform

> [Quickstart: Register an App - Microsoft identity platform | Microsoft Learn](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app)

![identity platform](https://learn.microsoft.com/en-us/entra/identity-platform/media/v2-overview/about-microsoft-identity-platform.svg)

<small>🤷 **Auth what?** See [An Illustrated Guide to OAuth and OpenID Connect | Okta Developer](https://developer.okta.com/blog/2019/10/21/illustrated-guide-to-oauth-and-oidc)</small>

---

## Example Walkthrough: Registering a Web App

1. **App Registrations:**
   - Navigate to App Registrations and select "New Registration".
2. **App Details:**
   - Provide a name, supported account types, and redirect URIs.
3. **API Permissions:**
   - Define the specific permission scopes your app requires.
4. **Client Secrets:**
   - Generate secure credentials for your app to use during authentication.

---

## Integrating Your App

> See [Code samples for Microsoft identity platform authentication and authorization - Microsoft identity platform | Microsoft Learn](https://learn.microsoft.com/en-us/entra/identity-platform/sample-v2-code?tabs=apptype)

### Steps to Consider

- **Authentication Libraries:**
  - Utilize Microsoft’s authentication libraries for your chosen technology stack. (MSAL)
- **App ID and Client Secret:**
  - Configure your app with the App ID (Client ID) and Client Secret obtained during registration.
- **Redirect Users:**
  - to Microsoft’s login page for a secure authentication process.
- **Handle Tokens:**
  - Use them to access resources and perform permitted actions.
