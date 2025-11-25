# 08 – Microsoft Purview: Compliance & Data Protection

In this part of my Modern Workplace & Copilot project, I configured Microsoft Purview to protect my organization’s data, meet compliance requirements, and ensure secure information governance across Microsoft 365.

I used Microsoft Purview to implement:

- Sensitivity labeling  
- Data Loss Prevention (DLP)  
- Retention & records management  
- eDiscovery & Audit  
- Exchange Online Archiving  

Some additional features (Insider Risk Management, Compliance Manager) are documented for awareness but not configured due to licensing requirements.

---

## 01. Sensitivity Labels  
I configured sensitivity labels to classify and protect documents and emails across Microsoft 365.  
This includes encryption settings, content marking, and publishing label policies to users.

**Full configuration:**  
[14-purview-compliance-and-data-protection.md](../docs/14-purview-compliance-and-data-protection.md)

---

## 02. Data Loss Prevention (DLP)  
I created a custom DLP policy to prevent sharing of financial information, specifically **credit card numbers**, across:

- Exchange Online  
- SharePoint Online  
- OneDrive for Business  
- Microsoft Teams  

**Full configuration:**  
[15-dlp-policies.md](../docs/15-dlp-policies.md)

---

## 03. Retention & Records Management  
I created a retention policy that keeps Exchange, SharePoint, and OneDrive data for **7 years** and then automatically deletes it.  
This supports compliance and efficient long-term storage management.

**Full configuration:**  
[16-retention-policy.md](../docs/16-retention-policy.md)

---

## 04. eDiscovery & Audit  
I created an eDiscovery case and performed searches across multiple workloads.  
I also used the Audit tool to review user/admin activities within a custom time range.

**Full configuration:**  
[17-ediscovery-and-audit.md](../docs/17-ediscovery-and-audit.md)

---

## 05. Exchange Online Archiving  
I enabled archive mailboxes and created an auto-archive retention policy that moves items older than **2 years** into the archive mailbox.

**Full configuration:**  
[18-exchange-archiving.md](../docs/18-exchange-archiving.md)

---

# Summary

Microsoft Purview provides enterprise-grade data protection and compliance capabilities.  
In this stage of my Modern Workplace & Copilot project, I implemented and documented:

| Feature | Purpose | Status |
|--------|---------|--------|
| **Sensitivity Labels** | Classify & protect data | Configured |
| **DLP Policies** | Prevent leakage of sensitive information | Configured |
| **Retention Policies** | Automate long-term retention & deletion | Configured |
| **eDiscovery & Audit** | Search, investigate, and review logs | Configured |
| **Exchange Archiving** | Improve mailbox storage & retention | Configured |

This completes the **Microsoft Purview: Compliance & Data Protection** stage of my Modern Workplace & Copilot deployment.
