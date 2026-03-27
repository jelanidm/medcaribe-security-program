# MedCaribe Health Group — Board-Level Risk Briefing

**Document Classification:** Confidential — Executive Leadership  
**Version:** 1.0  
**Date:** March 2026  
**Prepared By:** Jelani D. Maitland  
**Audience:** Medical Director, Operations Manager, Finance Manager

---

## Executive Summary

MedCaribe Health Group currently operates with minimal cybersecurity protections. A comprehensive security assessment has identified 20 risks, 8 of which are rated Critical. The organization's overall security maturity is 1.2 out of 5.

The three findings that require immediate executive attention are:

**1. MedCaribe is highly vulnerable to business email compromise and ransomware.** Multi-factor authentication is not enforced for most staff, and there is no verified backup that would allow recovery from a ransomware attack. A successful attack could shut down all four clinics and result in permanent loss of patient records. The estimated business impact of a week-long ransomware outage, based on industry averages for healthcare providers of this size, is TTD 150,000 to 400,000 in direct costs (lost revenue, recovery, potential regulatory fines) — not including reputational damage.

**2. Patient data is being handled outside of MedCaribe's control.** Staff routinely share patient information via personal WhatsApp and personal email accounts. This is a direct violation of the Data Protection Act and creates liability that MedCaribe cannot contain or remediate after the fact. The Data Protection Act allows fines up to TTD 50,000 per offence and imprisonment up to 3 years.

**3. MedCaribe has no plan for responding to a security incident.** If a breach occurs today, there are no defined roles, no escalation paths, no communication templates, and no pre-agreed authority to take containment actions. The result would be a disorganized response that extends downtime, increases data loss, and worsens regulatory exposure.

---

## Current Risk Profile

| Rating | Number of Risks | Key Themes |
|--------|----------------|------------|
| Critical (16-25) | 8 | Email compromise, ransomware, unauthorized access, data leakage, excessive privileges, no training, regulatory non-compliance |
| High (9-15) | 10 | Unpatched systems, no IR plan, flat network, unencrypted devices, no logging, no vendor oversight |
| Medium (5-8) | 2 | Default printer credentials, physical access to network equipment |

---

## Maturity Assessment

| Security Area | Current Score (1-5) | What This Means |
|---------------|--------------------|--------------------|
| Governance (policies, roles, strategy) | 1.0 | No policies exist. No one is formally responsible for security. |
| Asset and Risk Identification | 1.5 | IT admin knows what exists informally but nothing is documented. |
| Protective Controls | 1.5 | Some controls exist (partial MFA, basic antivirus) but major gaps remain. |
| Detection Capability | 1.0 | Logs are available but no one reviews them. Security events go unnoticed. |
| Incident Response | 1.0 | No plan, no team, no procedures. A major incident would be handled ad hoc. |
| Recovery Capability | 1.0 | No tested backups. Vendor backup is assumed but unverified. |

**Overall: 1.2 out of 5.** This places MedCaribe in the "Initial" maturity category — security is ad hoc, reactive, and dependent on individual knowledge rather than organizational capability.

---

## What This Means for the Business

**Patient trust:** Patients entrust MedCaribe with their most sensitive information. A data breach — especially one caused by easily preventable issues like WhatsApp data sharing — would damage trust that took years to build.

**Regulatory exposure:** MedCaribe is currently non-compliant with multiple provisions of the Data Protection Act, particularly regarding data handling, cross-border transfers, and security safeguards. The regulatory environment in Trinidad is tightening.

**Operational continuity:** A ransomware attack with no tested backup means potential permanent loss of patient records and extended clinic shutdowns. This is not theoretical — healthcare is the most targeted industry globally.

**Contractual risk:** Insurance companies and corporate clients increasingly require evidence of security controls. Inability to demonstrate basic security practices may affect MedCaribe's ability to maintain and win contracts.

---

## Recommended Investment

The good news is that the most impactful improvements are achievable within the organization's current technology licensing and at relatively low cost.

| Priority | Action | Estimated Cost | Estimated Timeline |
|----------|--------|----------------|-------------------|
| 1 | Enforce MFA for all M365 accounts | TTD 0 (included in M365 license) | 1-2 weeks |
| 2 | Configure M365 anti-phishing and auto-forwarding block | TTD 0 (included in M365 license) | 1 week |
| 3 | Verify EHR vendor backup and document recovery SLA | TTD 0 (vendor engagement) | 2-4 weeks |
| 4 | Implement immutable cloud backup for M365 | TTD 800-1,500 per month | 2-3 weeks |
| 5 | Enable BitLocker disk encryption on all devices | TTD 0 (included in Windows 11 Pro) | 1-2 weeks |
| 6 | Eliminate shared accounts and separate admin accounts | TTD 0 (configuration change) | 2 weeks |
| 7 | Deploy security awareness training | TTD 3,000-8,000 per year | 4-6 weeks |
| 8 | Implement formal offboarding checklist | TTD 0 (process change) | 1 week |
| 9 | Configure M365 audit logging and basic alerting | TTD 0 (included in M365 license) | 1-2 weeks |
| 10 | Separate staff and guest Wi-Fi | TTD 2,000-5,000 (equipment) | 4-6 weeks |

**Total estimated first-year investment: TTD 15,000 to 30,000** — significantly less than the potential cost of a single incident.

---

## Decision Requested

The security program requires Medical Director approval and authorization to proceed with the remediation roadmap. Specifically:

1. **Approve** the security policies developed as part of this program for organization-wide implementation.
2. **Authorize** the IT Administrator to enforce MFA and configure M365 security settings within 2 weeks.
3. **Approve** the estimated budget of TTD 15,000-30,000 for first-year security improvements.
4. **Assign** the Operations Manager as the formal security program owner with responsibility for ongoing oversight.
5. **Commit** to conducting the first tabletop exercise within 90 days.

---

## Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | J. Maitland | Initial version |
