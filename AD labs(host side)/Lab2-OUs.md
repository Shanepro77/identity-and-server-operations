# Lab 02 — OU, Users, and Group Design

## Purpose
This lab demonstrates **practical identity organisation and authorisation design** in Active Directory using OUs, users, and groups. The focus is on **structure, separation, and correctness**, validated through ADUC evidence.

---

## Scope
- Organisational Unit (OU) structure
- User identity placement
- Group-based authorisation
- Preparation for delegation and Group Policy

---

## OU Structure
OUs are organised by **location and function**, with clear separation between identity, machines, and servers.

![OU](OU-structure.png)
- OU hierarchy showing locations, Users, Workstations, Groups, and centralised Servers


---

## User Accounts
User accounts are created within their respective **location-based Users OUs**.

![OUuser](OU-users.png)
- Sample users visible inside a location Users OU


---

## Groups & Authorisation
Security groups are used to control access and administration.
Users are assigned to groups; permissions are not assigned directly to users.

![group](OU-groups.png)
- Security groups visible in Groups OU
`evidence/security-groups.png`
- User “Member Of” tab showing group membership
`evidence/user-group-membership.png`

---

## Design Decisions (Brief)
- Users represent **identity**
- Groups represent **access**
- Servers are managed **centrally**, not per location
- Workstations are separated from users for policy targeting

---

## Validation
- Users are located in correct OUs
- Group membership reflects intended roles
- No direct permissions applied to user accounts
- OU structure supports delegation and GPO scope

---

## Outcome
The domain now has a **clean, scalable identity and authorisation structure**, ready for:
- client domain joins
- Group Policy application
- delegated administration
- basic automation

---

## Design Insight
A clear OU and group structure reduces administrative risk and simplifies long-term identity operations.
