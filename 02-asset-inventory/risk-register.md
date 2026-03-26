# MedCaribe Health Group — Risk Register

**Document Classification:** Internal — Security Program  
**Version:** 1.0  
**Date:** March 2026  
**Author:** Jelani D. Maitland  
**Review Cycle:** Quarterly or upon significant environmental change

---

## 1. Purpose

This risk register identifies, scores, and prioritizes cybersecurity risks facing MedCaribe Health Group. Each risk is mapped to the relevant NIST CSF 2.0 function and category as well as the corresponding CIS Controls v8 Implementation Group 1 (IG1) safeguard.

The register serves as the primary input for security investment decisions, policy development, and remediation planning.

---

## 2. Scoring Methodology

### 2.1 Likelihood Scale

| Score | Rating | Definition |
|-------|--------|------------|
| 1 | Rare | Unlikely to occur in the next 12 months; no known incidents in similar organizations |
| 2 | Unlikely | Could occur but not expected; limited threat activity observed |
| 3 | Possible | Reasonable chance of occurring; incidents reported in similar organizations |
| 4 | Likely | Expected to occur within 12 months; common attack vector for this industry/size |
| 5 | Almost Certain | Expected to occur multiple times; actively observed in the current threat landscape |

### 2.2 Impact Scale

| Score | Rating | Definition |
|-------|--------|------------|
| 1 | Negligible | Minimal disruption; no data loss; resolved within hours |
| 2 | Minor | Limited disruption to one location or system; minor data exposure; resolved within 1 day |
| 3 | Moderate | Significant operational disruption; potential regulatory attention; recovery takes days |
| 4 | Major | Extended outage across multiple locations; confirmed data breach affecting patients; regulatory investigation likely; significant financial cost |
| 5 | Critical | Complete operational shutdown; large-scale patient data breach; regulatory penalties; reputational damage threatening business viability |

### 2.3 Risk Rating Matrix

| | Impact 1 | Impact 2 | Impact 3 | Impact 4 | Impact 5 |
|---|----------|----------|----------|----------|----------|
| **Likelihood 5** | 5 (Medium) | 10 (High) | 15 (Critical) | 20 (Critical) | 25 (Critical) |
| **Likelihood 4** | 4 (Low) | 8 (Medium) | 12 (High) | 16 (Critical) | 20 (Critical) |
| **Likelihood 3** | 3 (Low) | 6 (Medium) | 9 (High) | 12 (High) | 15 (Critical) |
| **Likelihood 2** | 2 (Low) | 4 (Low) | 6 (Medium) | 8 (Medium) | 10 (High) |
| **Likelihood 1** | 1 (Low) | 2 (Low) | 3 (Low) | 4 (Low) | 5 (Medium) |

**Risk Ratings:** Critical (16-25) = Immediate action required | High (9-15) = Priority remediation | Medium (5-8) = Planned remediation | Low (1-4) = Accept or monitor

---

## 3. Risk Register

### RISK-001: Business Email Compromise (BEC)

| Field | Detail |
|-------|--------|
| **Description** | An attacker compromises a staff email account through phishing or credential stuffing, then uses it to redirect insurance payments, send fraudulent invoices, or exfiltrate patient data. |
| **Threat Source** | External — cybercriminal (financially motivated) |
| **Vulnerability** | MFA not enforced for all users; no anti-phishing rules configured; shared mailbox accounts with weak passwords |
| **Likelihood** | 5 — Almost Certain. BEC is the number one attack vector for small healthcare organizations globally. |
| **Impact** | 4 — Major. Financial loss from redirected payments, patient data exposure, regulatory reporting obligation. |
| **Risk Score** | **20 — Critical** |
| **NIST CSF 2.0** | PR.AA (Protect — Identity Management, Authentication, and Access Control) |
| **CIS Control v8** | 6.3 — Require MFA for externally-exposed applications; 6.5 — Require MFA for administrative access |
| **Recommended Action** | Enforce MFA for all M365 accounts. Configure anti-phishing policies in Exchange Online. Eliminate shared mailbox accounts. |

---

### RISK-002: Ransomware Affecting Clinical Operations

