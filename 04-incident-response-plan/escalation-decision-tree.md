# MedCaribe Health Group — Escalation Decision Tree

**Document Classification:** Confidential — Incident Response Team  
**Version:** 1.0  
**Date:** March 2026  
**Author:** Jelani D. Maitland

---

## 1. Purpose

This document provides a quick-reference decision tree for classifying and escalating security incidents. It is designed to be printed and posted in the IT area and referenced during active incidents.

---

## 2. Escalation Flow

```
SECURITY EVENT DETECTED
(Staff report, alert, or log review)
│
▼
IS THIS A CONFIRMED OR SUSPECTED SECURITY INCIDENT?
(Unauthorized access, data exposure, malware, system compromise)
│
├── NO ──► Document and close. Monitor for recurrence.
│
▼ YES
│
CLASSIFY SEVERITY
│
├── CRITICAL ─────────────────────────────────────────────────┐
│   (Ransomware, mass data breach, EHR down, multi-system)   │
│                                                              │
│   IMMEDIATE ACTIONS:                                         │
│   1. Contain (disconnect, disable accounts)                  │
│   2. Notify IT Admin — NOW                                   │
│   3. Notify Operations Manager — NOW                         │
│   4. Notify Medical Director — WITHIN 1 HOUR                 │
│   5. Activate Incident Response Plan                         │
│   6. Consider external IR support                            │
│   7. Begin incident log                                      │
│                                                              │
├── HIGH ─────────────────────────────────────────────────────┐│
│   (Single account compromise with data access, malware      ││
│    on multiple workstations, backup failure during event)    ││
│                                                              ││
│   ACTIONS WITHIN 2 HOURS:                                    ││
│   1. Contain (disable account, isolate device)               ││
│   2. Notify IT Admin                                         ││
│   3. Notify Operations Manager                               ││
│   4. Begin investigation and incident log                    ││
│   5. Notify Medical Director if patient data affected        ││
│                                                              ││
├── MEDIUM ───────────────────────────────────────────────────┐││
│   (Single workstation malware contained, suspicious         │││
│    sign-in activity, policy violation with data exposure)   │││
│                                                              │││
│   ACTIONS WITHIN 24 HOURS:                                   │││
│   1. IT Admin investigates                                   │││
│   2. Notify Operations Manager                               │││
│   3. Document findings                                       │││
│   4. Determine if escalation to HIGH is needed               │││
│                                                              │││
└── LOW ──────────────────────────────────────────────────────┘│││
    (Phishing reported not clicked, single failed MFA,         │││
     minor policy violation)                                   │││
                                                               │││
    ACTIONS WITHIN 72 HOURS:                                   │││
    1. IT Admin reviews and documents                          │││
    2. Track for patterns                                      │││
    3. No escalation unless pattern emerges                    │││
```

---

## 3. Patient Data Decision Branch

```
DOES THE INCIDENT INVOLVE PATIENT DATA?
│
├── NO ──► Continue standard response per severity level
│
▼ YES
│
WAS PATIENT DATA ACTUALLY ACCESSED, EXFILTRATED, OR EXPOSED?
│
├── NO (only system compromised, data not reached) ──► Document. Monitor.
│
▼ YES
│
HOW MANY PATIENTS AFFECTED?
│
├── UNKNOWN ──► Treat as potentially large. Escalate to Medical Director.
│
├── 1-10 patients ──► Medical Director reviews. Legal counsel consulted.
│                      Determine if notification to Information Commissioner required.
│
├── 11-100 patients ──► Medical Director notified immediately.
│                        Legal counsel engaged.
│                        Prepare notification to Information Commissioner.
│                        Prepare individual patient notification.
│
└── 100+ patients ──► CRITICAL severity (if not already).
                       Medical Director leads response.
                       Legal counsel and external IR support engaged.
                       Information Commissioner notification prepared.
                       Patient notification drafted.
                       Consider public communication.
```

---

## 4. External Notification Decision

```
IS EXTERNAL NOTIFICATION REQUIRED?
│
├── Information Commissioner (Data Protection Act)
│   └── Required when: Confirmed breach of personal data
│       with potential harm to individuals
│       Decision authority: Medical Director
│       Timeline: As soon as practicable after confirmation
│
├── Insurance Companies
│   └── Required when: Patient insurance data is compromised
│       Decision authority: Operations Manager
│       Timeline: Per contractual requirements
│
├── Corporate Clients
│   └── Required when: Occupational health data from
│       corporate contracts is affected
│       Decision authority: Operations Manager
│       Timeline: Per contractual requirements
│
├── Law Enforcement (TTPS Cyber Crime Unit)
│   └── Required when: Criminal activity identified
│       (fraud, extortion, deliberate data theft)
│       Decision authority: Medical Director
│       Timeline: As appropriate per legal counsel advice
│
└── Affected Patients
    └── Required when: Personal data breach with
        potential harm to individuals
        Decision authority: Medical Director
        Timeline: After initial investigation complete
        Method: Written notification (letter or email)
```

---

## 5. Pre-Authorized Actions Quick Reference

The following actions can be taken by the IT Administrator or Operations Manager WITHOUT waiting for Medical Director approval:

| Action | When To Use |
|--------|-------------|
| Disable a user account | Account confirmed or strongly suspected compromised |
| Force sign-out all sessions | Account compromise or suspicious activity |
| Reset user password | Account compromise |
| Disconnect device from network | Malware suspected or confirmed |
| Block email sender/domain | Active phishing campaign |
| Revoke OAuth app consent | Suspicious third-party app access |
| Enable MFA on compromised account | Post-compromise hardening |

---

## 6. Actions Requiring Medical Director Approval

| Action | Reason |
|--------|--------|
| Notify Information Commissioner | Regulatory and legal implications |
| Notify patients of data breach | Reputational and legal implications |
| Engage external IR support | Cost and scope commitment |
| Contact law enforcement | Legal implications |
| Issue public statement | Reputational impact |
| Ransom payment decision | Financial and ethical implications (default: do not pay) |
| Shut down a clinic location | Operational and patient care impact |

---

## 7. Quick Contact Card

*Print this section and post in the IT area at San Fernando office.*

**SECURITY INCIDENT? CALL IN THIS ORDER:**

1. **IT Administrator (M. Doyle):** [phone number]
2. **Operations Manager (K. Rampersad):** [phone number]
3. **Medical Director (Dr. A. Dorian):** [phone number]

**Email:** security@medcaribe.tt

**External IR Support:** [TBD — to be established]

**IF YOU CANNOT REACH ANYONE:** Contain first (disconnect device, do not use the affected system), then keep trying contacts. Document everything you observe.

---

## 8. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | J. Maitland | Initial version |
