---
title: MS365 Entra ID Center
author: hasp

theme: moon

---

## [MS365 ENTRA-ID Center](https://entra.microsoft.com/#home)

<img src="./_img/logo-entra.png" alt="logo" style="zoom:67%;" />

### Create TestUsers and Group(s)

---

## Setup <small>Test-Env 1/4</small>

> Link: [Set up a test environment for your app - Microsoft identity platform | Microsoft Learn](https://learn.microsoft.com/en-us/entra/identity-platform/test-setup-environment)
>
> Best Way would be Test Tenant via Developer Program (I can't atm)

---

## User Creation <small>Test-Env 2/4</small>

- Browse to **Identity** > **Users** > **All users**.
- Select **New user** > **Create new user** and create some new test users in your directory.
- use the example-`.csv` (see [Bulk Creation - Microsoft Entra ID | Microsoft Learn](https://learn.microsoft.com/entra/identity/users/users-bulk-add)) and [Bulk Deletion - Microsoft Entra ID| Microsoft Learn](https://learn.microsoft.com/entra/identity/users/users-bulk-delete) - no whitespaces after `,`!
- Change domain (`contoso.com` won't work) - see [Domains - Microsoft 365 admin center](https://admin.cloud.microsoft/?#/Domains)
- and passwords (according to your security settings)!
- Recommendation - add a manager: Click User > **Edit Properties** > **All** > **Manager**

> ⚠️**Don't use the given passwords, this is a public repo and can be seen by others!**

---

<!-- .slide: data-background-image="https://media.tenor.com/j3cVEPj4bzkAAAAC/cat-typing.gif" data-background-opacity="0.2" -->

### *User Login Test*

- Open a new private window in your browser
- login as one of the test users
- set a new password (and remember it!)
- check, that you got NO apps 😭
- we need to add a license!  

---

## Security Group <small>Test-Env 3/4</small>

- **Identity** > **Groups** > **All groups** > **New Group**
  - Type: `Security`
  - Name: `_tst_sg_<YourChoice>`
  - Membership: `Dynamic User`
  - Owner: YOU! 🫵
  - Query: `(user.department -eq "TST") and (user.displayName -startsWith "_tst_")`
  - Check Query: **Validate Rules** Tab

---

## Licensing  <small>Test-Env 4/4</small>

- Open group: **Identity** > **Groups** > **All groups**
- search for `_tst` and select grp
- go to **Licenses** > select type (e.g. A1)
- DONE! 🎇

---

<!-- .slide: data-background-image="https://media.tenor.com/j3cVEPj4bzkAAAAC/cat-typing.gif" data-background-opacity="0.2" -->

### *User App Test*

- go back to private window
- refresh
- enjoy your MS Office Apps! 🥳

---

### YOU WANT MORE?

- Checkout **(Dynamic) Distribution Groups** in **Exchange**!
  - ⚠️ *I got the feeling MS wants to get rid of those...*
- You want to connect an App? - [Register a web app that signs in users - Microsoft identity platform | Microsoft Learn](https://learn.microsoft.com/en-us/entra/identity-platform/scenario-web-app-sign-user-app-registration?tabs=aspnetcore)
  - to sign on via `.net / java / node.js / python`
