# Lab 01 — Active Directory Domain Build

## Purpose
This lab demonstrates the **deployment and validation of a functional Active Directory domain** on Windows Server 2022. The focus is on confirming that core identity services are operational and ready for use, not on installation steps.

---

## Scope
- Domain Controller deployment
- AD-integrated DNS
- Domain-wide authentication policy
- Core service validation

---

## Domain Configuration
- Domain Controller: Windows Server 2022
- Domain: `ShaneAd.local`
- DNS hosted on the Domain Controller
- Single-DC lab scope

![dom](ShaneAd-IP-Dns.png)
- Domain visible in Active Directory Users and Computers


---

## Core Services Validation
The following services confirm a healthy domain controller:

![Sysol](net-share-sysvol.png)
- SYSVOL and NETLOGON shares present
`evidence/sysvol-netlogon.png`

- Active Directory–integrated DNS zones
`evidence/ad-dns-zones.png`

---

## Authentication Baseline
A domain-wide password policy is enforced to ensure consistent authentication standards.

![SEC](Domain-Level-SEC.png)
- Password and account policy configured at domain level
`evidence/domain-password-policy.png`

---

## Health Checks
Built-in validation tools were used to confirm domain readiness.

![SEC](Dcdiag-summary.png)
- Domain Controller diagnostics (`dcdiag`) with no critical errors
`evidence/dcdiag.png`

---

## Validation Summary
- Domain services are running
- DNS resolution supports Active Directory
- Authentication policy is enforced
- Domain is ready for client integration

---

## Outcome
The environment now provides a **stable identity foundation** upon which user management, policy enforcement, and client systems can be introduced.

---

## Design Insight
Active Directory should be validated for service health and security **before** introducing clients or higher-level operations.
