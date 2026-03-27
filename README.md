# MedCaribe Health Group - Security Program

## A Complete Cybersecurity Governance Program for a Caribbean Healthcare Provider

**Framework:** NIST Cybersecurity Framework (CSF) 2.0 + CIS Controls v8 (Implementation Group 1)  
**Industry:** Private Healthcare - Trinidad and Tobago  
**Author:** Jelani D. Maitland  
**Date:** March 2026

---

## Overview

This repository contains a complete, functional cybersecurity governance program built for **MedCaribe Health Group**, a fictional 55-person private healthcare provider operating in Trinidad and Tobago.

The program was designed from the ground up to demonstrate how a small-to-midsize healthcare organization in the Caribbean can establish a practical, standards-aligned security posture - even without a dedicated security team.

Every document in this repository is written to be **usable**, not theoretical. A real organization of this size and profile could adopt this program with minimal modification.

---

## Why Healthcare? Why Trinidad?

Healthcare is consistently the most targeted industry globally. Patient data commands premium prices on the dark web, ransomware operators exploit the urgency of clinical operations, and most small healthcare providers lack even basic security controls.

In Trinidad and Tobago, the **Data Protection Act (2011)** establishes legal obligations for organizations handling personal information - including healthcare providers - yet most small practices operate without a documented security program. This project addresses that gap directly.

---

## What Makes This Different

- **Dual-framework mapping:** Every risk and control is mapped to both NIST CSF 2.0 functions and CIS Controls v8 IG1 safeguards, showing how governance and technical controls connect.
- **Caribbean regulatory context:** Built around the Trinidad and Tobago Data Protection Act, not just US/EU frameworks.
- **Written for small organizations:** No assumptions about enterprise budgets, dedicated security teams, or advanced tooling. This is designed for environments with one IT person and a Microsoft 365 subscription.
- **Practical over performative:** Policies are concise and actionable. The risk register reflects real-world threats to small healthcare providers, not generic compliance filler.

---

## Repository Structure

```
medcaribe-security-program/
├── README.md
├── 01-company-profile/
│   ├── company-overview.md          # Organization profile and business context
│   └── asset-inventory.md           # Technology environment and data flows
├── 02-risk-assessment/
│   ├── risk-register.md             # Scored risk register with 20 identified risks
│   ├── nist-csf-cis-mapping.md      # Dual-framework control mapping
│   └── gap-analysis.md              # Current state maturity assessment
├── 03-policies/
│   ├── acceptable-use-policy.md     # Technology and data acceptable use
│   ├── access-control-policy.md     # Identity and access management
│   ├── incident-response-policy.md  # Security incident handling
│   ├── data-classification-policy.md # Data handling and classification
│   └── vendor-risk-policy.md        # Third-party risk management
├── 04-incident-response-plan/
│   ├── ir-plan.md                   # Full incident response plan
│   └── escalation-decision-tree.md  # Escalation paths and decision criteria
├── 05-executive-summary/
│   ├── board-risk-briefing.md       # Executive-level risk summary
│   └── remediation-roadmap.md       # Prioritized improvement plan
└── pdf-versions/
    └── (all documents exported as PDF)
```

---

## Frameworks Used

### NIST Cybersecurity Framework (CSF) 2.0
The six core functions - **Govern, Identify, Protect, Detect, Respond, Recover** - provide the strategic structure for the program. Each risk and control maps to specific CSF categories and subcategories.

### CIS Controls v8 - Implementation Group 1
IG1 represents essential cyber hygiene and is designed for organizations with limited resources and expertise. Every technical control recommendation aligns to specific CIS safeguards appropriate for a small healthcare environment.

---

## Regulatory Context

**Trinidad and Tobago Data Protection Act (2011)** - Chapter 22:04

Key obligations relevant to this program:
- Organizations are responsible for personal information under their control
- Purpose for data collection must be identified before or at the time of collection
- Consent is required prior to collection, use, or disclosure
- Personal data must be accurate, secure, relevant, and not excessive
- Cross-border data transfers require comparable safeguards
- Non-compliance penalties include fines up to TTD 50,000 and imprisonment up to 3 years

---

## How to Use This Repository

**If you are a security professional:** Use this as a reference for building governance programs for small organizations. Fork it, adapt it, and make it your own.

**If you are a small business owner:** Read the executive summary and risk briefing first. Then work through the policies with your IT support to understand what applies to your environment.

**If you are studying GRC:** Walk through the risk register and dual-framework mapping to understand how governance frameworks translate into practical controls.

---

## About the Author

Jelani D. Maitland is a cybersecurity professional based in Trinidad and Tobago, holding CySA+, Security+, SC-200, and Fortinet FCA certifications. He specializes in security operations, governance, and risk management for small and midsize organizations in the Caribbean.

- [LinkedIn](https://linkedin.com/in/jelanidm)
- [GitHub](https://github.com/jelanidm)

---

## License

This project is shared under the [MIT License](LICENSE). You are free to use, modify, and distribute these materials with attribution.
