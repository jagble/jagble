# Hi, I'm Josh 👋

I build IAM Projects, break them, fix them, and document all of it.
 
**Experience:** Identity & Access Management · Active Directory · Entra ID · PowerShell
 
🎓 B.S. Information Technology, WGU

![Security+](https://img.shields.io/badge/CompTIA-Security%2B-C8202F?style=flat-square)
![Cloud+](https://img.shields.io/badge/CompTIA-Cloud%2B-C8202F?style=flat-square)
![Network+](https://img.shields.io/badge/CompTIA-Network%2B-C8202F?style=flat-square)
![A+](https://img.shields.io/badge/CompTIA-A%2B-C8202F?style=flat-square)
![AWS Cloud Practitioner](https://img.shields.io/badge/AWS-Cloud%20Practitioner-FF9900?style=flat-square)
![Linux Essentials](https://img.shields.io/badge/LPI-Linux%20Essentials-333333?style=flat-square)
![ITIL 4 Foundation](https://img.shields.io/badge/ITIL%204-Foundation-5A2D82?style=flat-square)
<br><sub>In progress: Microsoft SC-300 (Identity and Access Administrator)</sub>


---

## ⭐ Featured Projects

Labs on one fictional defense contractor, **Potomac Defense Systems**. Each picks up the gaps the last one found.

| Project | What I built | Status |
|---|---|:---:|
| **[Hybrid IAM JML Lab](https://github.com/jagble/hybrid-iam-jml-lab)**<br><sub>Automated Joiner-Mover-Leaver for AD + Entra ID</sub> | A PowerShell engine that gives people access on day one, changes it when their job changes, and removes it when they leave, across AD and Entra ID | ✅ Complete<br><sub>[6-part walkthrough](https://github.com/jagble/hybrid-iam-jml-lab#what-i-built)</sub> |
| **[Zero Trust IAM Lab](https://github.com/jagble/zero-trust-iam-lab)**<br><sub>Conditional Access, PIM and Access Governance in Entra ID</sub> | Closes Project 1's gaps: Conditional Access, just-in-time admin, request-and-approval access, access reviews, incident response | 🚧 6 of 8 parts |
| **[Federated SSO and PKI Lab](https://github.com/jagble/federated-sso-pki-lab)**<br><sub>AD FS to Entra Migration, SAML, OIDC and Certificate-Based Auth</sub> | Moves apps off AD FS to Entra ID, adds SAML and OIDC apps, SCIM provisioning, and certificate sign-in backed by an internal PKI (the lab version of CAC/PIV) | 📋 Planned |

---

## 🎯 Real-World Scenarios
 
Problems IAM teams deal with, what I did about each one, and where to see it.
 
| Scenario | What I did | Evidence |
|---|---|---|
| **A fired employee can still get in** | Measured how long a terminated user kept cloud access: the old password still worked at 79 seconds. Made offboarding revoke sessions and force a sync, cutting the cloud disable lag from ~29 minutes to ~3 | [Leaver Offboarding & Exposure Window](https://github.com/jagble/hybrid-iam-jml-lab/blob/main/parts/1.5-lifecycle-automation/README.md#5-leaver-and-the-exposure-window) |
| **300 new hires start on the same day** | Created 306 accounts in one run from an HR file, each with the right role groups, checked against a pre-written answer key | [Provisioning Scale test](https://github.com/jagble/hybrid-iam-jml-lab/blob/main/parts/1.5-lifecycle-automation/README.md#9-scale-test-340-people) |
| **A Domain Admin hidden in a nested group** | Built a review that follows group nesting. It found the Domain Admin path I planted, plus two problems I didn't plant | [Privileged access review](https://github.com/jagble/hybrid-iam-jml-lab/blob/main/parts/1.6-security-review/README.md) |
| **One person can create a vendor and pay it** | Blocked anyone holding both Finance and Accounts Payable access: found by a script in Project 1, refused at request time in Project 2 | [LifeCycle SoD Enforcement](https://github.com/jagble/hybrid-iam-jml-lab/blob/main/parts/1.5-lifecycle-automation/README.md#7-separation-of-duties) | [Request-Time SoD Enforcement](https://github.com/jagble/zero-trust-iam-lab/blob/main/parts/2.4-access-packages/README.md#4-finance-payables-and-separation-of-duties) |
| **Admins hold Global Admin 24/7** | Removed standing admin access, including mine. Global Admin now needs MFA, a reason and a second person's approval, and expires after 1 hour | [Privileged Identity Management](https://github.com/jagble/zero-trust-iam-lab/blob/main/parts/2.3-privileged-identity-management/README.md) |
| **An engineer needs temporary access to sensitive program data** | Request goes to the manager, then the program manager. Access is granted automatically and ends after 90 days | [Access request](https://github.com/jagble/zero-trust-iam-lab/blob/main/parts/2.4-access-packages/README.md#6-test-1-chris-requests-radar) |
| **A helpdesk tech kept admin rights after a ticket** | A quarterly review flagged the extra role, Security denied it, and it was removed automatically | [Access review & Remediation](https://github.com/jagble/zero-trust-iam-lab/blob/main/parts/2.5-access-reviews/README.md#5-test-1-monica-reviews-admin-roles) |
| **Someone uses the emergency account or weakens a security policy** | Email alerts on any break-glass sign-in and any change to Conditional Access policies or their exclusion groups | [Conditional Access Monitoring & Alerts](https://github.com/jagble/zero-trust-iam-lab/blob/main/parts/2.2-conditional-access/README.md#10-alerts) |
| **An employee's account is compromised** | Rebuilt the timeline from the logs, confirmed one account was affected, and contained it in 11 minutes. Found that passing MFA marked the risk as resolved, and added an alert for it | [Incident response](https://github.com/jagble/zero-trust-iam-lab/blob/HEAD/parts/2.6-incident-response/README.md) · [Incident report](https://github.com/jagble/zero-trust-iam-lab/blob/HEAD/docs/03-incident-report-maria-lopez.md) |
 
---
 
## 🛠️ Skills & Tools
 
| Area | What I've used |
|---|---|
| **Identity & Access Management** | `Active Directory` `Entra ID` `Entra Connect Sync` `Hybrid Identity` `RBAC` `JML Lifecycle` `Separation of Duties` `Group Policy` |
| **Zero Trust** | `Conditional Access` `MFA` `Passkeys` `Phishing-Resistant MFA` `Identity Protection` `Break-Glass Accounts` `Named Locations` |
| **Privileged Access** | `PIM` `Just-in-Time Access` `Approval Workflows` `Admin Tiering` `Delegated Administration` `Privileged Access Review` `gMSA` |
| **Identity Governance** | `Entitlement Management` `Access Packages` `Multi-Stage Approvals` `Time-Limited Access` `SoD Rules` |
| **Automation** | `PowerShell` `Microsoft Graph API` `Certificate-Based App Auth` `Python` |
| **Monitoring & Logging** | `Log Analytics` `KQL` `Azure Monitor Alerts` `Entra Sign-in Logs` `Entra Audit Logs` `Windows Event Logs` |
| **Cloud & Infrastructure** | `Microsoft Azure` `Azure VMs` `Windows Server` `DNS` `DHCP` `Network Security Groups` `Wireshark` |
| **IT Service Management** | `osTicket` `SLAs` `Ticket Routing & Escalation` `ITIL 4` |
 

 
---

## Earlier Projects

| Project | What I built |
|---|---|
| **[Active Directory Lab](https://github.com/jagble/configure-ad)** | Windows Server domain controller in Azure, 10,000+ users bulk-created with PowerShell, account lockout and access policies with Group Policy |
| **[osTicket Help Desk](https://github.com/jagble/osticket-prereqs)** | Ticketing system with SLA tiers, routing and escalation, worked from intake to resolution · [Setup](https://github.com/jagble/osticket-prereqs) · [Configuration](https://github.com/jagble/osticket-post-installaion) · [Ticket Lifecycle](https://github.com/jagble/osticket-ticket-simulation) |
| **[Azure Networking & Packet Analysis](https://github.com/jagble/Azure-Compute-and-Networking)** | Azure VMs and Wireshark to inspect DNS, DHCP, ICMP, RDP and SSH traffic and test Network Security Group rules |

---

## Contact

[![Email](https://img.shields.io/badge/Email-joshuaagble%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:joshuaagble@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-joshagble-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/joshagble/)