| Field | Detail |
|-------|--------|
| **Description** | Ransomware encrypts workstations, shared files, and potentially the NAS backup, preventing access to patient records, billing systems, and appointment scheduling. |
| **Threat Source** | External — cybercriminal (ransomware operator) |
| **Vulnerability** | No immutable or offsite backup; basic endpoint protection only; no network segmentation; no tested recovery plan |
| **Likelihood** | 4 — Likely. Healthcare is the most targeted industry for ransomware globally. |
| **Impact** | 5 — Critical. All four clinics unable to operate; patient care disrupted; potential permanent data loss. |
| **Risk Score** | **20 — Critical** |
| **NIST CSF 2.0** | PR.DS (Protect — Data Security); RC.RP (Recover — Recovery Planning) |
| **CIS Control v8** | 11.1 — Establish and maintain a data recovery practice; 11.2 — Perform automated backups; 11.4 — Establish and maintain an isolated instance of recovery data |
| **Recommended Action** | Implement immutable cloud backup for M365 and critical data. Test backup restoration quarterly. Verify EHR vendor backup and recovery SLA. |

---

### RISK-003: Unauthorized Access to Patient Records via EHR

| Field | Detail |
|-------|--------|
| **Description** | Staff or former staff access patient records they are not authorized to view, either through excessive permissions, shared credentials, or accounts not disabled after departure. |
| **Threat Source** | Internal — employees and former employees |
| **Vulnerability** | No RBAC implemented in EHR; no offboarding process to disable accounts; no access logging review |
| **Likelihood** | 4 — Likely. Shared credentials and no offboarding process make this virtually certain. |
| **Impact** | 4 — Major. Violation of Data Protection Act; patient privacy breach; potential legal and regulatory consequences. |
| **Risk Score** | **16 — Critical** |
| **NIST CSF 2.0** | PR.AA (Protect — Identity Management, Authentication, and Access Control) |
| **CIS Control v8** | 5.3 — Disable dormant accounts; 6.1 — Establish an access granting process; 6.2 — Establish an access revoking process |
| **Recommended Action** | Implement formal onboarding/offboarding checklist. Configure role-based access in CloudMed EHR. Conduct quarterly access review. |

---

### RISK-004: Patient Data Leakage via WhatsApp and Personal Devices

| Field | Detail |
|-------|--------|
| **Description** | Staff share patient information (lab results, appointment details, medical notes) via personal WhatsApp accounts, creating uncontrolled copies of sensitive data on personal devices. |
| **Threat Source** | Internal — staff (unintentional; operational convenience) |
| **Vulnerability** | No approved communication channel for patient interaction; no acceptable use policy; no mobile device management |
| **Likelihood** | 5 — Almost Certain. Staff confirmed this is current practice across all locations. |
| **Impact** | 3 — Moderate. Data Protection Act violation; patient privacy breach; no ability to contain or audit. |
| **Risk Score** | **15 — Critical** |
| **NIST CSF 2.0** | PR.DS (Protect — Data Security); GV.PO (Govern — Policy) |
| **CIS Control v8** | 3.1 — Establish and maintain a data management process; 3.4 — Enforce data retention |
| **Recommended Action** | Establish acceptable use policy prohibiting patient data on personal messaging platforms. Implement a sanctioned secure communication alternative. |

---

### RISK-005: Phishing Attack Leading to Credential Theft

| Field | Detail |
|-------|--------|
| **Description** | Staff receive phishing emails designed to harvest M365 credentials, giving attackers access to email, OneDrive, and potentially EHR systems if passwords are reused. |
| **Threat Source** | External — cybercriminal |
| **Vulnerability** | No security awareness training; limited anti-phishing configuration; partial MFA deployment; likely password reuse across systems |
| **Likelihood** | 5 — Almost Certain. Phishing is the most common initial access vector globally. |
| **Impact** | 3 — Moderate. Credential compromise of one account; lateral movement potential; data exposure. |
| **Risk Score** | **15 — Critical** |
| **NIST CSF 2.0** | PR.AT (Protect — Awareness and Training); DE.CM (Detect — Continuous Monitoring) |
| **CIS Control v8** | 14.1 — Establish and maintain a security awareness program; 14.2 — Train workforce on recognizing social engineering attacks |
| **Recommended Action** | Implement quarterly security awareness training. Configure M365 anti-phishing and safe links policies. Enforce MFA organization-wide. |

