# Lab 04 — Active Directory Operations Automation (Basic)

## Purpose
This lab demonstrates **basic Active Directory operational automation** using PowerShell to reduce repetitive administrative tasks. The focus is on automating **common, low-risk actions** that are routinely performed through Active Directory Users and Computers (ADUC).

Automation in this lab supports operations; it does not replace administrative decision-making.

---

## Scope
- Bulk user account creation
- Group membership management
- User account hygiene (inactive accounts)
- Readable, administrator-initiated scripts

---

## Automation Tasks

### Bulk User Creation
User accounts are created in bulk from a structured input file rather than being added manually one at a time.

📄 **Artifact**
- `create-users-from-csv.ps1`
- `users.csv`

---

### Group Membership Management
Users are added to security groups programmatically to enforce **group-based authorisation**.

📄 **Artifact**
- `add-users-to-groups.ps1`

---

### Account Hygiene
Inactive user accounts are identified and disabled to reduce security risk and administrative overhead.

📄 **Artifact**
- `disable-inactive-users.ps1`

---

## Design Notes
- Scripts are executed manually by an administrator
- Tasks mirror existing ADUC workflows
- Automation is limited to clearly understood operations
- Group-based access control is preserved
- No changes occur without explicit execution

---

## Validation
- Users appear in the correct OUs after creation
- Group membership reflects intended access
- Inactive accounts are disabled without affecting active users

---

## Outcome
Routine identity operations can now be performed **consistently and efficiently** without repetitive manual interaction, while retaining full administrative control.

---

## Design Insight
Effective automation in Active Directory begins with **bulk operations and account hygiene**, not complex frameworks.
