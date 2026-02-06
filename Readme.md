# Identity and Server Operations

## Overview
This repository documents hands-on labs focused on **enterprise identity management and core server operations** using Microsoft Active Directory. The work demonstrates how identity infrastructure is **built, structured, secured, validated, and operated** in a virtualised environment.

The emphasis is on **operational correctness, clarity of design, and real-world administrative practices**, rather than advanced tooling or theoretical implementations.

---

## Repository Structure
The repository is organised to reflect how identity systems are implemented and consumed in real environments:

- **Labs 01–02:** Domain-side (host) identity build and design
- **Lab 03:** Client-side domain consumption and validation
- **Lab 04:** Basic Active Directory operational automation

Each lab is documented independently and focuses on a specific responsibility area.

---

## Labs Included

### Lab 01 — Active Directory Domain Build (Host)
**Focus:** Foundational identity infrastructure

This lab covers the deployment and validation of a Windows Server 2022 Domain Controller, including:
- Active Directory Domain Services (AD DS) installation
- AD-integrated DNS configuration
- Domain creation and verification
- Domain-wide password and authentication policy
- Validation of core services (DNS, SYSVOL, NETLOGON)
- Domain health checks and readiness for client integration

This lab establishes the **authentication backbone** of the environment.

---

### Lab 02 — OU, Users, and Group Design (Host)
**Focus:** Identity structure and authorisation

This lab builds on the domain foundation and focuses on enterprise identity design:
- Organisational Unit (OU) structure by **location and function**
- Separation of **users, groups, and computer objects**
- Centralised server object management
- Security vs distribution group usage
- Group-based authorisation model (User → Group → Resource)
- Delegation-ready OU structure for operational separation

This lab defines **how identities are managed and controlled**, not just created.

---

### Lab 03 — Client Domain Join & Validation (Client)
**Focus:** Domain consumption and authentication validation

This lab introduces a Windows client system and validates that the domain functions as intended when consumed by end-user machines:
- Client DNS alignment with the domain controller
- Domain join process and computer account creation
- Placement of client objects into the correct OUs
- Domain user authentication on a non-server OS
- Validation of identity, group membership, and policy scope

This lab proves the domain is **usable and functional**, not only built.

---

### Lab 04 — Active Directory Operations Automation (Basic)
**Focus:** Reducing repetitive administrative tasks

This lab demonstrates **basic Active Directory automation** using PowerShell to perform common operational tasks that are normally handled manually through ADUC.

Automation in this lab is intentionally:
- Readable
- Limited in scope
- Administrator-initiated
- Focused on bulk and hygiene operations

Tasks include:
- Bulk user creation from CSV
- Adding users to security groups
- Disabling inactive user accounts

This lab demonstrates an **automation mindset** without over-claiming advanced tooling or frameworks.

---

## Environment
- Windows Server 2022 (Domain Controller)
- Windows Client OS (Lab 03)
- Active Directory Domain Services (AD DS)
- AD-integrated DNS
- VMware (virtualised lab environment)

---

## Skills Demonstrated
- Enterprise identity and access management fundamentals
- Active Directory domain architecture and validation
- Organisational Unit (OU) and identity lifecycle design
- Group-based security and authorisation
- Domain-wide authentication policy enforcement
- Client-domain interaction and authentication validation
- Active Directory operational hygiene
- Basic PowerShell automation for identity operations
- Clear technical documentation and troubleshooting

---

## Design Philosophy
- Build identity infrastructure **before** consuming it
- Separate authentication, authorisation, and operations
- Prefer group-based access over direct user permissions
- Automate **repetition**, not decision-making
- Keep automation simple, explainable, and safe
- Document systems so another administrator can understand them quickly

---

## Notes
Each lab contains its own README and supporting evidence.
Future extensions may include Group Policy enforcement, file services, and more advanced automation once operational scale justifies it.