---

### RISK-006: Unverified EHR Vendor Backup and Recovery

| Field | Detail |
|-------|--------|
| **Description** | CloudMed EHR vendor is assumed to maintain backups but MedCaribe has never verified the backup frequency, retention period, recovery time, or tested a restore. |
| **Threat Source** | Vendor — third-party failure |
| **Vulnerability** | No vendor SLA review; no backup verification; no documented RPO/RTO; no contractual requirement for restore testing |
| **Likelihood** | 3 — Possible. Vendor outages or data loss events do occur, particularly with smaller SaaS providers. |
| **Impact** | 5 — Critical. Permanent loss of all patient records; inability to provide continuity of care; catastrophic regulatory and legal exposure. |
| **Risk Score** | **15 — Critical** |
| **NIST CSF 2.0** | ID.SC (Identify — Supply Chain Risk Management); RC.RP (Recover — Recovery Planning) |
| **CIS Control v8** | 11.1 — Establish and maintain a data recovery practice; 15.4 — Ensure service provider contracts include security requirements |
| **Recommended Action** | Request vendor backup SLA documentation. Define RPO/RTO requirements. Request a test restore or proof of backup. Include backup requirements in vendor contract renewal. |

---

### RISK-007: Excessive Administrative Privileges

| Field | Detail |
|-------|--------|
| **Description** | Three users have Global Admin access to M365 (IT admin, Medical Director, Operations Manager), giving them full control over all data, accounts, and configurations. |
| **Threat Source** | Internal — privilege misuse or compromise |
| **Vulnerability** | No privileged access management; admin accounts used for daily work; no separation of admin and user accounts |
| **Likelihood** | 4 — Likely. Admin accounts are high-value targets; using them for daily work multiplies exposure. |
| **Impact** | 4 — Major. Compromised admin account gives attacker full control of entire M365 environment and all data. |
| **Risk Score** | **16 — Critical** |
| **NIST CSF 2.0** | PR.AA (Protect — Identity Management, Authentication, and Access Control) |
| **CIS Control v8** | 5.4 — Restrict administrator privileges to dedicated administrator accounts; 6.5 — Require MFA for administrative access |
| **Recommended Action** | Create separate admin accounts for IT functions. Remove Global Admin from Medical Director and Operations Manager. Implement emergency access (break-glass) accounts. |

---

### RISK-008: No Security Awareness Training Programme

| Field | Detail |
|-------|--------|
| **Description** | No staff member has received formal cybersecurity training. Staff are unable to identify phishing emails, understand password hygiene, or follow secure data handling practices. |
| **Threat Source** | Internal — human error |
| **Vulnerability** | No training programme exists; no security communication from management; no testing of staff awareness |
| **Likelihood** | 5 — Almost Certain. Without training, human error-based incidents are inevitable. |
| **Impact** | 3 — Moderate. Increased probability of successful phishing, data leakage, and policy violations. |
| **Risk Score** | **15 — Critical** |
| **NIST CSF 2.0** | PR.AT (Protect — Awareness and Training) |
| **CIS Control v8** | 14.1 — Establish and maintain a security awareness program; 14.2 — Train workforce members to recognize social engineering attacks |
| **Recommended Action** | Implement at minimum quarterly security awareness sessions. Include phishing recognition, password hygiene, and data handling. Track completion. |

---

### RISK-009: Non-Compliant Cross-Border Data Transfers

| Field | Detail |
|-------|--------|
| **Description** | Patient data is stored in US-based cloud services (EHR vendor, M365, QuickBooks) without verified comparable safeguards in the receiving jurisdiction, as required by the Data Protection Act. |
| **Threat Source** | Regulatory — non-compliance |
| **Vulnerability** | No data processing agreements reviewed; no cross-border transfer assessment performed; no legal review of vendor terms |
| **Likelihood** | 5 — Almost Certain. This is the current state — data is already being transferred without compliance verification. |
| **Impact** | 3 — Moderate. Regulatory investigation; fines up to TTD 50,000 per offence; reputational damage. |
| **Risk Score** | **15 — Critical** |
| **NIST CSF 2.0** | GV.OC (Govern — Organizational Context); GV.SC (Govern — Supply Chain Risk Management) |
| **CIS Control v8** | 15.4 — Ensure service provider contracts include security requirements |
| **Recommended Action** | Review vendor data processing agreements. Perform cross-border transfer assessment. Implement DPA-compliant contractual safeguards with each vendor. |

