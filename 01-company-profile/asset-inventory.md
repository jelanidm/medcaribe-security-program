# MedCaribe Health Group — Technology Asset Inventory and Data Flow

**Document Classification:** Internal — Security Program  
**Version:** 1.0  
**Date:** March 2026  
**Author:** Jelani D. Maitland  
**Review Cycle:** Quarterly or upon significant technology change

---

## 1. Purpose

This document provides a structured inventory of all technology assets, software platforms, and data flows within MedCaribe Health Group. It serves as the foundation for risk assessment, access control decisions, and incident response planning.

Maintaining an accurate asset inventory is a foundational control under both NIST CSF 2.0 (ID.AM — Asset Management) and CIS Controls v8 (Control 1 — Inventory and Control of Enterprise Assets, Control 2 — Inventory and Control of Software Assets).

---

## 2. Hardware Assets

### 2.1 Endpoint Devices

| Asset Type | Quantity | Location(s) | OS | Management Status |
|------------|----------|-------------|-----|-------------------|
| Desktop workstations | 22 | All locations | Windows 11 Pro | Domain-joined via Entra ID; no centralized patch management |
| Laptop computers | 8 | Mobile staff, management | Windows 11 Pro | Entra ID joined; used on and off-site |
| Reception tablets | 4 | Front desks — all locations | Android 13 | Patient check-in kiosks; consumer-grade, no MDM |
| Label/receipt printers | 6 | Admin and lab areas | Embedded firmware | Network-connected; unmanaged |
| Multifunction printers | 4 | One per location | Embedded firmware | Network-connected; default credentials likely unchanged |

### 2.2 Network Infrastructure

| Asset Type | Quantity | Location | Notes |
|------------|----------|----------|-------|
| Internet gateway / router | 4 | One per location | ISP-provided; consumer-grade at 3 locations |
| Wireless access points | 6 | All locations | Mixed vendors; single SSID for staff and guest at most locations |
| Network switch | 4 | Server/comms area per location | Unmanaged switches; no VLAN segmentation |
| NAS device (backup) | 1 | San Fernando main office | Synology NAS; local backup target for admin files |

### 2.3 Server and Infrastructure

| Asset Type | Quantity | Location | Purpose |
|------------|----------|----------|---------|
| On-premise server | 0 | N/A | No on-premise servers — cloud-first approach |
| UPS battery backup | 2 | San Fernando, Chaguanas | Protects network equipment and workstations in main offices |

---

## 3. Software and Cloud Services

### 3.1 Core Business Platforms

| Platform | Type | Hosting | Purpose | Data Stored | Users |
|----------|------|---------|---------|-------------|-------|
| Microsoft 365 Business Premium | SaaS | Microsoft Cloud | Email, calendar, Teams, file storage (OneDrive/SharePoint) | Business communications, documents, internal files | All 55 staff |
| CloudMed EHR (fictional) | SaaS | Vendor-hosted (US-based data centre) | Electronic health records, appointment scheduling, prescriptions | Patient demographics, medical history, diagnoses, treatment records, lab results | 35 clinical and admin staff |
| QuickBooks Online | SaaS | Intuit Cloud | Accounting, invoicing, payroll | Financial records, employee salary data, vendor payments | 4 finance and management staff |
| Sagicor / Guardian Insurance Portals | Web portals | Insurer-hosted | Insurance claim submission and tracking | Patient identity, policy numbers, diagnoses, claim amounts | 6 billing staff |

### 3.2 Supporting Software

| Software | Type | Purpose | Data Sensitivity |
|----------|------|---------|------------------|
| Microsoft Defender (built-in) | Endpoint security | Basic antivirus and threat protection | N/A — security tool |
| WhatsApp (personal devices) | Messaging | Informal staff communication, sometimes patient coordination | High risk — unmanaged, patient data may transit |
| Zoom | SaaS | Telemedicine consultations (ad hoc) | High — clinical discussions, not BAA-covered |
| Google Drive (personal) | SaaS | Ad hoc file sharing by individual staff | High risk — unmanaged, potential data leakage |
| USB drives | Removable media | File transfer between locations | High risk — unencrypted, no policy enforcement |

