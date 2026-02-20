## Troubleshooting & Lessons Learned

### 1. DNS Dependency for Domain Join
**Issue:** Domain join initially failed.  
**Root Cause:** Client DNS not pointing to Domain Controller.  
**Resolution:** Configured client DNS to use the Domain Controller IP.  
**Lesson:** Active Directory is DNS-dependent. Domain joins fail without correct DNS resolution.

---

### 2. Host vs Client Role Separation
**Issue:** Confusion between Domain Controller role and client role.  
**Lesson:** Domain Controllers provide authentication services; client systems consume them. These roles must be tested separately to validate authentication flow.

---

### 3. OU Design Over-Engineering Risk
**Issue:** Reworking OU structure unnecessarily.  
**Lesson:** OUs exist for delegation and Group Policy scope — not aesthetics. Structure should serve operational control.

---

### 4. Group-Based Authorisation Discipline
**Issue:** Initial temptation to assign permissions directly to users.  
**Resolution:** Enforced the model:
User → Group → Resource  
**Lesson:** Direct user permissions reduce scalability and increase administrative risk.

---

### 5. Computer Object Placement
**Issue:** Domain-joined computers defaulted to the default container.  
**Resolution:** Moved computer objects into the appropriate Workstations OU.  
**Lesson:** Proper OU placement is required for GPO targeting and administrative separation.

---

### 6. Domain Health Validation
Validated:
- SYSVOL and NETLOGON shares
- DNS zone integrity
- Domain Controller diagnostics (`dcdiag`)

**Lesson:** Installation success does not equal operational health. Service dependencies must be verified.

---

### 7. Automation Scope Discipline
**Issue:** Risk of overselling automation complexity.  
**Resolution:** Limited automation to bulk user creation, group management, and account hygiene.  
**Lesson:** Automation should reflect understood manual workflows. Never automate what cannot be clearly explained.

---

### 8. PowerShell Module Awareness
**Issue:** AD cmdlets failed due to missing module context.  
**Resolution:** Imported required module using:
`Import-Module ActiveDirectory`  
**Lesson:** Script execution depends on environment readiness and module availability.