---

### RISK-010: Unpatched and Unmanaged Endpoints

| Field | Detail |
|-------|--------|
| **Description** | Workstations and laptops have no centralized patch management. Windows updates depend on individual users accepting prompts, leading to inconsistent and delayed patching. |
| **Threat Source** | External — exploit of known vulnerability |
| **Vulnerability** | No centralized update management; no visibility into patch status; no vulnerability scanning |
| **Likelihood** | 4 — Likely. Unpatched endpoints are a primary initial access vector for attackers. |
| **Impact** | 3 — Moderate. Compromise of individual workstation; potential lateral movement; data access. |
| **Risk Score** | **12 — High** |
| **NIST CSF 2.0** | PR.PS (Protect — Platform Security) |
| **CIS Control v8** | 7.1 — Establish and maintain a vulnerability management process; 7.3 — Perform automated operating system patch management |
| **Recommended Action** | Enable Windows Update for Business via Intune (available with M365 Business Premium). Configure automatic update deployment. Monitor compliance. |

---

### RISK-011: No Formal Incident Response Plan

| Field | Detail |
|-------|--------|
| **Description** | MedCaribe has no documented process for responding to a security incident. No defined roles, escalation paths, or communication procedures exist. |
| **Threat Source** | Operational — lack of preparation |
| **Vulnerability** | No IR plan; no defined incident coordinator; no communication templates; no external IR support relationship |
| **Likelihood** | 3 — Possible. An incident requiring coordinated response is likely within 12-24 months. |
| **Impact** | 4 — Major. Uncoordinated response extends downtime, increases data loss, worsens regulatory exposure. |
| **Risk Score** | **12 — High** |
| **NIST CSF 2.0** | RS.MA (Respond — Incident Management); RS.RP (Respond — Response Planning) |
| **CIS Control v8** | 17.1 — Designate personnel to manage incident handling; 17.4 — Establish and maintain an incident response process |
| **Recommended Action** | Develop and document incident response plan. Assign roles and conduct a tabletop exercise. |

---

### RISK-012: Unsecured Network Infrastructure

| Field | Detail |
|-------|--------|
| **Description** | Consumer-grade routers at three locations, no VLAN segmentation, single Wi-Fi SSID for staff and guests, and unmanaged switches create a flat network where a compromise on any device can reach all others. |
| **Threat Source** | External or internal — network-based attack |
| **Vulnerability** | No network segmentation; consumer-grade equipment; shared Wi-Fi; no network monitoring |
| **Likelihood** | 3 — Possible. Lateral movement is a common post-compromise technique. |
| **Impact** | 4 — Major. Attacker moves freely across all devices at that location. |
| **Risk Score** | **12 — High** |
| **NIST CSF 2.0** | PR.IR (Protect — Technology Infrastructure Resilience) |
| **CIS Control v8** | 12.1 — Ensure network infrastructure is up to date; 12.6 — Use DNS filtering services |
| **Recommended Action** | Separate staff and guest Wi-Fi. Implement VLAN segmentation. Replace consumer-grade routers at primary locations. |

---

### RISK-013: Unencrypted Data on Local Workstations and USB Drives

| Field | Detail |
|-------|--------|
| **Description** | Financial spreadsheets, scanned patient documents, and copied records exist on local drives and unencrypted USB drives. A stolen laptop or lost USB drive exposes this data. |
| **Threat Source** | External — theft; Internal — device loss |
| **Vulnerability** | No disk encryption; no USB policy; no device control; local copies of sensitive data |
| **Likelihood** | 3 — Possible. Device theft and loss are common, especially for mobile staff. |
| **Impact** | 4 — Major. Patient data breach; financial data exposure; DPA violation. |
| **Risk Score** | **12 — High** |
| **NIST CSF 2.0** | PR.DS (Protect — Data Security) |
| **CIS Control v8** | 3.6 — Encrypt data on end-user devices; 3.9 — Encrypt data on removable media |
| **Recommended Action** | Enable BitLocker on all Windows devices. Implement policy prohibiting unencrypted USB drives for sensitive data. |

