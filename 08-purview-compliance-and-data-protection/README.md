# 08 – Microsoft Purview: Compliance & Data Protection

In this part of my modern workplace project, I configured Microsoft Purview to protect my organization’s data, meet compliance requirements, and ensure secure information governance across Microsoft 365.  

I used Microsoft Purview to implement **sensitivity labeling, data loss prevention, retention, eDiscovery, auditing, and mailbox archiving**.  
Each section below includes a short overview and a link to the full technical configuration steps documented in my project.

---

## 01. Sensitivity Labels

I configured sensitivity labels to classify and protect documents and emails across Microsoft 365.  
This included creating labels, defining encryption and content marking rules, and publishing label policies so users can apply them in Office apps.

**Read the full configuration:**  
[01-sensitivity-labels.md](../docs/08-purview-compliance-and-data-protection)

---

## 02. Data Loss Prevention (DLP)

I created a custom DLP policy focused on protecting **financial information**, specifically **credit card numbers**.  
My DLP policies monitor and prevent sensitive information from being shared outside the organization across Exchange, SharePoint, OneDrive, and Teams.

**Read the full configuration:**  
[03-dlp-policies.md](../docs/15-dlp-policies.md)

---

## 03. Insider Risk Management *(informational only)*

Insider risk requires an E3/E5 add-on license, so I did not enable the feature.  
Instead, I documented how Insider Risk Management works and where it fits into a real production environment.

**Overview and notes:**  
[04-insider-risk.md](../docs/16-insider-risk.md)

---

## 04. Retention & Records Management

I created a retention policy that keeps Exchange, SharePoint, and OneDrive content for **7 years**, then automatically deletes it.  
This helps me meet compliance standards and maintain clean data storage across Microsoft 365.

**Read the full configuration:**  
[05-retention-records.md](../docs/17-retention-records.md)

---

## 05. eDiscovery & Audit

I created an **eDiscovery case** to simulate an internal investigation and performed searches across Exchange, SharePoint, OneDrive, and Teams.  
Additionally, I used **Audit** to review user and admin activities with custom search criteria.

**Read the full configuration:**  
[06-ediscovery-and-audit.md](../docs/18-ediscovery-and-audit.md)

---

## 06. Compliance Manager *(informational only)*

Compliance Manager provides score-based compliance assessments.  
In my project, I documented its purpose and how organizations typically use it, without configuring full assessments or improvement actions.

**Overview and notes:**  
[07-compliance-manager.md](../docs/19-compliance-manager.md)

---

## 07. Exchange Online Archiving (Auto-Archive Mailboxes)

I enabled mailbox archiving for my user and created a retention policy that automatically moves items older than 2 years to the archive mailbox.  
This helps maintain mailbox size limits and improves long-term email management.

**Read the full configuration:**  
[08-exchange-archiving.md](../docs/20-exchange-archiving.md)

---

# Summary

Microsoft Purview plays a major role in securing and governing information across Microsoft 365.  
In this part of my project, I implemented and documented:

| Area | Purpose | Status |
|------|---------|--------|
| **Sensitivity Labels** | Classify & protect data | Configured |
| **DLP Policies** | Prevent sharing sensitive data | Configured |
| **Insider Risk** | Detect risky activity | Documented only |
| **Retention & Records** | Keep/delete content for compliance | Configured |
| **eDiscovery & Audit** | Investigate and review user actions | Configured |
| **Compliance Manager** | Assess compliance posture | Documented only |
| **Mailbox Archiving** | Manage long-term email storage | Configured |

This completes the Purview portion of my Modern Workplace & Copilot deployment.

