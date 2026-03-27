# MedCaribe Health Group - Vendor and Third-Party Risk Management Policy

**Document Classification:** Internal - Management and IT  
**Policy ID:** POL-005  
**Version:** 1.0  
**Effective Date:** March 2026  
**Approved By:** Dr. A. Dorian, Medical Director  
**Review Cycle:** Annual  
**Owner:** Operations Manager

---

## 1. Purpose

This policy establishes requirements for assessing, managing, and monitoring cybersecurity risks introduced by third-party vendors and service providers. MedCaribe Health Group relies on external vendors for critical services including electronic health records, cloud infrastructure, accounting, insurance processing, and laboratory services. A security failure at any of these vendors directly impacts MedCaribe's data and operations.

Under the Trinidad and Tobago Data Protection Act (2011), MedCaribe remains responsible for the protection of personal data regardless of whether that data is processed by a third party.

---

## 2. Scope

This policy applies to all third-party relationships where the vendor has access to MedCaribe data (including patient data, employee data, or financial data), provides technology services or infrastructure to MedCaribe, processes or stores data on behalf of MedCaribe, or has network connectivity or physical access to MedCaribe systems.

This includes but is not limited to: CloudMed EHR provider, Microsoft (M365), Intuit (QuickBooks), insurance companies receiving claims data, external reference laboratories, IT support contractors, and any future vendors meeting the criteria above.

---

## 3. Vendor Risk Tiering

All vendors must be classified into a risk tier based on their level of access to MedCaribe data and the criticality of their service.

### Tier 1 - Critical (High Risk)

**Criteria:** Vendor stores or processes RESTRICTED data (patient records, credentials) OR provides a service whose failure would halt MedCaribe operations.

**Examples:** CloudMed EHR provider, Microsoft (M365)

**Assessment Requirements:** Full vendor security questionnaire before onboarding. Annual reassessment. Review of SOC 2 or equivalent audit report. Data processing agreement required. Backup and recovery SLA documented and verified. Cross-border data transfer assessment required per DPA. Right-to-audit clause in contract.

### Tier 2 - Important (Medium Risk)

**Criteria:** Vendor accesses CONFIDENTIAL data OR provides a service that supports but does not directly enable core clinical operations.

**Examples:** QuickBooks (Intuit), insurance company portals, external reference laboratories

**Assessment Requirements:** Abbreviated vendor security questionnaire before onboarding. Biennial reassessment. Data processing agreement required where personal data is shared. Cross-border transfer assessment if data leaves Trinidad and Tobago.

### Tier 3 - Standard (Low Risk)

**Criteria:** Vendor has no access to sensitive data and provides non-critical services.

**Examples:** Office supply vendors, cleaning services, general equipment suppliers

**Assessment Requirements:** No formal security assessment required. Standard contract terms sufficient. Reassess tier if relationship scope changes.

---

## 4. Vendor Assessment Process

### 4.1 New Vendors

Before engaging any new Tier 1 or Tier 2 vendor, the Operations Manager must ensure the following steps are completed:

1. **Identify data exposure:** Document what data the vendor will access, process, or store, and its classification level.
2. **Determine risk tier:** Classify the vendor using Section 3 criteria.
3. **Conduct assessment:** Issue the appropriate vendor security questionnaire and review responses.
4. **Review certifications and audits:** Request and review SOC 2 Type II reports, ISO 27001 certificates, or equivalent evidence of security practices (Tier 1 only).
5. **Cross-border transfer check:** If vendor processes data outside Trinidad and Tobago, assess whether comparable safeguards exist per DPA Section 6(l).
6. **Contract review:** Ensure the contract includes required security clauses (Section 5).
7. **Approval:** Tier 1 vendors require Medical Director approval. Tier 2 vendors require Operations Manager approval.

### 4.2 Existing Vendors

All existing Tier 1 and Tier 2 vendors must be assessed within 6 months of this policy's effective date. Vendors who do not respond to assessment requests or who fail to meet minimum requirements will be escalated to the Medical Director for a risk acceptance or vendor replacement decision.

### 4.3 Vendor Inventory

The Operations Manager must maintain an up-to-date inventory of all Tier 1 and Tier 2 vendors, including vendor name and primary contact, service provided, data accessed or processed and its classification, risk tier, date of last assessment, contract renewal date, and cross-border transfer status.

---

## 5. Contractual Requirements

All contracts with Tier 1 and Tier 2 vendors must include the following security clauses where applicable:

**Data protection:** Vendor must protect MedCaribe data with security controls at least equivalent to those MedCaribe applies to the same data classification.

**Breach notification:** Vendor must notify MedCaribe within 48 hours of discovering any security incident or data breach affecting MedCaribe data.

**Data return and deletion:** Upon contract termination, vendor must return all MedCaribe data and certify destruction of all copies within 30 days.

**Audit rights:** MedCaribe reserves the right to request evidence of the vendor's security practices, either through self-assessment questionnaires, third-party audit reports, or direct inspection (Tier 1 only).

**Subprocessors:** Vendor must notify MedCaribe before engaging any subcontractor who will access MedCaribe data.

**Compliance:** Vendor must comply with applicable Trinidad and Tobago law, including the Data Protection Act, with respect to MedCaribe data.

---

## 6. Ongoing Monitoring

6.1 Tier 1 vendors must be reassessed annually. Tier 2 vendors must be reassessed every two years.

6.2 Vendor assessments must also be triggered by a security incident at the vendor, significant changes to the services provided, contract renewal, or changes to the type or volume of MedCaribe data the vendor accesses.

6.3 The Operations Manager will track vendor assessment due dates and escalate overdue assessments to the Medical Director.

---

## 7. Incident Response

If a vendor experiences a security incident that affects MedCaribe data, the vendor must notify MedCaribe within 48 hours (per contractual requirements). The MedCaribe Incident Response Policy and Plan will be activated. The vendor must cooperate fully with MedCaribe's investigation and provide all relevant information.

MedCaribe will assess the impact on patient data and determine whether notification to the Office of the Information Commissioner or affected individuals is required.

---

## 8. Vendor Termination

Upon termination of a vendor relationship (for any reason), the Operations Manager must ensure all MedCaribe data is returned or securely destroyed, all vendor access to MedCaribe systems is revoked, and written confirmation of data destruction is obtained and filed.

---

## 9. Enforcement

Engaging a Tier 1 or Tier 2 vendor without completing the required assessment process is a policy violation. Violations will be escalated to the Medical Director for review and may result in suspension of the vendor relationship until the assessment is completed.

---

## 10. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | J. Maitland | Initial version |

**Next Review:** March 2027 or upon significant change to vendor relationships or regulatory requirements.