### 3.3 Software Inventory Summary (CIS Control 2)

| Category | Authorized | Unauthorized / Shadow IT |
|----------|------------|--------------------------|
| Productivity | Microsoft 365 suite | Google Drive (personal accounts) |
| Clinical | CloudMed EHR | None identified |
| Financial | QuickBooks Online | Personal spreadsheets on local drives |
| Communication | Microsoft Teams, Outlook | WhatsApp (personal), Zoom (no enterprise license) |
| Security | Microsoft Defender (basic) | None |
| Backup | OneDrive, Synology NAS | None formalized |

---

## 4. Identity and Access Management

### 4.1 Current State

| Component | Status | Notes |
|-----------|--------|-------|
| Identity provider | Microsoft Entra ID (via M365 Business Premium) | All staff have M365 accounts |
| Multi-factor authentication (MFA) | Partially enabled | MFA enabled for management accounts; not enforced for all users |
| Password policy | Default M365 settings | No custom complexity or expiration policy configured |
| Privileged accounts | 3 global admin accounts | IT admin (1), Medical Director (1), Operations Manager (1) — excessive admin rights |
| Shared accounts | At least 2 known | "reception@medcaribe.tt" and "lab@medcaribe.tt" used by multiple staff |
| Offboarding process | Informal | No documented process; accounts sometimes remain active after departure |
| Role-based access control | Not implemented | Most users have similar access levels regardless of role |

### 4.2 Access by System

| System | Authentication Method | MFA | Access Review Frequency |
|--------|----------------------|-----|------------------------|
| Microsoft 365 | Entra ID (email + password) | Partial | None |
| CloudMed EHR | Username + password (separate credentials) | No | None |
| QuickBooks Online | Email + password | No | None |
| Insurance portals | Username + password (shared per location) | No | None |
| Network (Wi-Fi) | Pre-shared key (same for all staff) | N/A | Never changed |
| Synology NAS | Local admin account | No | None |

---

## 5. Data Flow Mapping

### 5.1 Patient Data Lifecycle

```
Patient Arrival
    │
    ▼
Reception Check-in ──► CloudMed EHR (demographics, insurance info entered)
    │
    ▼
Clinical Consultation ──► CloudMed EHR (diagnosis, notes, prescriptions)
    │
    ▼
Diagnostic Testing ──► CloudMed EHR (lab results, imaging reports)
    │
    ├──► External Reference Lab (sample + requisition via courier + portal)
    │
    ▼
Billing & Insurance ──► QuickBooks (invoice) + Insurer Portal (claim submission)
    │
    ▼
Follow-up / Ongoing Care ──► CloudMed EHR (updated records, appointment scheduling)
```

### 5.2 Data at Rest

| Data Type | Primary Storage | Secondary / Backup | Encryption at Rest |
|-----------|----------------|-------------------|-------------------|
| Patient health records | CloudMed EHR (vendor cloud) | None verified | Vendor-managed (assumed) |
| Business email and files | Microsoft 365 (Exchange Online, OneDrive, SharePoint) | None configured | Microsoft-managed |
| Financial records | QuickBooks Online | Local spreadsheet copies on some workstations | No (local copies unencrypted) |
| Scanned documents | OneDrive / local workstation folders | Synology NAS (inconsistent) | No |
| Insurance claims data | Insurer portals (copies in email) | Email attachments in Outlook | Microsoft-managed (email); not encrypted locally |

### 5.3 Data in Transit