---

### RISK-014: No Data Classification or Handling Standards

| Field | Detail |
|-------|--------|
| **Description** | No data classification scheme exists. All data is treated identically regardless of sensitivity. |
| **Threat Source** | Operational — governance gap |
| **Vulnerability** | No classification policy; no labelling; staff unaware of sensitivity requirements |
| **Likelihood** | 5 — Almost Certain. This is the current state. |
| **Impact** | 2 — Minor. Increases mishandling probability but is not a direct breach event alone. |
| **Risk Score** | **10 — High** |
| **NIST CSF 2.0** | GV.PO (Govern — Policy); ID.AM (Identify — Asset Management) |
| **CIS Control v8** | 3.1 — Establish and maintain a data management process; 3.7 — Establish and maintain a data classification scheme |
| **Recommended Action** | Implement data classification policy with four tiers: Public, Internal, Confidential, Restricted. |

---

### RISK-015: Insurance Portal Shared Credentials

| Field | Detail |
|-------|--------|
| **Description** | Billing staff share login credentials for insurance portals. Credentials are written on sticky notes visible at workstations. |
| **Threat Source** | Internal — unauthorized access; External — credential theft via physical access |
| **Vulnerability** | Shared credentials; credentials physically visible; no individual accountability |
| **Likelihood** | 4 — Likely. Physical access to sticky notes is trivial. |
| **Impact** | 3 — Moderate. Unauthorized claim submissions; patient data access; potential fraud implication. |
| **Risk Score** | **12 — High** |
| **NIST CSF 2.0** | PR.AA (Protect — Identity Management, Authentication, and Access Control) |
| **CIS Control v8** | 5.2 — Use unique passwords; 6.1 — Establish an access granting process |
| **Recommended Action** | Request individual accounts from insurers. Use a password manager. Remove all posted credentials. |

---

### RISK-016: Personal Email Forwarding of Business Data

| Field | Detail |
|-------|--------|
| **Description** | Staff forward work emails to personal Gmail accounts, bypassing M365 security controls and creating unmanaged copies of sensitive data. |
| **Threat Source** | Internal — staff (convenience-driven) |
| **Vulnerability** | No mail flow rules preventing forwarding; no acceptable use policy; no DLP |
| **Likelihood** | 4 — Likely. Confirmed practice among multiple staff. |
| **Impact** | 3 — Moderate. Sensitive data in unmanaged email; breach risk if personal account compromised. |
| **Risk Score** | **12 — High** |
| **NIST CSF 2.0** | PR.DS (Protect — Data Security); GV.PO (Govern — Policy) |
| **CIS Control v8** | 3.1 — Establish and maintain a data management process; 9.5 — Implement DMARC |
| **Recommended Action** | Block auto-forwarding to external domains in Exchange Online. Implement acceptable use policy. Provide M365 mobile app as secure alternative. |

---

### RISK-017: Multifunction Printers with Default Credentials

| Field | Detail |
|-------|--------|
| **Description** | Network printers at all locations likely retain factory-default passwords, providing a potential pivot point for network attackers. |
| **Threat Source** | External — network attacker |
| **Vulnerability** | Default credentials; network-connected; no segmentation |
| **Likelihood** | 3 — Possible. Printers are commonly exploited as pivot points. |
| **Impact** | 2 — Minor. Primarily a stepping stone; limited direct data on device. |
| **Risk Score** | **6 — Medium** |
| **NIST CSF 2.0** | PR.PS (Protect — Platform Security) |
| **CIS Control v8** | 4.1 — Establish and maintain a secure configuration process; 4.7 — Manage default accounts |
| **Recommended Action** | Change default credentials. Disable unnecessary services. Place on separate segment where possible. |

---

### RISK-018: Lack of Logging and Monitoring

