# 05 – SharePoint & OneDrive Information Architecture and Migration  

---

### Building a Modern, Secure, and Migration-Ready SharePoint Environment

In this phase of my Modern Workplace & Copilot project, I designed and deployed my complete **SharePoint Online Information Architecture**, configured all **SharePoint Admin Center governance controls**, and performed a **sample migration using the SharePoint Migration Tool (SPMT)**.

This work ensures my environment is:

- Scalable  
- Secure  
- Well-structured  
- Copilot-ready  
- Optimized for data governance and future automation  

This article summarizes the three major SharePoint steps of my project and links to each detailed sub-article.

---

## 1. Designing My SharePoint Information Architecture  
**Documentation:**  
[09-sharepoint-information-architecture.md](../docs/09-sharepoint-information-architecture.md)

I first created my **Intranet communication site**, which became the main hub for navigation, branding, and centralized governance.

Then I created a set of **private departmental SharePoint team sites**:

- Human Resources  
- Finance  
- Marketing  
- Sales  
- Operations  
- Management  
- Projects  
- Learning & Development  

I registered the Intranet as my **Hub Site** and associated all departments to it.  
This provided:

- Unified navigation  
- Consistent branding  
- Central governance  
- Logical site hierarchy  
- Search alignment across all sites  

This completed the foundation for SharePoint, OneDrive, and Copilot readiness.

---

## 2. Configuring SharePoint Admin Settings for Governance & Security  
**Documentation:**  
[10-sharepoint-admin-configuration.md](../docs/10-sharepoint-admin-configuration.md)

Before performing any migration, I applied a set of core governance and security configurations inside SharePoint Admin Center.

### External Sharing  
- Default links → **Internal only**  
- Guest access expiration → **30 days**  
- Reauthentication → **30 days**  
- Disabled “Allow guests to reshare items they don’t own”  

### Version History  
- Enabled **manual version limits**  
- Set limit to **500 versions**  

### Site Creation  
- Disabled user-driven site creation  
- Ensured consistent creation path (`/sites/`)  
- Locked down site lifecycle to admin control  

These settings enforce Zero Trust principles and prepare the tenant for controlled data growth and compliance.

---

## 3. Migrating Legacy Content Using SPMT  
**Documentation:**  
[11-sharepoint-migration-spmt.md](../docs/11-sharepoint-migration-spmt.md)

Once my IA and governance were in place, I performed a full sample migration to validate the end-to-end process.

### Migration Workflow I Completed  
1. Prepared local “legacy file share” folders  
2. Opened the **SharePoint Migration Tool (SPMT)**  
3. Selected **File Share → SharePoint** migration  
4. Chose my local folder as the source  
5. Mapped it to my SharePoint target site's **Documents** library  
6. Configured migration settings (hidden files on, NTFS permissions off, auto-mapping on)  
7. Ran the migration  
8. Verified the migrated files inside the SharePoint site  

This confirmed that my SharePoint structure, permissions, and governance settings fully support future migration workloads.

---

# Final Result

By completing all three steps, I now have:

- A clean SharePoint Information Architecture aligned with departments  
- Secure, governed, and standardized SharePoint settings  
- A validated migration pipeline using SPMT  
- A strong foundation for:  
  - OneDrive rollout  
  - Data governance  
  - Sensitivity labels  
  - Retention policies  
  - Copilot content discovery  
  - Enterprise modernization  

This completes the SharePoint phase of my Modern Workplace & Copilot project.



