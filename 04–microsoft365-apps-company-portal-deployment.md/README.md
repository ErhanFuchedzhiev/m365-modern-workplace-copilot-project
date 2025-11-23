# 04 – Microsoft 365 Apps & Company Portal Deployment  
_Deploying the core productivity and management apps for all Autopilot devices_

---

## Overview

After enrolling my device using the Company Portal, I continued with deploying the core applications needed for a modern M365-managed Windows environment:

- **Company Portal** (Microsoft Store app – new)  
- **Microsoft 365 Apps for Windows 10 and later**  
- **Microsoft Edge** (already deployed earlier)

These apps ensure users have seamless access to corporate resources, productivity tools, and self-service capabilities.

This article includes step-by-step guidance and screenshots.

---

# 1️. Deploy the Company Portal App

The **Company Portal** app is required for self-service app installation, device compliance checks, and user-based onboarding.

---

## Step 1 — Create the App

**Intune Admin Center → Apps → Windows Apps → + Create → Microsoft Store app (new)**

![company-portal-step1](../screenshots/52.app-information.png)

---

## Step 2 — Configure App Information

- **Name:** Company Portal  
- **Publisher:** Microsoft Corporation  
- **Installer Type:** UWP  
- **Install behavior:** User  
- **Privacy URL:** <https://learn.microsoft.com/mem/intune/user-help/use-the-company-portal-app>  

![company-portal-info](../screenshots/53.assignments.png)

---

## Step 3 — Assign the App

Assign to:

- **Required → Autopilot Devices**

![company-portal-assignments](../screenshots/54.deployed-company-portal.png)

---

## Step 4 — Deployment Completed

The Company Portal app is now successfully deployed.

---

# 2️. Deploy Microsoft 365 Apps (Office)

Microsoft 365 Apps provide Outlook, Word, Excel, OneDrive, Teams, and the essential productivity suite for Windows.

---

## Step 1 — Create the App

**Apps → Windows Apps → + Create → Windows 10 and later → Microsoft 365 Apps**

![m365-step1](../screenshots/46.m365-apps-deploying.png)

---

## Step 2 — App Suite Information

- **Suite name:** Microsoft 365 Apps for Windows 10 and later  
- **Category:** Productivity  
- Leave logo and metadata as default (Microsoft-provided).

![m365-info](../screenshots/47.app-information.png)

---

## Step 3 — Configure App Suite (Important)

On **Configure app suite**:

### 3.1 Select Office apps

Under **Select Office apps**, I selected the standard productivity set (8 selected in the UI):

- Microsoft Outlook  
- Microsoft Word  
- Microsoft Excel  
- Microsoft PowerPoint  
- Microsoft OneNote  
- Microsoft Teams (per-machine)  
- OneDrive (Groove / Sync client)  
- Microsoft Access / Publisher (optional, but included in my lab)

> **Select other Office apps (license required):** `0 selected` (none needed for this lab).

### 3.2 App suite information & update settings

Then I configured:

| Setting                     | Value                             |
| --------------------------- | --------------------------------- |
| **Architecture**            | 64-bit                            |
| **Default file format**     | Office Open Document Format       |
| **Update channel**          | Monthly Enterprise Channel        |
| **Remove other versions**   | Yes                               |
| **Version to install**      | Latest                            |
| **Shared computer activation** | No                            |
| **Accept license terms on behalf of users** | Yes             |
| **Install background service for Microsoft Search in Bing** | Yes |
| **Languages**               | No languages selected (OS default)|

![m365-config](../screenshots/48.configure-app-suite.png)

This ensures all selected Office apps are installed in a consistent, evergreen way.

---

## Step 4 — Assign the App

Assign to:

- **Required → Autopilot Devices**

![m365-assignments](../screenshots/49.assignments.png)

---

## Step 5 — Deployment Completed

![m365-deployed](../screenshots/50.deployed-m365-apps.png)

Microsoft 365 Apps are now deployed to all devices.

---

# 3️. Microsoft Edge Deployment (Already Completed)

Edge was deployed earlier in the Browser Policies article and appears in the Windows Apps list.

![edge-deployed](../screenshots/51.deploying-company-portal.png)

---

# Summary

You successfully deployed all core apps required for a modern Windows 11 M365 environment:

| App              | Status     |
| ---------------- | ---------- |
| Microsoft Edge   |  Deployed |
| Company Portal   |  Deployed |
| Microsoft 365 Apps |  Deployed |

These apps ensure:

- smooth onboarding  
- access to productivity tools  
- corporate resource access  
- compliance and self-service capabilities  

Your device app baseline is now complete.
