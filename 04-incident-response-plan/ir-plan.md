# MedCaribe Health Group — Incident Response Plan

**Document Classification:** Confidential — Incident Response Team Only  
**Version:** 1.0  
**Date:** March 2026  
**Author:** Jelani D. Maitland  
**Review Cycle:** Annual and after each Critical/High incident

---

## 1. Purpose

This plan provides step-by-step procedures for MedCaribe Health Group to detect, respond to, contain, and recover from cybersecurity incidents. It operationalizes the Incident Response Policy (POL-003) and follows the NIST SP 800-61 incident response lifecycle.

---

## 2. Incident Response Team

### 2.1 Core Team

| Role | Primary | Alternate | Contact |
|------|---------|-----------|---------|
| Incident Coordinator | K. Rampersad (Operations Manager) | S. Mohammed (Finance Manager) | [phone] / [email] |
| Technical Lead | M. Doyle (IT Administrator) | Incident Coordinator acts as liaison if IT unavailable | [phone] / [email] |
| Decision Authority | Dr. A. Dorian (Medical Director) | K. Rampersad (Operations Manager) for non-critical decisions | [phone] / [email] |
| Communications Lead | K. Rampersad (Operations Manager) | Dr. A. Dorian (Medical Director) | [phone] / [email] |

### 2.2 Extended Contacts

| Contact Type | Organization/Name | Contact Details | When to Engage |
|-------------|-------------------|-----------------|----------------|
| External IR Support | [To be identified — cybersecurity firm] | [TBD] | Critical incidents requiring forensic investigation |
| Legal Counsel | [To be identified] | [TBD] | Data breaches requiring regulatory notification |
| Insurance (Cyber) | [If applicable — cyber insurance broker] | [TBD] | Any incident likely to result in a claim |
| Law Enforcement | TTPS Cyber Crime Unit | [TBD] | Criminal activity (fraud, extortion, deliberate theft) |
| Information Commissioner | Office of the Information Commissioner | [TBD] | Confirmed personal data breaches requiring notification |
| Microsoft Support | Microsoft 365 Support | support.microsoft.com | M365-specific technical issues during incidents |

---

## 3. Phase 1 — Preparation

### 3.1 Readiness Checklist

The following must be maintained at all times:

- Incident Response Plan printed and stored in the San Fernando office secure cabinet
- All contact details current and verified quarterly
- At least one person trained in basic IR procedures available during business hours
- Break-glass admin account tested and sealed envelope intact
- M365 audit logging enabled and verified
- Backup of critical contact lists stored offline (not only in M365)

### 3.2 Detection Sources

Incidents may be detected through staff reports (phishing emails, suspicious activity, unusual system behaviour), Microsoft 365 security alerts (sign-in anomalies, impossible travel, malware detection), Microsoft Defender alerts on endpoints, external notification (vendor, insurer, client, or law enforcement), and review of audit logs during weekly checks.

---

## 4. Phase 2 — Detection and Analysis

### 4.1 Initial Triage

When a potential incident is reported or detected:

**Step 1:** Receive the report. Record who reported it, when, what they observed, and which systems or data may be affected.

**Step 2:** Make an initial assessment. Determine whether this is a confirmed incident, a suspected incident requiring investigation, or a false alarm. If false alarm, document and close.

**Step 3:** Classify severity using the table in the Incident Response Policy (Critical, High, Medium, Low).

**Step 4:** Notify the Incident Coordinator (Operations Manager). For Critical severity, also notify the Medical Director immediately.

**Step 5:** Begin the incident log. Every action taken from this point forward must be documented with timestamps.

### 4.2 Analysis Questions

The Technical Lead should determine: What systems are affected? What data may be compromised and at what classification level? How many users or patients are potentially impacted? Is the incident ongoing or has it been contained? What was the initial access vector (phishing, credential theft, malware, insider)? Is there evidence of lateral movement?

### 4.3 Incident Log Template

| Timestamp | Action | Performed By | Notes |
|-----------|--------|-------------|-------|
| [Date Time] | [Action taken] | [Name] | [Additional context] |

A fresh incident log must be started for every confirmed incident. Logs must be preserved for a minimum of 3 years.

---

## 5. Phase 3 — Containment, Eradication, and Recovery

### 5.1 Containment Procedures by Incident Type

#### Compromised Email Account

1. Immediately disable the compromised account or force sign-out from all sessions
2. Reset the account password
3. Review and revoke any suspicious OAuth app consents
4. Review mailbox rules for unauthorized forwarding or deletion rules
5. Check sent items for phishing emails sent from the compromised account
6. Notify recipients of any fraudulent emails sent
7. Review M365 sign-in logs for the account to determine scope and duration
8. If MFA was not enabled, enable immediately
9. Scan the user's workstation for malware

