# MedCaribe Health Group — Access Control Policy

**Document Classification:** Internal — Management and IT  
**Policy ID:** POL-002  
**Version:** 1.0  
**Effective Date:** March 2026  
**Approved By:** Dr. A. Dorian, Medical Director  
**Review Cycle:** Annual  
**Owner:** IT Administrator (with oversight by Operations Manager)

---

## 1. Purpose

This policy establishes requirements for managing user identities, authentication, and authorization across all MedCaribe Health Group systems. It ensures that access to patient data, financial information, and organizational resources is granted based on the principle of least privilege and is properly controlled throughout the user lifecycle.

This policy addresses risks identified in the MedCaribe Risk Register: RISK-001 (Business Email Compromise), RISK-003 (Unauthorized EHR Access), RISK-007 (Excessive Admin Privileges), and RISK-015 (Shared Credentials).

---

## 2. Scope

This policy applies to all systems that require user authentication, including Microsoft 365, CloudMed EHR, QuickBooks Online, insurance portals, network access, and any future systems. It covers all user accounts including employee accounts, contractor accounts, administrative accounts, service accounts, and shared or generic accounts.

---

## 3. Account Management

### 3.1 Account Provisioning (Onboarding)

All new user accounts must be requested by the hiring manager using the New User Access Request Form. The IT Administrator will create accounts based on the user's role and the access matrix (Section 5). Accounts will be provisioned with the minimum access required for the user's job function.

No account will be created without documented management approval.

### 3.2 Account Modification

Changes to user access (role changes, transfers, additional system access) must be requested in writing by the user's manager. The IT Administrator will verify the request and adjust access accordingly. Previous access that is no longer required must be removed at the time of the change.

### 3.3 Account Deprovisioning (Offboarding)

When a staff member departs MedCaribe — whether through resignation, termination, or contract end — the following must occur within 24 hours of their last working day:

- Microsoft 365 account disabled (not deleted — retain for 90 days for potential data recovery and legal holds)
- CloudMed EHR account disabled
- QuickBooks access revoked
- Insurance portal passwords changed if the departing user had access
- Any shared credentials the user was aware of must be rotated
- Physical keys and access cards collected
- Personal devices removed from any authorized device lists

The Operations Manager is responsible for notifying the IT Administrator of all departures. HR must confirm departure dates.

### 3.4 Shared and Generic Accounts

Shared accounts (such as reception@medcaribe.tt or lab@medcaribe.tt) are prohibited for any system that accesses patient data, financial data, or sensitive information.

Existing shared accounts must be migrated to individual accounts within 90 days of this policy's effective date. Where a shared mailbox is operationally necessary (such as a general enquiry address), it must be configured as a Microsoft 365 Shared Mailbox with individual user access — not a shared login.

### 3.5 Account Reviews

The IT Administrator will conduct a quarterly review of all user accounts across M365, CloudMed EHR, and QuickBooks to verify that all active accounts correspond to current employees or authorized contractors, no dormant accounts exist (no login in 45+ days without documented leave), and access levels remain appropriate for current roles.

Results of each review will be documented and provided to the Operations Manager.

---

## 4. Authentication Requirements

### 4.1 Passwords

All passwords must meet the following minimum requirements: at least 12 characters in length, containing a mix of uppercase letters, lowercase letters, numbers, and special characters. Passwords must be unique to each system and must not be reused across personal and work accounts.

Passwords must not be written down, stored in unencrypted files, or shared with anyone. A password manager approved by the IT Administrator may be used to store credentials securely.

### 4.2 Multi-Factor Authentication (MFA)

MFA is mandatory for all users on all systems that support it. This includes all Microsoft 365 accounts (no exceptions), CloudMed EHR (when supported by vendor), and QuickBooks Online.

MFA must use the Microsoft Authenticator app or equivalent approved authenticator. SMS-based MFA is acceptable only as a temporary fallback during initial enrollment.

Administrative accounts must use phishing-resistant MFA methods where available.

### 4.3 Session Management

Users must lock their workstation when stepping away (Windows key + L). Automatic screen lock must be configured to activate after 10 minutes of inactivity. Active sessions on shared workstations (such as front desk) must be logged out at the end of each user's shift.

---

## 5. Role-Based Access Matrix

Access to systems is granted based on role. The following matrix defines the standard access levels:

| Role | Microsoft 365 | CloudMed EHR | QuickBooks | Insurance Portals | Admin Console |
|------|--------------|--------------|------------|-------------------|---------------|
| Medical Director | Full | Full clinical | View only | No | No (separate admin account) |
| Operations Manager | Full | Administrative view | Full | View only | No (separate admin account) |
| Finance Manager | Full | No | Full | No | No |
| Clinic Manager | Full | Clinical (own location) | View only | No | No |
| Physician | Full | Full clinical | No | No | No |
| Nurse | Standard | Clinical (limited) | No | No | No |
| Lab Technician | Standard | Lab module only | No | No | No |
| Billing/Admin | Standard | Administrative view | View only | Full (individual account) | No |
| Reception | Standard | Scheduling only | No | No | No |
| IT Administrator | Standard (daily) | No | No | No | Full (dedicated admin account only) |

This matrix will be reviewed and updated whenever new roles or systems are added.

---

## 6. Privileged Access Management

### 6.1 Dedicated Admin Accounts

All administrative access must use dedicated admin accounts that are separate from daily-use accounts. Admin accounts must follow the naming convention admin.[username]@medcaribe.tt.

Admin accounts must not be used for email, web browsing, or any activity other than administrative tasks.

### 6.2 Admin Account Limits

The number of Global Administrator accounts in Microsoft 365 must not exceed two. Additional administrative roles (such as Exchange Administrator, User Administrator) should be assigned using least-privilege role assignments. The Medical Director and Operations Manager must not hold Global Admin rights — they will be assigned specific limited roles appropriate to their oversight needs.

### 6.3 Emergency Access (Break-Glass) Accounts

One emergency access account must be maintained with Global Admin privileges. This account must have a unique, complex password stored in a sealed envelope in the secure cabinet at the San Fernando office. It must use a non-personal email address and must not be used for daily operations. Its use must be logged and reviewed.

---

## 7. Third-Party and Remote Access

7.1 Third-party vendors requiring system access (such as the EHR vendor for support) must be granted time-limited access with the minimum privileges needed. Access must be revoked immediately after the support session.

7.2 Remote access to MedCaribe systems must be through approved methods only (M365 web apps, VPN if implemented). Access from personal devices must comply with the Acceptable Use Policy.

---

## 8. Enforcement

Violations of this policy may result in immediate suspension of access pending investigation and disciplinary action in accordance with HR procedures and the Acceptable Use Policy. Violations involving unauthorized access to patient records may be reported to the Office of the Information Commissioner under the Data Protection Act.

---

## 9. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | J. Maitland | Initial version |

**Next Review:** March 2027 or upon significant change to systems, roles, or regulatory requirements.
