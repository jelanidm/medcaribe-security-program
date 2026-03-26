# MedCaribe Health Group — Security Maturity Gap Analysis

**Document Classification:** Internal — Security Program  
**Version:** 1.0  
**Date:** March 2026  
**Author:** Jelani D. Maitland  
**Review Cycle:** Semi-annual

---

## 1. Purpose

This document assesses MedCaribe Health Group's current cybersecurity maturity against each NIST CSF 2.0 function using a five-level maturity scale. It identifies specific gaps and provides the basis for the remediation roadmap.

---

## 2. Maturity Scale

| Level | Rating | Definition |
|-------|--------|------------|
| 1 | Initial | No formal process; ad hoc and reactive; dependent on individual knowledge |
| 2 | Developing | Some awareness exists; informal processes in place but inconsistent; not documented |
| 3 | Defined | Documented policies and procedures exist; roles assigned; processes followed but not measured |
| 4 | Managed | Processes are measured and monitored; metrics tracked; regular review and improvement |
| 5 | Optimized | Continuous improvement based on data; proactive risk management; integrated into business operations |

---

## 3. Current State Assessment

### 3.1 GOVERN — Maturity Level: 1 (Initial)

| Area | Finding | Gap |
|------|---------|-----|
| Organizational context | No documented understanding of regulatory obligations or threat landscape | Need formal documentation of regulatory requirements (DPA) and business context |
| Risk management strategy | No defined risk appetite or risk management approach | Need board-approved risk management strategy |
| Roles and responsibilities | IT admin handles security reactively; no formal assignment | Need documented security roles and RACI matrix |
| Policy | Zero security policies exist | Need complete policy suite (five core policies being developed in this program) |
| Supply chain risk | No vendor assessments; no contractual security requirements | Need vendor risk management process and contract review |

**Target maturity:** Level 3 (Defined) within 12 months.

---

### 3.2 IDENTIFY — Maturity Level: 1.5 (Between Initial and Developing)

| Area | Finding | Gap |
|------|---------|-----|
| Asset management | IT admin has informal knowledge of devices and software but no documented inventory | Need formalized asset inventory with ownership and update cadence (produced in this program) |
| Risk assessment | No prior risk assessment performed | Need documented risk assessment process with regular review (produced in this program) |
| Improvement tracking | No process to track or measure security improvements | Need improvement register tied to risk register |

**Target maturity:** Level 3 (Defined) within 12 months.

---

### 3.3 PROTECT — Maturity Level: 1.5 (Between Initial and Developing)

| Area | Finding | Gap |
|------|---------|-----|
| Identity and access | MFA only partially deployed; shared accounts; no RBAC; excessive admin rights; no offboarding | Need full MFA enforcement; eliminate shared accounts; implement RBAC; separate admin accounts; document offboarding |
| Awareness and training | Zero security training delivered to any staff member | Need quarterly security awareness program with phishing training |
| Data security | No encryption on endpoints or USB; no classification; data on personal devices; no DLP | Need BitLocker enforcement; data classification policy; acceptable use policy; block external forwarding |
| Platform security | No centralized patching; default printer credentials; no hardening standards | Need Intune-based patch management; printer hardening; secure baseline configurations |
| Infrastructure resilience | Consumer-grade routers; no segmentation; shared Wi-Fi; no DNS filtering | Need business-grade firewalls at primary sites; VLAN segmentation; separate guest Wi-Fi |

**Target maturity:** Level 2.5 (Developing to Defined) within 12 months. Full Level 3 within 18 months.

---

### 3.4 DETECT — Maturity Level: 1 (Initial)

| Area | Finding | Gap |
|------|---------|-----|
| Continuous monitoring | M365 audit logs available but never reviewed; no alerting configured; no SIEM | Need M365 audit log review cadence; basic alert rules for suspicious sign-ins and mailbox changes |
| Adverse event analysis | No capability to analyze security events; no process to triage alerts | Need at minimum a weekly log review process and escalation criteria |

**Target maturity:** Level 2 (Developing) within 12 months. Level 3 requires dedicated monitoring capability.

---

### 3.5 RESPOND — Maturity Level: 1 (Initial)

| Area | Finding | Gap |
|------|---------|-----|
| Incident management | No defined process for managing security incidents | Need incident response plan with roles, escalation paths, and communication templates (produced in this program) |
| Response planning | No IR plan exists | Need documented and tested IR plan |
| Incident communication | No internal or external communication procedures for incidents | Need communication templates and contact lists for incidents |
| Incident analysis | No capability to investigate incidents beyond basic IT troubleshooting | Need relationship with external IR support for complex incidents |
| Incident mitigation | No pre-approved containment actions; no authority to isolate systems | Need pre-authorized containment procedures (account disable, device isolation) |

**Target maturity:** Level 3 (Defined) within 12 months after plan development and tabletop exercise.

---

### 3.6 RECOVER — Maturity Level: 1 (Initial)

| Area | Finding | Gap |
|------|---------|-----|
| Recovery planning | No documented recovery plan; no RTO/RPO defined; vendor backup unverified | Need defined RTO/RPO per system; verified vendor backup; tested restore process |
| Recovery communication | No plan for communicating with patients, insurers, or regulators during recovery | Need recovery communication plan as part of IR plan |

**Target maturity:** Level 2.5 (Developing to Defined) within 12 months.

---

## 4. Maturity Summary

| NIST CSF Function | Current Level | Target Level (12 months) | Gap |
|-------------------|---------------|--------------------------|-----|
| Govern | 1.0 | 3.0 | 2.0 |
| Identify | 1.5 | 3.0 | 1.5 |
| Protect | 1.5 | 2.5 | 1.0 |
| Detect | 1.0 | 2.0 | 1.0 |
| Respond | 1.0 | 3.0 | 2.0 |
| Recover | 1.0 | 2.5 | 1.5 |
| **Overall Average** | **1.2** | **2.7** | **1.5** |

---

## 5. Critical Gap Priorities

Based on the assessment, the following gaps represent the highest combined risk and fastest path to maturity improvement:

1. **MFA enforcement across all accounts** — Closes the most critical vulnerability (BEC, credential theft) with minimal cost using existing M365 licensing.

2. **Incident response plan creation and testing** — Moves Respond function from Level 1 to Level 3 with a single documented deliverable and tabletop exercise.

3. **Security policy suite** — Establishes governance foundation that enables all other improvements.

4. **Backup verification and immutable backup** — Addresses the highest-impact risk (ransomware) by confirming recovery capability.

5. **Security awareness training** — Reduces the most common attack vector (phishing/social engineering) across the entire organization.

---

## 6. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | J. Maitland | Initial gap analysis based on current state assessment |

**Next Review:** September 2026 or upon completion of first remediation phase.
