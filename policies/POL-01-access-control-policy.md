# POL-01 — Access Control Policy

| | |
|---|---|
| **Organization** | CivicStack Solutions LLC |
| **Version** | 2.1 · **Effective** 2026-09-15 · **Next review** 2027-09-15 |
| **Owner** | CISO · **Approved by** CEO |
| **Applies to** | All CivicStack workforce and all customer users (including CMHA caseworkers) of systems that store or process customer data, including the Housing Assistance Portal (HAP) |
| **Implements** | NIST SP 800-53 Rev 5 AC-1, AC-2, AC-3, AC-6, AC-7, AC-11, AC-17, IA-2, IA-5, PS-4, PS-5 · ISO/IEC 27001:2022 A.5.15–A.5.18, A.8.2, A.8.3, A.8.5 |

Each clause ends with the controls it satisfies, so an assessor can trace any requirement back to policy in a single step.

---

## 1. Purpose

**1.1** This policy sets the rules for granting, using, reviewing and removing access to CivicStack systems and customer data, so that every user has only the access their job requires and every action can be traced to a person. — *Satisfies: AC-1(a)(1) · ISO A.5.15*

## 2. Roles

**2.1** The **CISO** owns this policy, reviews it annually and after any significant incident or audit finding, and approves exceptions. — *Satisfies: AC-1(b), AC-1(c) · ISO A.5.2*

**2.2** **System owners** define the roles for their system, the privileges in each role, and who may approve each role. — *Satisfies: AC-2(a), AC-2(c) · ISO A.5.15*

**2.3** The **IAM Engineer** provisions, modifies and removes accounts only on an approved request, and performs the monthly reconciliation in §4.7. — *Satisfies: AC-2(b) · ISO A.5.18*

## 3. Principles

**3.1** **Least privilege.** Access is granted at the minimum level needed for the user's assigned duties, for customer data scoped to the user's jurisdiction or office. — *Satisfies: AC-6, AC-6(5) · ISO A.8.3*

**3.2** **Separation of duties.** No one person may both request and approve their own access, or both make and approve a production change. — *Satisfies: AC-5 · ISO A.5.3*

**3.3** **Unique identity.** Every user has an individual account. Shared and group accounts are prohibited except the vaulted break-glass credential in §6. — *Satisfies: AC-2(a), IA-2, IA-4 · ISO A.5.16*

## 4. Account lifecycle

**4.1** Account types are limited to: workforce, customer user, service (non-person) and break-glass. Each service account has a named human owner. — *Satisfies: AC-2(a), IA-4 · ISO A.5.16*

**4.2** Accounts are created **only after** documented approval by the requester's supervisor of record (CMHA) or engineering manager (CivicStack). The approved role is the role provisioned. — *Satisfies: AC-2(e), AC-2(d) · ISO A.5.18*

**4.3** Customer users are provisioned from role templates scoped by office. Statewide access (`case:read:all`) requires CMHA ISSO approval and expires after 90 days. — *Satisfies: AC-6(5), AC-2(d) · ISO A.8.3*

**4.4** Role changes are handled as a new request. Access no longer needed in the new role is removed within 5 business days. — *Satisfies: AC-2(f), PS-5 · ISO A.5.18*

**4.5** Accounts inactive for **35 days (privileged)** or **90 days (standard)** are disabled automatically. Customer-user accounts with no sign-in for 14 days are disabled pending reconfirmation. — *Satisfies: AC-2(3) · ISO A.5.18*

**4.6** On separation, access is disabled within **24 hours**, or **8 hours** for privileged users. Separations are fed automatically from the HR system of record (SCIM for CMHA, HRIS for CivicStack). — *Satisfies: PS-4(a), AC-2(h) · ISO A.6.5, A.5.18*

**4.7** Each month the IAM Engineer reconciles active accounts against the HR systems of record, with a named backup performer, by the 5th business day. Exceptions are disabled the same day and reported to the Security Lead. — *Satisfies: AC-2(j), PS-4 · ISO A.5.18*

**4.8** Privileged entitlements are recertified **quarterly** by a reviewer who neither holds nor reports to the holder of the entitlement under review. Revocations are completed within 5 business days. — *Satisfies: AC-6(7), AC-2(j) · ISO A.5.18, A.8.2*

## 5. Authentication

**5.1** Privileged access requires phishing-resistant MFA (FIDO2). Workforce access to any system holding customer data requires MFA. — *Satisfies: IA-2(1), IA-2(2) · ISO A.8.5*

**5.2** Passwords are at least 12 characters, screened against breached-password lists when set and at next sign-in, stored only as salted hashes, and not rotated on a schedule unless compromise is suspected. — *Satisfies: IA-5(1) · ISO A.5.17*

**5.3** After 5 consecutive failed sign-ins the account is locked for 30 minutes. Sessions lock after 15 minutes of inactivity and end after 12 hours. — *Satisfies: AC-7, AC-11, AC-12 · ISO A.8.5*

## 6. Privileged and emergency access

**6.1** Administrative access to production is granted just-in-time through the privileged access management (PAM) tool, for no more than 4 hours, and logged. — *Satisfies: AC-2(1), AC-6(1), AC-6(9) · ISO A.8.2*

**6.2** The break-glass credential is vaulted. Checking it out alerts the Security Lead, who reviews the session and records sign-off within 2 business days. — *Satisfies: AC-2(2), AU-6 · ISO A.8.2, A.8.15*

## 7. Remote access

**7.1** Remote administrative access is only through the managed session service. No inbound SSH or RDP is exposed. Operator devices must pass a posture check. — *Satisfies: AC-17, AC-17(1), AC-17(3) · ISO A.6.7, A.8.1*

## 8. Exceptions and enforcement

**8.1** Exceptions must be requested in writing, risk-assessed, approved by the CISO, and expire within 12 months. They are tracked in the exception register. — *Satisfies: AC-1(a)(1), PM-9 · ISO A.5.36*

**8.2** Violations may lead to removal of access and disciplinary action under the HR policy. — *Satisfies: PS-8 · ISO A.6.4*