#### Ransomware or Malware Infection

1. Immediately disconnect the affected device from the network (pull Ethernet, disable Wi-Fi)
2. Do NOT power off the device (preserve memory evidence if possible)
3. Identify other devices that may be affected — check for lateral movement
4. If multiple devices are affected, consider disconnecting the affected location's network
5. Verify that backups are intact and have not been compromised
6. Contact external IR support for Critical severity
7. Do NOT attempt to decrypt or negotiate without Medical Director authorization
8. Restore from known-good backup after eradication is confirmed

#### Unauthorized Access to Patient Records

1. Disable the account(s) used for unauthorized access
2. Document which records were accessed, by whom, and when (from audit logs)
3. Determine whether this was accidental (excessive permissions) or deliberate
4. Assess whether data was exfiltrated or only viewed
5. If personal data was compromised, initiate data breach assessment process
6. Notify the Medical Director for regulatory notification decision

#### Data Leakage (Personal Email, WhatsApp, USB)

1. Identify the scope of data exposed and its classification level
2. Request the involved staff member to delete the data from personal devices/accounts (and verify where possible)
3. Determine whether the data reached any unintended third parties
4. If RESTRICTED data (patient records) was exposed externally, treat as a potential data breach
5. Implement technical controls to prevent recurrence (block forwarding, USB policy)

#### Vendor Security Incident

1. Contact the vendor to understand the scope and nature of the incident
2. Determine what MedCaribe data was potentially affected
3. Request the vendor's incident report and timeline
4. Assess impact on MedCaribe patients and operations
5. Activate breach notification process if patient data is confirmed compromised
6. Document vendor cooperation and response quality for future vendor risk review

### 5.2 Recovery

After the threat has been eradicated, restore affected systems from known-good backups. Re-enable disabled accounts only after confirming they are secure (new passwords, MFA enabled). Monitor restored systems closely for 30 days for signs of re-compromise. Verify data integrity after restoration.

---

## 6. Phase 4 — Post-Incident Activity

### 6.1 Post-Incident Review

A formal post-incident review must be conducted within 14 days of incident closure for all Critical and High incidents. The review must address: what happened (root cause and timeline), what went well, what did not work or was missing, specific improvements to implement, updates to the risk register, and updates to this plan.

### 6.2 Post-Incident Review Attendees

All Incident Response Team members who participated, the Medical Director (for Critical incidents), and any external support providers involved.

### 6.3 Deliverables

A written incident report including timeline, root cause, impact assessment, actions taken, and recommended improvements. This report is classified as CONFIDENTIAL and stored securely.

---

## 7. Communication Templates

### 7.1 Internal Staff Notification (During Incident)

Subject: Security Notice — Action Required

Team, we are currently addressing a security matter that affects [system/service]. While we investigate, please [specific instructions — e.g., do not open email from X, change your password, do not use system Y]. If you notice anything unusual, report it immediately to [contact]. We will provide an update by [timeframe]. Thank you for your cooperation.

— [Incident Coordinator name]

### 7.2 Patient Notification (If Data Breach Confirmed)

Subject: Important Notice Regarding Your Information

Dear [Patient Name], we are writing to inform you that MedCaribe Health Group recently identified a security incident that may have affected some of your personal information. We take the protection of your information very seriously and want to provide you with the details of what happened, what information was involved, and what steps we are taking. [Details]. We recommend that you [specific protective steps]. If you have questions, please contact us at [number/email]. We sincerely apologize for any concern this may cause.

— Dr. A. Dorian, Medical Director

### 7.3 Regulator Notification (Information Commissioner)

This notification must be drafted by the Medical Director with support from legal counsel. It should include the nature of the incident, the personal data affected, the number of individuals impacted, measures taken to address the incident, and measures taken to mitigate harm to affected individuals.

---

## 8. Data Breach Assessment Criteria

When an incident involves personal data, use the following criteria to determine whether regulatory notification is required:

| Factor | Assessment |
|--------|------------|
| Was personal data actually accessed or exfiltrated (not just exposed)? | Yes / No / Unknown |
| What type of personal data? (medical records carry higher severity) | Description |
| How many individuals are affected? | Count or estimate |
| Is the data encrypted or otherwise protected? | Yes / No |
| Has the data appeared publicly or been shared with unauthorized parties? | Yes / No / Unknown |
| What is the potential harm to affected individuals? | Low / Medium / High |

If the assessment indicates a confirmed or likely breach of personal data with potential harm to individuals, the Medical Director must authorize notification to the Office of the Information Commissioner.

---

## 9. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | J. Maitland | Initial version |

**Next Review:** March 2027, after each Critical/High incident, or upon significant organizational change.
