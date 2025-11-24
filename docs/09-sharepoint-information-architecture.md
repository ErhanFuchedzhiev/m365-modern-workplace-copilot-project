# 09 – SharePoint Information Architecture
Modern SharePoint Hub Design for a Structured Digital Workplace

In this part of my Modern Workplace project, I built the SharePoint Online Information Architecture (IA) that will support all document management, collaboration, governance, and future migration activities.
This includes creation of the Intranet hub, department sites, hub association, and establishing a scalable structure aligned with Microsoft 365 best practices.
This article summarizes the full workflow and links to screenshots used throughout the build.

---

## 1. Creating the Intranet Communication Site

I started by creating the main Intranet site, which acts as the central communication hub for the entire organization.

This site will provide:

- Company-wide news
- Corporate resources
- Global navigation
- Central branding
- Unified search

After creation, the Intranet site appears in Active sites. 

![Validation Passed](../images/55.sharepoint-site-creation.png)

---

## 2. Creating All Department Sites

After creating the hub, I deployed a set of Team Sites for each department.
Each site was created as Private, following least-privilege and zero-trust principles.

Departments created:

- Human Resources
- Finance
- Marketing
- Sales
- Operations
- Management
- Projects
- Learning & Development

These represent the core content containers for future document migration.

![Validation Passed](../images/56.sharepoint-active-sites-creation.png)

---

## 3. Registering the Intranet as a Hub Site

Next, I registered the Intranet as a Hub Site so it can serve as the root of the SharePoint hierarchy.

This enables:

- Hub navigation
- Branding inheritance
- Unified permissions logic
- Central governance

Consistent experience across all departments.

![Validation Passed](../images/57.Intranet-register-as-hub-site.png)

![Validation Passed](../images/58.intranet-hub-site.png)

---

## 4. Associating Each Department Site With the Intranet Hub

Once all department sites were created, I associated every site to the Intranet Hub.

This delivers:

- Shared navigation
- Consistent branding
- Centralized governance
- Logical site hierarchy
- Improved search experience

Association was applied in bulk.

![Validation Passed](../images/58.each-folder-hub-association.png)

---

## 5. Final Verification – All Sites Connected to the Hub

After completing the association, the Hub column now shows Intranet for every department site.

This confirms the Information Architecture is properly aligned.

![Validation Passed](../images/59.all-site-intranet-completed.png)

---

## Final Result

With all steps completed, my SharePoint Online Information Architecture now includes:

- A centrally managed Intranet hub site
- Private departmental team sites
- Full hub association for consistent branding and navigation
- A clean, scalable structure for document migration
- Alignment with Copilot readiness
- Governance-friendly site separation
- A modern M365-compliant information architecture

This structure now serves as the foundation for:

- SharePoint migration
- OneDrive rollout
- Data governance
- Sensitivity label architecture
- Copilot document exposure control
- Organizational knowledge structure

My IA is now modern, secure, scalable, and ready for the next steps of the Modern Workplace project.

