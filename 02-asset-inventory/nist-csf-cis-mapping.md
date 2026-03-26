# MedCaribe Health Group — NIST CSF 2.0 to CIS Controls v8 IG1 Mapping

**Document Classification:** Internal — Security Program  
**Version:** 1.0  
**Date:** March 2026  
**Author:** Jelani D. Maitland

---

## 1. Purpose

This document maps the NIST Cybersecurity Framework (CSF) 2.0 functions and categories to the corresponding CIS Controls v8 Implementation Group 1 (IG1) safeguards relevant to MedCaribe Health Group's environment.

**How to read this mapping:** NIST CSF tells you *what* security areas to address. CIS Controls tell you *how* to address them technically. Together, they create a complete picture from boardroom to server room.

---

## 2. Mapping by NIST CSF 2.0 Function

### GOVERN (GV)

*Establishes the organization's cybersecurity risk management strategy, expectations, and policy.*

| NIST CSF Category | Description | CIS Control v8 IG1 Safeguard | MedCaribe Status |
|-------------------|-------------|------------------------------|------------------|
| GV.OC — Organizational Context | Understand mission, stakeholder expectations, and regulatory requirements | 15.1 — Establish and maintain inventory of service providers | NOT IMPLEMENTED |
| GV.RM — Risk Management Strategy | Establish and communicate risk management priorities | No direct IG1 mapping (governance-level) | NOT IMPLEMENTED |
| GV.RR — Roles and Responsibilities | Assign cybersecurity roles and responsibilities | 17.1 — Designate personnel to manage incident handling | PARTIAL |
| GV.PO — Policy | Establish, communicate, and enforce cybersecurity policy | 3.1 — Establish and maintain a data management process | NOT IMPLEMENTED |
| GV.SC — Supply Chain Risk Management | Manage supply chain cybersecurity risk | 15.4 — Ensure service provider contracts include security requirements | NOT IMPLEMENTED |

### IDENTIFY (ID)

*Understand the organization's current cybersecurity risk posture.*

| NIST CSF Category | Description | CIS Control v8 IG1 Safeguard | MedCaribe Status |
|-------------------|-------------|------------------------------|------------------|
| ID.AM — Asset Management | Identify and manage assets | 1.1 — Establish enterprise asset inventory; 2.1 — Establish software inventory | PARTIAL |
| ID.RA — Risk Assessment | Understand cybersecurity risks | 3.7 — Establish data classification scheme | NOT IMPLEMENTED |
| ID.IM — Improvement | Identify improvements to posture | No direct IG1 mapping | NOT IMPLEMENTED |

### PROTECT (PR)

*Use safeguards to prevent or reduce cybersecurity risk.*

| NIST CSF Category | Description | CIS Control v8 IG1 Safeguard | MedCaribe Status |
|-------------------|-------------|------------------------------|------------------|
| PR.AA — Identity Management and Access Control | Manage identities, credentials, and access | 5.1 — Account inventory; 5.2 — Unique passwords; 5.3 — Disable dormant accounts; 5.4 — Restrict admin privileges; 6.1 — Access granting; 6.2 — Access revoking; 6.3 — Require MFA externally; 6.5 — Require MFA for admin | POOR |
| PR.AT — Awareness and Training | Provide cybersecurity awareness training | 14.1 — Security awareness program; 14.2 — Social engineering training | NOT IMPLEMENTED |
| PR.DS — Data Security | Manage data consistent with risk strategy | 3.1 — Data management process; 3.4 — Enforce data retention; 3.6 — Encrypt end-user devices; 3.9 — Encrypt removable media; 3.12 — Segment data by sensitivity | POOR |
| PR.PS — Platform Security | Manage security of hardware, software, services | 4.1 — Secure configuration; 4.7 — Manage default accounts; 7.1 — Vulnerability management; 7.3 — Automated OS patching | POOR |
| PR.IR — Infrastructure Resilience | Manage network and infrastructure security | 12.1 — Update network infrastructure; 12.6 — DNS filtering | POOR |

### DETECT (DE)

*Find and analyze possible cybersecurity attacks and compromises.*

| NIST CSF Category | Description | CIS Control v8 IG1 Safeguard | MedCaribe Status |
|-------------------|-------------|------------------------------|------------------|
| DE.CM — Continuous Monitoring | Monitor for anomalies and indicators of compromise | 8.2 — Collect audit logs; 8.5 — Collect detailed audit logs | NOT IMPLEMENTED |
| DE.AE — Adverse Event Analysis | Analyze events to determine if adverse | 8.2 — Collect audit logs | NOT IMPLEMENTED |

### RESPOND (RS)

*Take action regarding a detected cybersecurity incident.*

| NIST CSF Category | Description | CIS Control v8 IG1 Safeguard | MedCaribe Status |
|-------------------|-------------|------------------------------|------------------|
| RS.MA — Incident Management | Manage incidents through resolution | 17.1 — Designate incident handling personnel; 17.4 — Establish IR process | NOT IMPLEMENTED |
| RS.RP — Response Planning | Execute incident response plan | 17.4 — Establish IR process | NOT IMPLEMENTED |
| RS.CO — Incident Communication | Coordinate response with stakeholders | 17.1 — Designate personnel | NOT IMPLEMENTED |
| RS.AN — Incident Analysis | Investigate incidents | 17.4 — Establish IR process | NOT IMPLEMENTED |
| RS.MI — Incident Mitigation | Prevent expansion and mitigate effects | 17.4 — Establish IR process | NOT IMPLEMENTED |

### RECOVER (RC)

*Restore assets and operations affected by a cybersecurity incident.*

| NIST CSF Category | Description | CIS Control v8 IG1 Safeguard | MedCaribe Status |
|-------------------|-------------|------------------------------|------------------|
| RC.RP — Recovery Planning | Execute recovery activities | 11.1 — Data recovery practice; 11.2 — Automated backups; 11.4 — Isolated recovery data | POOR |
| RC.CO — Recovery Communication | Coordinate restoration activities | No direct IG1 mapping | NOT IMPLEMENTED |

---

## 3. Coverage Summary

| NIST CSF Function | Total Categories | Fully Implemented | Partial | Poor | Not Implemented |
|-------------------|-----------------|-------------------|---------|------|-----------------|
| Govern | 5 | 0 | 1 | 0 | 4 |
| Identify | 3 | 0 | 1 | 0 | 2 |
| Protect | 5 | 0 | 0 | 4 | 1 |
| Detect | 2 | 0 | 0 | 0 | 2 |
| Respond | 5 | 0 | 0 | 0 | 5 |
| Recover | 2 | 0 | 0 | 1 | 1 |
| **Total** | **22** | **0** | **2** | **5** | **15** |

**Current posture: 0% fully implemented, 9% partial, 23% poor, 68% not implemented.**

---

## 4. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | J. Maitland | Initial mapping based on current state assessment |
