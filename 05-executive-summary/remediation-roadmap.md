# MedCaribe Health Group — Remediation Roadmap

**Document Classification:** Confidential — Executive Leadership and IT  
**Version:** 1.0  
**Date:** March 2026  
**Author:** Jelani D. Maitland  
**Review Cycle:** Quarterly

---

## 1. Purpose

This roadmap provides a phased, prioritized plan to address the gaps and risks identified in the MedCaribe security assessment. Actions are sequenced by impact, cost, and dependency — starting with quick wins that use existing licensing and progressing to investments that require budget approval.

---

## 2. Guiding Principles

Actions are prioritized based on: risk reduction impact (addresses Critical or High risks first), cost efficiency (free or low-cost actions before major investments), dependency (foundational actions that enable later improvements are done first), and operational disruption (changes are staged to minimize impact on clinical operations).

---

## 3. Phase 1 — Quick Wins (Weeks 1-4)

*Cost: TTD 0. These actions use existing M365 licensing and require only configuration changes.*

### Week 1-2

| Action | Risk(s) Addressed | Owner | Status |
|--------|--------------------|-------|--------|
| Enforce MFA for all M365 accounts using Microsoft Authenticator | RISK-001, RISK-005, RISK-007 | IT Admin | Pending |
| Create separate admin accounts (admin.doyle@, admin.rampersad@) and remove Global Admin from daily accounts | RISK-007 | IT Admin | Pending |
| Create and secure break-glass emergency admin account | RISK-007 | IT Admin + Ops Manager | Pending |
| Configure Exchange Online to block auto-forwarding to external domains | RISK-016 | IT Admin | Pending |
| Review and remove any existing unauthorized mailbox forwarding rules | RISK-001, RISK-016 | IT Admin | Pending |

### Week 3-4

| Action | Risk(s) Addressed | Owner | Status |
|--------|--------------------|-------|--------|
| Enable M365 Unified Audit Logging and verify it is recording | RISK-018 | IT Admin | Pending |
| Configure basic M365 alerts: impossible travel, sign-in from unfamiliar locations, new inbox forwarding rules, mailbox permission changes | RISK-018, RISK-001 | IT Admin | Pending |
| Enable Microsoft Defender anti-phishing and Safe Links policies | RISK-005 | IT Admin | Pending |
| Enable BitLocker disk encryption on all Windows workstations and laptops | RISK-013 | IT Admin | Pending |
| Implement formal offboarding checklist and communicate to HR and all managers | RISK-003 | Ops Manager | Pending |
| Distribute Acceptable Use Policy to all staff with signed acknowledgement | RISK-004, RISK-016 | Ops Manager | Pending |

**Phase 1 Outcome:** The most critical vulnerability (no MFA) is closed. Email compromise risk is significantly reduced. Admin privilege abuse is contained. Data leakage via forwarding is blocked. Endpoint encryption protects against device theft. All at zero additional cost.

---

## 4. Phase 2 — Foundation Building (Months 2-3)

*Cost: TTD 800-1,500/month for backup; TTD 0 for remaining items.*

| Action | Risk(s) Addressed | Owner | Estimated Cost | Status |
|--------|--------------------|-------|----------------|--------|
| Contact CloudMed EHR vendor to obtain documented backup SLA, RPO/RTO, and request a test restore | RISK-006 | Ops Manager + IT Admin | TTD 0 | Pending |
| Implement immutable cloud backup for M365 (email, OneDrive, SharePoint) using a third-party backup solution | RISK-002 | IT Admin | TTD 800-1,500/month | Pending |
| Migrate shared accounts (reception@, lab@) to M365 Shared Mailboxes with individual access | RISK-003, RISK-015 | IT Admin | TTD 0 | Pending |
| Request individual accounts from insurance portals for each billing staff member. Remove posted credentials. | RISK-015 | Ops Manager | TTD 0 | Pending |
| Configure role-based access in CloudMed EHR (clinical vs. admin vs. scheduling vs. lab) | RISK-003 | IT Admin + Ops Manager | TTD 0 | Pending |
| Deploy Windows Update for Business via Intune for centralized patch management | RISK-010 | IT Admin | TTD 0 (M365 BP includes Intune) | Pending |
| Conduct first quarterly access review across M365, EHR, and QuickBooks | RISK-003 | IT Admin | TTD 0 | Pending |
| Distribute Data Classification, Access Control, and Incident Response policies | RISK-014, RISK-003, RISK-011 | Ops Manager | TTD 0 | Pending |

**Phase 2 Outcome:** Recovery capability is established (immutable backup + verified vendor backup). Identity and access management reaches a functional state. Patch management is automated. Core policies are in effect.

---

## 5. Phase 3 — Capability Building (Months 4-6)

*Cost: TTD 3,000-8,000 for training platform; TTD 2,000-5,000 for network improvements.*

