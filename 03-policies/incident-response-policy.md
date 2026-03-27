# MedCaribe Health Group - Incident Response Policy

**Document Classification:** Internal - All Staff  
**Policy ID:** POL-003  
**Version:** 1.0  
**Effective Date:** March 2026  
**Approved By:** Dr. A. Dorian, Medical Director  
**Review Cycle:** Annual  
**Owner:** Operations Manager

---

## 1. Purpose

This policy establishes the requirements for identifying, reporting, managing, and learning from cybersecurity incidents at MedCaribe Health Group. It ensures that security events are handled consistently, that patient data is protected, and that MedCaribe meets its obligations under the Trinidad and Tobago Data Protection Act (2011).

This policy defines the rules. The Incident Response Plan (a separate document) provides the detailed procedures, roles, escalation paths, and communication templates.

---

## 2. Scope

This policy applies to all cybersecurity incidents affecting MedCaribe systems, data, networks, or personnel - regardless of whether the incident originates internally or externally, and regardless of the system or location affected.

All employees, contractors, and third parties with access to MedCaribe resources are required to comply with this policy.

---

## 3. Definitions

**Security Event:** Any observable occurrence in a system or network that may indicate a potential security issue. Examples include a failed login attempt, a phishing email received, or an antivirus alert.

**Security Incident:** A security event that has been confirmed or is reasonably suspected to have compromised the confidentiality, integrity, or availability of MedCaribe data, systems, or operations. Examples include a confirmed compromised email account, ransomware infection, unauthorized access to patient records, or data exfiltration.

**Data Breach:** A security incident that results in unauthorized access to, disclosure of, or loss of personal data as defined by the Data Protection Act. All data breaches are security incidents, but not all security incidents are data breaches.

---

## 4. Incident Classification

All confirmed or suspected incidents must be classified by severity to determine the appropriate response level:

| Severity | Definition | Examples | Response Requirement |
|----------|------------|----------|---------------------|
| Critical | Immediate threat to patient safety, widespread data breach, or total operational shutdown | Ransomware across multiple systems; confirmed mass patient data exfiltration; EHR unavailable | Immediate response; all hands; Medical Director notified within 1 hour |
| High | Confirmed compromise of system or data with significant impact potential | Single account compromise with patient data access; malware on multiple workstations; backup failure during incident | Response within 2 hours; Operations Manager leads |
| Medium | Confirmed security event with limited immediate impact but requiring investigation | Single workstation malware detection (contained); suspicious sign-in activity; policy violation with data exposure | Response within 24 hours; IT Administrator investigates |
| Low | Security event requiring awareness or minor action | Phishing email reported (not clicked); single failed MFA attempt; minor policy violation | Response within 72 hours; documented for trend analysis |

---

## 5. Reporting Requirements

### 5.1 Internal Reporting

All staff are required to report suspected security events immediately. Reports can be made verbally to the Operations Manager or IT Administrator, by email to security@medcaribe.tt, or by phone to the IT Administrator's direct line.

Staff must not attempt to investigate or resolve suspected incidents on their own. Do not delete suspicious emails, power off potentially compromised systems (unless instructed), or attempt to "fix" the issue before reporting.

There is no penalty for reporting something that turns out not to be an incident. There will be consequences for failing to report a legitimate incident.

### 5.2 External Reporting

The following external notifications may be required depending on the incident:

**Office of the Information Commissioner:** Required under the Data Protection Act if personal data is compromised. The Medical Director, in consultation with legal counsel, will make the determination and authorize notification.

**Insurance Companies:** Required if patient insurance data is compromised, per contractual obligations.

**Corporate Clients:** Required if occupational health data from corporate contracts is affected.

**Law Enforcement (Trinidad and Tobago Police Service - Cyber Crime Unit):** May be engaged for incidents involving criminal activity such as fraud, extortion, or deliberate data theft. The Medical Director authorizes law enforcement engagement.

All external communications regarding incidents must be approved by the Medical Director. No staff member may communicate with media, regulators, or external parties about a security incident without explicit authorization.

---

## 6. Incident Response Phases

MedCaribe follows the NIST SP 800-61 incident response lifecycle:

**Phase 1 - Preparation:** Maintain the incident response plan, train staff on reporting procedures, ensure tools and contacts are available, and conduct periodic exercises.

**Phase 2 - Detection and Analysis:** Identify and validate security events, classify severity, determine scope and impact, and begin documentation.

**Phase 3 - Containment, Eradication, and Recovery:** Contain the incident to prevent further damage, remove the threat, restore affected systems, and verify restoration.

**Phase 4 - Post-Incident Activity:** Conduct a post-incident review, document lessons learned, update the risk register, and improve procedures based on findings.

Detailed procedures for each phase are documented in the Incident Response Plan.

---

## 7. Authority and Decision-Making

### 7.1 Pre-Authorized Containment Actions

The IT Administrator and Operations Manager are pre-authorized to take the following containment actions without waiting for additional approval:

- Disable or suspend a compromised user account
- Disconnect a compromised device from the network
- Block a malicious email sender or domain
- Reset passwords for affected accounts
- Isolate a workstation suspected of malware infection

### 7.2 Actions Requiring Medical Director Approval

The following actions require Medical Director authorization:

- External notifications to regulators, insurers, or patients
- Engagement of external incident response support
- Engagement of law enforcement
- Any communication to media
- Decisions to pay or not pay ransom demands (MedCaribe's default position is not to pay)
- Significant operational decisions (such as shutting down a clinic location)

---

## 8. Evidence Preservation

All incident-related evidence must be preserved to support investigation and potential legal proceedings. Staff must not delete emails, logs, files, or other data that may be relevant to an incident under investigation. The IT Administrator will coordinate evidence preservation, including screenshots, log exports, and email headers.

Chain of custody documentation must be maintained for any evidence collected.

---

## 9. Post-Incident Review

A post-incident review must be conducted within 14 days of incident closure for all High and Critical severity incidents. The review must document what happened (timeline and root cause), what worked well in the response, what did not work or was missing, specific improvements to be made to policies, procedures, or controls, and updates to the risk register.

Post-incident review findings will be reported to the Medical Director and used to update the incident response plan.

---

## 10. Training and Exercises

All staff must receive annual training on incident identification and reporting procedures. The incident response team (Operations Manager, IT Administrator, and designated alternates) must participate in at least one tabletop exercise per year.

---

## 11. Enforcement

Failure to report a suspected security incident may result in disciplinary action. Deliberately concealing a security incident or interfering with an incident investigation is grounds for immediate termination and may be referred for legal action.

---

## 12. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | J. Maitland | Initial version |

**Next Review:** March 2027, after each Critical/High incident, or upon significant organizational change.
