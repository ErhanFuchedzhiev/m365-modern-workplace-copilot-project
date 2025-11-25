# 07. Exchange Online and Mail Flow

In this article, I document how I designed, structured, and secured my Exchange Online environment as part of my Modern Workplace build. This includes my mailbox architecture, my migration approach, and the core security and compliance controls that I implemented across Exchange Online and mail flow.

---

## 1. My Mailbox Structure

Before I configured policies, transport rules, and security controls, I first aligned my Exchange Online mailbox structure with my organization’s operational needs.  

Here’s how I approached it:

- **User Mailboxes:**  
  I provision user mailboxes automatically through Entra ID and assign the appropriate license bundles. Each mailbox inherits my default address book policy, retention processing, and standard Exchange Online feature set.

- **Shared Mailboxes:**  
  I create shared mailboxes for functional or departmental use cases such as HR, Finance, IT Operations, Service Desk, and generic contact points. I assign delegated permissions using “Send As”, “Send on Behalf”, or “Full Access”, depending on the role requirements.

- **Resource Mailboxes:**  
  I configure room and equipment mailboxes where needed (meeting rooms, shared equipment). I maintain booking restrictions, scheduling windows, and delegation as required.

- **Distribution Lists / Groups:**  
  I use Microsoft 365 Groups or Distribution Lists depending on the collaboration pattern. Where email distribution only is needed, I use traditional distribution lists.

This structure ensures my mail routing, permissions, and compliance rules operate consistently across my environment.

---

## 2. My Migration Strategy

My migration approach depends on the environment I am transforming. I typically use one of these strategies:

- **Cutover Migration:**  
  I use this for small organizations where I can move all mailboxes in a single batch.

- **Staged Migration:**  
  I use this when mailboxes must be moved in phases, especially when the cutover window must be minimized.

- **Hybrid Migration:**  
  I deploy Exchange Hybrid when coexistence is required. This gives me features such as shared free/busy, secure mail routing, on-prem directory synchronization, and staged migration waves.

- **Third-party or PST Migration:**  
  When the source system is non-Exchange, I prepare mail data for import and assign licenses post-migration.

Regardless of method, I ensure the following are prepared:

- DNS and domain verification  
- Mail routing cutover plan  
- Directory synchronization (if required)  
- Recipient and identity clean-up  
- Licensing readiness  
- User communication plan

This allows me to transition mail services to Exchange Online with minimal impact.

---

## 3. My Email Protection Controls

I configured my email security baselines across Anti-Phish, Anti-Spam, Safe Links, and Safe Attachments. This ensures that I protect my users against phishing, malware, and malicious URLs.

I documented the complete setup in:

**[12-email-protection-policies.md](https://github.com/ErhanFuchedzhiev/m365-modern-workplace-copilot-project/blob/main/docs/12-email-protection-policies.md)**

This article includes all configurations I implemented:

- Anti-phishing policies  
- Anti-spam inbound and outbound policies  
- Anti-malware policies  
- Safe Links  
- Safe Attachments  
- User impersonation protection  
- Domain impersonation protection  
- Global security baselines

These protections establish my secure email perimeter and form the foundation of my Exchange Online security posture.

---

## 4. My Transport Rules (Compliance & Mail Flow)

To enhance both compliance and user awareness, I implemented several Exchange Online transport (mail flow) rules. These rules help me manage sensitive data, enforce encryption, and provide external sender warnings.

All rules are fully documented in:

**[13-exchange-online-transport-rules.md](https://github.com/ErhanFuchedzhiev/m365-modern-workplace-copilot-project/blob/main/docs/13-exchange-online-transport-rules.md)**

This includes:

- Outbound Sensitive Data Encryption  
- Outbound Sensitive Tagging  
- External Email Warning Banner  
- Outbound Message Encryption (OMEv2)  
- Rule conditions and exception logic  
- Matching sender address behavior  
- Enforcement settings  

These rules help me automate compliance, improve security awareness, and prevent data leakage.

---

## 5. My Message Encryption Controls

Message Encryption (OME) enables me to protect sensitive outbound email communications with enforced encryption when sent to external recipients.

The full configuration is included within the same article:

**[Message Encryption (Section 4)](https://github.com/ErhanFuchedzhiev/m365-modern-workplace-copilot-project/blob/main/docs/13-exchange-online-transport-rules.md)**

This includes:

- External recipient detection  
- Encryption enforcement  
- OMEv2 rights-protection settings  
- Exceptions for internal users  
- Rule sequencing and enforcement  

By implementing this rule, I ensure that sensitive external communication is always encrypted.

---

## Summary

In this article, I summarized the core components of how I designed and secured my Exchange Online and mail flow configuration:

| Area | What I Completed |
|------|------------------|
| **Mailbox Structure** | I defined my user, shared, resource, and distribution mailbox models |
| **Migration Strategy** | I use cutover, staged, hybrid, or import-based migrations depending on the scenario |
| **Email Protection Policies** | Anti-phish, anti-spam, Safe Links, Safe Attachments, malware filtering |
| **Transport Rules** | Tagging, encryption, disclaimers, external alerts |
| **Message Encryption** | OMEv2 enforced encryption for external recipients |

These components together form my complete Exchange Online and mail flow architecture.

---

