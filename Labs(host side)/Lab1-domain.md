# Lab 01 — Active Directory Domain Build

## Overview
This lab documents the **design, deployment, and validation** of an Active Directory domain using Windows Server 2022. The focus is on establishing a **stable, secure identity foundation** that is ready for client integration and operational use.

The lab emphasises correctness, service dependency awareness, and verification of core domain functionality.

---

## Objectives
- Deploy a Windows Server 2022 Domain Controller
- Create a DNS-backed Active Directory domain
- Enforce a baseline domain-wide authentication policy
- Validate core Active Directory services and domain health
- Prepare the domain for client consumption

---

## Environment
- Windows Server 2022
- Active Directory Domain Services (AD DS)
- AD-integrated DNS
- VMware virtualised environment

---

## Domain Design
- **Domain Name:** ShaneAd.local
- **Single Domain Controller** (lab scope)
- DNS hosted on the Domain Controller
- Static server identity suitable for directory services

The domain is designed as a **central identity authority**, not a general-purpose server.

---

## Core Configuration Summary
The following components were configured as part of the domain build:

- Active Directory Domain Services installation
- Domain creation and promotion to Domain Controller
- DNS role installation and AD integration
- SYSVOL and NETLOGON share creation
- Domain-wide password and authentication policy

All configuration choices align with standard Active Directory best practices.

---

## Security Baseline
A **domain-wide password policy** was configured to enforce consistent authentication standards across all domain users.

Policy considerations included:
- Minimum password length
- Password complexity enforcement
- Password history and rotation

The policy is applied at the **domain level**, ensuring uniform enforcement.

---

## Validation & Health Checks
Domain functionality was validated using built-in tools and service checks, including:

- Verification of SYSVOL and NETLOGON shares
- DNS zone presence and AD service records
- Domain Controller diagnostic checks
- Confirmation of domain readiness for client joins

These checks confirm the domain is **operational and stable**, not just installed.

---

## Outcome
At the conclusion of this lab:
- The domain is fully functional
- Core identity services are operational
- Authentication policies are enforced
- The environment is ready for client systems and further identity design

This lab establishes the **foundation upon which all subsequent identity and server operations depend**.

---

## Design Insight
A reliable identity system is built by validating service dependencies and enforcing baseline security **before** introducing clients or automation.
