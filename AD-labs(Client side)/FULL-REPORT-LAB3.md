# Lab 03 — Client Domain Join & Validation

## Purpose
This lab validates that the Active Directory domain built in Lab 01 and structured in Lab 02 can be **consumed by a client system**. The focus is on authentication, DNS dependency, and correct object placement within the domain.

---

## Scope
- Client system integration with Active Directory
- DNS-based domain discovery
- Domain authentication on a non-server OS
- Computer object placement into correct OUs

---

## Client Configuration
- Client OS: Windows (client edition)
- Joined to domain: `ShaneAd.local`
- DNS configured to point to the Domain Controller

📸 **Evidence**
- Client network configuration showing DNS set to Domain Controller
`evidence/client-dns-config.png`

---

## Domain Join Validation
The client successfully joins the domain and establishes a secure trust relationship.

📸 **Evidence**
- Successful domain join confirmation
`evidence/domain-join-success.png`

---

## Computer Object Management
After joining the domain, the client computer account is visible in Active Directory and moved into the appropriate **Workstations OU**.

📸 **Evidence**
- Computer object visible in ADUC
`evidence/client-object-aduc.png`
- Computer object placed in correct OU
`evidence/client-moved-to-ou.png`

---

## User Authentication Validation
Domain users are able to authenticate on the client system using domain credentials.

📸 **Evidence**
- Domain user login on client machine
`evidence/domain-user-login.png`

---

## Validation Summary
- Client successfully discovers the domain via DNS
- Secure domain trust established
- Computer object correctly managed within OU structure
- Domain user authentication confirmed

---

## Outcome
The Active Directory domain is now **fully functional and consumable** by client systems, validating the correctness of domain services, identity structure, and authentication flow.

---

## Design Insight
A domain is only proven functional once clients can discover it via DNS and authenticate using domain identities.