| Action | Risk(s) Addressed | Owner | Estimated Cost | Status |
|--------|--------------------|-------|----------------|--------|
| Deploy security awareness training platform and conduct first all-staff training session | RISK-005, RISK-008 | Ops Manager | TTD 3,000-8,000/year | Pending |
| Conduct first phishing simulation to establish baseline awareness | RISK-005, RISK-008 | Ops Manager + IT Admin | Included in training platform | Pending |
| Separate staff and guest Wi-Fi at all locations | RISK-012 | IT Admin | TTD 1,000-2,500 | Pending |
| Change default credentials on all printers and disable unnecessary services | RISK-017 | IT Admin | TTD 0 | Pending |
| Establish weekly M365 audit log review cadence | RISK-018 | IT Admin | TTD 0 | Pending |
| Conduct first tabletop exercise using business email compromise scenario | RISK-011 | Ops Manager | TTD 0 (internal) | Pending |
| Distribute Vendor Risk Policy and begin Tier 1 vendor assessment (CloudMed EHR) | RISK-019, RISK-006 | Ops Manager | TTD 0 | Pending |
| Secure network equipment in locked enclosures at Chaguanas, Couva, and Point Fortin | RISK-020 | IT Admin + Facilities | TTD 1,000-2,500 | Pending |
| Review and sign Data Processing Agreements with M365, CloudMed, QuickBooks | RISK-009 | Ops Manager + Medical Director | TTD 0 (or legal review cost) | Pending |

**Phase 3 Outcome:** Human layer is addressed through training. Network segmentation begins. Detection capability becomes operational through regular log review. Incident response is tested. Vendor oversight begins. Regulatory compliance gaps are addressed.

---

## 6. Phase 4 — Maturity Development (Months 7-12)

*Cost: TTD 5,000-15,000 for firewall upgrades; other items minimal.*

| Action | Risk(s) Addressed | Owner | Estimated Cost | Status |
|--------|--------------------|-------|----------------|--------|
| Replace consumer-grade routers with business-grade firewalls at San Fernando and Chaguanas | RISK-012 | IT Admin | TTD 5,000-15,000 | Pending |
| Implement VLAN segmentation at primary locations (clinical, admin, guest, IoT) | RISK-012 | IT Admin | Included in firewall deployment | Pending |
| Conduct second tabletop exercise using ransomware scenario | RISK-011 | Ops Manager | TTD 0 | Pending |
| Complete Tier 2 vendor assessments (QuickBooks, insurance portals, labs) | RISK-019 | Ops Manager | TTD 0 | Pending |
| Conduct full annual review of risk register and update scores | All | Ops Manager + IT Admin | TTD 0 | Pending |
| Conduct annual policy review cycle | All | Ops Manager | TTD 0 | Pending |
| Perform second maturity assessment to measure improvement | All | Ops Manager | TTD 0 | Pending |
| Develop USB and removable media policy with approved encrypted devices | RISK-013 | IT Admin + Ops Manager | TTD 500-1,500 for encrypted drives | Pending |
| Evaluate DNS filtering service deployment | RISK-012 | IT Admin | TTD 0-500/month | Pending |
| Establish relationship with external IR support provider | RISK-011 | Ops Manager + Medical Director | Retainer TBD | Pending |

**Phase 4 Outcome:** Network infrastructure hardened. Continuous improvement cycle established. Vendor risk management operational. Second maturity assessment expected to show improvement from 1.2 to 2.5+.

---

## 7. Budget Summary

| Phase | Timeline | Estimated Cost (TTD) | Key Deliverables |
|-------|----------|---------------------|------------------|
| Phase 1 — Quick Wins | Weeks 1-4 | 0 | MFA, admin separation, encryption, forwarding block |
| Phase 2 — Foundation | Months 2-3 | 800-1,500/month (backup) | Immutable backup, vendor SLA, RBAC, patching |
| Phase 3 — Capability | Months 4-6 | 4,000-10,500 one-time | Training, Wi-Fi separation, tabletop, vendor assessment |
| Phase 4 — Maturity | Months 7-12 | 5,500-17,000 | Firewalls, VLANs, annual review, IR support |
| **Year 1 Total** | **12 months** | **TTD 15,100-37,500** | **Maturity from 1.2 to 2.5+** |

---

## 8. Success Metrics

| Metric | Baseline (March 2026) | Target (March 2027) |
|--------|-----------------------|---------------------|
| Overall maturity score | 1.2 / 5 | 2.5+ / 5 |
| MFA adoption rate | ~30% (management only) | 100% |
| Critical risks | 8 | 3 or fewer |
| Policies in place | 0 | 5 (all reviewed and acknowledged) |
| Staff trained on security awareness | 0 | 100% |
| Backup tested | Never | Quarterly |
| Incidents with no response plan | All | None (plan in place and exercised) |
| Vendor assessments completed | 0 | 100% Tier 1, 50% Tier 2 |

---

## 9. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | J. Maitland | Initial version |

**Next Review:** June 2026 (quarterly) to track progress and adjust priorities.