| Field | Detail |
|-------|--------|
| **Description** | No centralized logging, no SIEM, and no routine review of M365 audit logs. Security events could go undetected for extended periods. |
| **Threat Source** | Operational — detection gap |
| **Vulnerability** | No log review; no monitoring tools; audit logs available but never reviewed; no alerting |
| **Likelihood** | 5 — Almost Certain. Without monitoring, events are going undetected now. |
| **Impact** | 2 — Minor. Does not directly cause harm but dramatically increases dwell time of any incident. |
| **Risk Score** | **10 — High** |
| **NIST CSF 2.0** | DE.CM (Detect — Continuous Monitoring); DE.AE (Detect — Adverse Event Analysis) |
| **CIS Control v8** | 8.2 — Collect audit logs; 8.5 — Collect detailed audit logs |
| **Recommended Action** | Configure M365 unified audit logging. Set up basic sign-in and mailbox rule change alerts. Establish weekly log review. |

---

### RISK-019: No Vendor Risk Assessment Process

| Field | Detail |
|-------|--------|
| **Description** | Third-party vendors including EHR provider, cloud services, and external labs have not undergone any security assessment. |
| **Threat Source** | Vendor — supply chain risk |
| **Vulnerability** | No vendor questionnaire; no contractual security requirements; no periodic review |
| **Likelihood** | 3 — Possible. Third-party breaches are increasing significantly. |
| **Impact** | 3 — Moderate. Vendor breach exposes patient data; MedCaribe liable under DPA regardless. |
| **Risk Score** | **9 — High** |
| **NIST CSF 2.0** | GV.SC (Govern — Supply Chain Risk Management); ID.RA (Identify — Risk Assessment) |
| **CIS Control v8** | 15.1 — Establish inventory of service providers; 15.4 — Ensure contracts include security requirements |
| **Recommended Action** | Develop vendor risk questionnaire. Prioritize EHR vendor assessment. Include security clauses in contracts. |

---

### RISK-020: Physical Access to Network Equipment

| Field | Detail |
|-------|--------|
| **Description** | Network equipment at three locations is physically accessible to staff and visitors. |
| **Threat Source** | Internal or external — physical access |
| **Vulnerability** | Unlocked areas; no physical access controls; equipment visible and accessible |
| **Likelihood** | 2 — Unlikely. Requires physical presence and intent. |
| **Impact** | 3 — Moderate. Enables traffic interception, device compromise, or service disruption. |
| **Risk Score** | **6 — Medium** |
| **NIST CSF 2.0** | PR.AA (Protect); PR.IR (Protect — Infrastructure Resilience) |
| **CIS Control v8** | 1.1 — Establish and maintain detailed enterprise asset inventory |
| **Recommended Action** | Secure equipment in locked enclosures. Limit key access to IT admin and location managers. |

---

## 4. Risk Summary by Score

| Rating | Count | Risk IDs |
|--------|-------|----------|
| **Critical (16-25)** | 8 | RISK-001, RISK-002, RISK-003, RISK-004, RISK-005, RISK-007, RISK-008, RISK-009 |
| **High (9-15)** | 10 | RISK-006, RISK-010, RISK-011, RISK-012, RISK-013, RISK-014, RISK-015, RISK-016, RISK-018, RISK-019 |
| **Medium (5-8)** | 2 | RISK-017, RISK-020 |
| **Low (1-4)** | 0 | None |

---

## 5. Top 5 Priority Risks

1. **RISK-001: Business Email Compromise** (Score: 20) — Immediate MFA enforcement and anti-phishing configuration required.
2. **RISK-002: Ransomware** (Score: 20) — Immutable backup implementation is the critical control.
3. **RISK-003: Unauthorized EHR Access** (Score: 16) — Offboarding process and RBAC implementation needed.
4. **RISK-007: Excessive Admin Privileges** (Score: 16) — Separate admin accounts and reduce privilege scope.
5. **RISK-004: Patient Data via WhatsApp** (Score: 15) — Policy enforcement and secure alternative required.

---

## 6. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | J. Maitland | Initial version — 20 risks identified and scored |

**Next Review:** June 2026 (quarterly) or upon significant change to threat landscape, technology environment, or organizational structure.