| Data Flow | Source | Destination | Protocol | Encrypted |
|-----------|--------|-------------|----------|-----------|
| Email (external) | M365 Outlook | External recipients | TLS (opportunistic) | Yes (when recipient supports TLS) |
| EHR access | Staff workstations | CloudMed vendor cloud | HTTPS | Yes |
| Insurance claim submission | Billing workstations | Insurer portals | HTTPS | Yes |
| Lab results (reference lab) | External lab portal | Staff email / EHR | HTTPS / Email | Partially — portal is HTTPS; email may not be encrypted |
| Internal file sharing | Staff devices | OneDrive / SharePoint | HTTPS | Yes |
| WhatsApp messages | Personal mobile devices | WhatsApp servers | End-to-end encrypted | Yes, but unmanaged and non-compliant |
| Wi-Fi traffic | All devices | Router / internet | WPA2 (no enterprise auth) | Basic — susceptible to key compromise |

### 5.4 Cross-Border Data Transfers

| Data Type | Destination | Purpose | DPA Compliance Status |
|-----------|-------------|---------|----------------------|
| Patient health records | United States (CloudMed EHR vendor data centre) | Clinical record storage and processing | **Unverified** — no documented assessment of vendor safeguards per DPA Section 6(l) |
| Business email | United States / Ireland (Microsoft data centres) | Email and file storage | **Partially compliant** — Microsoft DPA available but not reviewed or signed |
| Financial data | United States (Intuit / QuickBooks) | Accounting and payroll | **Unverified** — no documented assessment |

---

## 6. Backup and Recovery

### 6.1 Current Backup Status

| System | Backup Method | Frequency | Tested |
|--------|--------------|-----------|--------|
| Microsoft 365 (email, files) | Native M365 retention (not true backup) | Continuous (retention policies) | Never tested |
| CloudMed EHR | Vendor-managed backups (assumed) | Unknown | Never verified with vendor |
| QuickBooks Online | Intuit-managed | Unknown | Never tested |
| Local files (workstations) | Ad hoc copy to Synology NAS | Inconsistent — manual process | Never tested |
| Network device configurations | Not backed up | N/A | N/A |

### 6.2 Recovery Gaps

- No documented recovery time objective (RTO) or recovery point objective (RPO) for any system
- No formal backup verification or restoration testing has ever been performed
- M365 native retention is not a substitute for backup — deleted items may be unrecoverable after retention period expires
- EHR backup and recovery capabilities have never been confirmed with the vendor
- No offline or immutable backup copy exists to protect against ransomware encryption

---

## 7. Physical Security (IT-Relevant)

| Location | Server/Comms Room | Access Control | Visitor Policy |
|----------|-------------------|---------------|----------------|
| San Fernando | Small locked closet for network equipment and NAS | Key held by IT admin and Operations Manager | Sign-in sheet at reception |
| Chaguanas | Network equipment in unlocked utility area | No restricted access | Sign-in sheet at reception |
| Couva | Network equipment on open shelf in admin area | No restricted access | None formalized |
| Point Fortin | Network equipment behind reception desk | Accessible to reception staff | None formalized |

---

## 8. Known Shadow IT and Unmanaged Risk Areas

The following unmanaged technology practices have been identified through staff interviews and observation:

1. **WhatsApp for patient communication** — Staff use personal WhatsApp accounts to confirm appointments and occasionally share lab results with patients. No consent, logging, or retention controls.

2. **Personal Google Drive** — At least 3 staff members store work documents in personal Google Drive accounts for convenience when working across locations.

3. **USB drive file transfers** — Unencrypted USB drives are used to move files between locations where network connectivity is unreliable.

4. **Shared login credentials** — Insurance portal credentials are shared among billing staff at each location. The credentials are written on sticky notes near workstations.

5. **Personal email for business use** — Some staff forward work emails to personal Gmail accounts for remote access, bypassing M365 security controls.

---

## 9. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | March 2026 | J. Maitland | Initial version |

**Next Review:** June 2026 (quarterly review) or upon any significant change to technology environment.
