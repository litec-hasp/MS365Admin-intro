---
title: Exchange Admin Center
author: hasp

theme: moon
---

## Exchange Admin Center

<img src="./_img/logo-exchange.png" alt="logo" style="zoom:67%;" />

### Create a DDG & Mail Flow

---

## Exchange Admin Center (EAC)

- Centralized hub for managing Exchange Online (and in hybrid scenarios, on-premises Exchange)
- Control mailboxes, distribution groups, settings, ...
- **Key Sections**:
  - Recipients (Mailboxes, groups, resources, contacts)
  - Compliance Management (Security and data governance)
  - Organization (Company settings, add-ons)
  - Protection (Anti-spam, anti-malware)
  - Mail Flow (Rules, delivery reports, connectors)

---

## DDG Example (Step-by-Step)

### Dynamic Distribution Groups Creation

1. Access **Recipients** > **Groups** in the EAC
2. Click **+** and select **Dynamic distribution group**
3. Define a descriptive name `_tst_...`
4. Set filtering rules (Department `TST`)
5. Configure additional options (owner, membership approval)
6. Save the new dynamic distribution group

---

## Mail Flow Rules

- "Transport Rules"
- Control what happens to messages based on:
  - Senders/Recipients
  - Message content
  - Other conditions
- Actions:
  - Redirecting, forwarding, or CC/BCCing
  - Adding disclaimers/headers
  - Blocking or quarantining messages

---

## Mail Flow Rule Usage Example

### Enforcing Legal Disclaimers

- Condition: Message is sent from our `_tst` group or `_tst` user, ...
- Action: Append a standard legal disclaimer to the message footer

---

### Mail FLow - Fallback Action

- **Fallback Actions**
  - Determine how Exchange handles messages if a rule can't be applied correctly
- **Options**
  - **Wrap:** Creates a new message, original becomes an attachment, disclaimer or modifications are added.
  - **Ignore:** Rule is bypassed, message proceeds without changes.
  - **Reject:** Message is bounced back to the sender with a customizable NDR.

---

## Other Features

- **Auditing:** Track changes by administrators
- **Mobile Device Management:**  Control phone policies
- **Hybrid Setup:** Manage on-premises/cloud coexistence
- **eDiscovery:** Search and retain mail data
