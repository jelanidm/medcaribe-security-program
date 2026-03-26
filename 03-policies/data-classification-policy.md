# MedCaribe Health Group — Data Classification Policy

**Document Classification:** Internal — All Staff  
**Policy ID:** POL-004  
**Version:** 1.0  
**Effective Date:** March 2026  
**Approved By:** Dr. A. Dorian, Medical Director  
**Review Cycle:** Annual  
**Owner:** Operations Manager

---

## 1. Purpose

This policy establishes a data classification scheme for MedCaribe Health Group to ensure that information is identified, labelled, handled, stored, and disposed of according to its sensitivity level. Proper data classification is the foundation of all data protection controls and is required to meet obligations under the Trinidad and Tobago Data Protection Act (2011).

---

## 2. Scope

This policy covers all data created, collected, processed, stored, transmitted, or disposed of by MedCaribe — in any format (digital or physical) and on any system or medium (cloud platforms, workstations, mobile devices, paper, removable media).

All employees, contractors, and third parties handling MedCaribe data must comply with this policy.

---

## 3. Classification Levels

### Level 1: PUBLIC

**Definition:** Information that is intended for public distribution or that would cause no harm if disclosed.

**Examples:** Clinic addresses and phone numbers, general service descriptions, public health awareness materials, job postings.

**Handling Requirements:** No special handling required. May be shared freely. No encryption or access restriction necessary.

### Level 2: INTERNAL

**Definition:** Information intended for internal use within MedCaribe that is not sensitive but should not be publicly distributed.

**Examples:** Internal meeting notes, staff schedules, operational procedures, vendor contact lists, non-sensitive correspondence.

**Handling Requirements:** Store in approved systems (M365, OneDrive, SharePoint). Do not share externally without management approval. No encryption required at rest but must use encrypted transmission (HTTPS, TLS email) when sent externally.

### Level 3: CONFIDENTIAL

**Definition:** Sensitive information whose unauthorized disclosure could cause harm to individuals or to MedCaribe. This is the default classification for any data that has not been explicitly classified.

**Examples:** Employee HR records, salary information, internal financial reports, vendor contracts, insurance claim data, business strategy documents, security assessment findings.

**Handling Requirements:** Store only in approved systems with access limited to authorized personnel. Encrypt at rest on endpoints (BitLocker). Encrypt in transit. Do not store on personal devices or personal cloud accounts. Do not print unless necessary; collect printed copies promptly. Shred physical documents when no longer needed.

### Level 4: RESTRICTED

**Definition:** Highly sensitive information whose unauthorized disclosure could cause serious harm to individuals, result in regulatory penalties, or significantly damage MedCaribe's operations or reputation. This classification includes all personal data defined as sensitive under the Data Protection Act.

**Examples:** Patient medical records, diagnoses, prescriptions, lab results, patient insurance information, patient contact details and demographics, employee medical information, system administrator credentials, security incident details, passwords and access keys.

**Handling Requirements:** Store only in approved, access-controlled systems (CloudMed EHR for clinical data, M365 with restricted access for other data). Access restricted to staff with a documented need based on role (see Access Control Policy). Encrypt at rest and in transit — no exceptions. Never store on personal devices, personal email, personal cloud, USB drives, or paper left unattended. Never transmit via WhatsApp, personal email, or any unapproved channel. Physical documents containing RESTRICTED data must be stored in locked cabinets and shredded when no longer required. Access must be logged where technically possible.

---

## 4. Classification Rules

4.1 **Default Classification:** Any data that has not been explicitly classified must be treated as CONFIDENTIAL until reviewed and classified appropriately.

4.2 **Data Owner Responsibility:** The manager of the department that creates or is primarily responsible for the data is the Data Owner and is responsible for ensuring correct classification.

4.3 **Mixed Data:** When a document or dataset contains data at multiple classification levels, the entire document must be handled at the highest classification level present. For example, a report containing both clinic operational data (INTERNAL) and patient names (RESTRICTED) is classified as RESTRICTED.

4.4 **Reclassification:** Data may be reclassified when circumstances change (for example, when a public announcement makes previously CONFIDENTIAL information PUBLIC). Reclassification must be approved by the Data Owner and documented.

4.5 **Third-Party Data:** Data received from insurance companies, corporate clients, labs, or other third parties must be classified based on its content using MedCaribe's classification levels, regardless of how the third party classifies it.

---

## 5. Data Handling Summary

| Requirement | Public | Internal | Confidential | Restricted |
|-------------|--------|----------|--------------|------------|
| Access restriction | None | MedCaribe staff | Authorized staff only | Role-based, documented need |
| Encryption at rest | Not required | Not required | Required on endpoints | Required everywhere |
| Encryption in transit | Not required | Required for external | Required | Required — no exceptions |
| Personal device storage | Permitted | Not recommended | Prohibited | Prohibited |
| Personal email/WhatsApp | Permitted | Prohibited | Prohibited | Prohibited |
| USB drive transfer | Permitted | Approved encrypted only | Prohibited unless approved | Prohibited |
| Printing | Permitted | Permitted | Minimize; collect promptly | Minimize; locked storage; shred |
| Disposal (digital) | Standard delete | Standard delete | Secure delete | Secure delete; verify |
| Disposal (physical) | Recycling | Shredding | Shredding | Cross-cut shredding |

---

## 6. Data Retention and Disposal

6.1 Data must not be retained longer than necessary for its business or legal purpose. Specific retention periods are defined by record type:

- **Patient medical records:** Minimum 7 years after last visit (or as required by the Medical Board of Trinidad and Tobago)
- **Insurance claims:** Minimum 7 years
- **Financial records:** Minimum 7 years (per tax and corporate law requirements)
- **Employee HR records:** Duration of employment plus 7 years
- **General business correspondence:** 3 years unless specific retention applies
- **Security logs and audit records:** Minimum 1 year

6.2 When data reaches the end of its retention period, it must be disposed of using the method specified in Section 5 for its classification level.

6.3 No patient data may be disposed of without approval from the Medical Director or Operations Manager.

---

## 7. Labelling

7.1 Where technically feasible, documents should include a classification label. For digital documents, include the classification level in the document header or footer (as demonstrated in this security program's documents). For email, include the classification level in the subject line prefix for CONFIDENTIAL and RESTRICTED content. For physical documents, stamp or mark the classification level on the first page.

7.2 Labelling is encouraged but not a substitute for proper handling. Even unlabelled data must be handled according to its actual sensitivity.

---

## 8. Enforcement

Violations of this policy, particularly mishandling of RESTRICTED data, may result in disciplinary action, and in cases involving patient data, may trigger reporting obligations under the Data Protection Act. Repeated or deliberate violations are grounds for termination.

---

## 9. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | J. Maitland | Initial version |

**Next Review:** March 2027 or upon changes to regulatory requirements or data handling practices.
