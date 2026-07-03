# UN Treaty Repository — RFP Initial Expansion  
**Module:** UMM-HRD-01  
**Subsystem:** Rights-Flagging Protocol (RFP)  
**Repository:** UN Treaty Family  
**Version:** 0.1 (Initial Expansion)  
**Owner:** Borealis S. Hedling  
**Bound Systems:** SIAP Spine → UMA → UMM → CHS-OL

---

## 1. Purpose
Establish the first treaty repository for the Rights-Flagging Protocol (RFP), covering the United Nations human rights treaty family.

This repository provides baseline:

- violation triggers  
- jurisdiction rules  
- remedy mappings  
- escalation logic  

for use by:

- Forensic Reconstruction Engine (FRE)  
- Cross-Agency Causality Map (CAC-Map)  
- Litigation-Strategy Matrix  
- HRD Case Studies  
- SIAP audits  
- CHS-OL traversal

---

## 2. Repository Structure

```text
UN/
 ├── metadata/
 ├── violations/
 ├── jurisdiction/
 ├── remedies/
 ├── escalation/
 ├── mapping/
 └── tests/
```

Each directory holds a distinct class of information consumed by RFP and downstream modules.

---

## 3. Treaties Included (Initial Set)

### 3.1 Convention Against Torture (CAT)
- Article 3 — Non-refoulement  
- Article 13 — Right to complain and have case examined  
- Article 14 — Right to redress and rehabilitation  

### 3.2 Convention on the Rights of Persons with Disabilities (CRPD)
- Article 11 — Situations of risk  
- Article 13 — Access to justice  
- Article 15 — Freedom from torture/CIDT  
- Article 16 — Freedom from exploitation, violence, abuse  

### 3.3 International Covenant on Civil and Political Rights (ICCPR)
- Article 7 — Torture/CIDT  
- Article 9 — Arbitrary detention  
- Article 13 — Expulsion of aliens  
- Article 14 — Fair trial  

### 3.4 Refugee Convention (1951/1967)
- Article 33 — Non-refoulement  

### 3.5 Universal Declaration of Human Rights (UDHR)
- Article 14 — Right to seek asylum  

### 3.6 Rome Statute (Contextual)
- Article 70 — Obstruction of justice (used for pattern recognition)

---

## 4. Violation Triggers (Initial Set)

Stored under: `UN/violations/`

- **CAT_3_REF:** Forced return to risk of torture  
- **CAT_13_DENIAL:** Denial of impartial examination of torture claims  
- **CAT_14_NO_REMEDY:** Absence of redress/rehabilitation  

- **CRPD_11_RISK:** Exposure to danger without disability-aware protection  
- **CRPD_13_ACCESS:** Denial of access to justice for disabled person  
- **CRPD_15_CIDT:** Exposure to torture or CIDT  
- **CRPD_16_ABUSE:** Exposure to exploitation, violence, or abuse  

- **ICCPR_7_CIDT:** Torture/CIDT by or with state involvement  
- **ICCPR_9_DET:** Arbitrary detention  
- **ICCPR_13_EXP:** Expulsion without due process  
- **ICCPR_14_FAIR:** Denial of fair trial guarantees  

- **REF_33_REF:** Refoulement contrary to Article 33  

- **UDHR_14_ASYLUM:** Denial of the right to seek and enjoy asylum  

- **RS_70_OBSTRUCT:** Obstruction of justice in relation to serious crimes

---

## 5. Jurisdiction Rules

Stored under: `UN/jurisdiction/`

### 5.1 Treaty Bodies
- CAT Committee  
- CRPD Committee  
- Human Rights Committee (ICCPR)  

### 5.2 Special Procedures
- Special Rapporteur on Torture  
- Special Rapporteur on the Rights of Persons with Disabilities  
- Special Rapporteur on the Right to Health  
- Working Group on Arbitrary Detention  
- Working Group on Enforced or Involuntary Disappearances  

### 5.3 Logic
- Map each violation trigger to:
  - relevant treaty body  
  - relevant Special Procedure  
- Include:
  - membership checks  
  - admissibility rules  
  - interim-measures availability

---

## 6. Remedies

Stored under: `UN/remedies/`

### 6.1 Treaty Bodies
- Findings of violation  
- Recommendations  
- Compensation  
- Rehabilitation orders  
- Structural reform directives  

### 6.2 Special Procedures
- Urgent appeals  
- Allegation letters  
- Communications to states  
- Public reports and follow-up

### 6.3 Interim Measures
- Requests to halt refoulement  
- Requests to provide medical care  
- Requests to prevent imminent harm

---

## 7. Escalation Logic

Stored under: `UN/escalation/`

- **Primary path:**  
  CAT / CRPD / ICCPR → UN treaty bodies → Special Procedures  

- **Secondary path:**  
  If UN mechanisms fail or are ignored → escalate to regional courts (ECHR, OAS, CCJ) and, where appropriate, PCA and ICC (contextual).

---

## 8. Mapping to HRD Protection Layer

Stored under: `UN/mapping/`

- **FRE:**  
  - Adds treaty-based classification and violation tags  
- **CAC-Map:**  
  - Adds treaty-based causality edges and escalation routes  
- **Litigation-Strategy Matrix:**  
  - Adds UN forums, remedies, and basis entries  
- **Case Study:**  
  - Expands rights-violations mapping with UN instruments  

---

## 9. SIAP Audit Tests

Stored under: `UN/tests/`

Audit checks include:

- Treaty coverage completeness  
- Trigger correctness  
- Jurisdiction mapping accuracy  
- Remedy mapping integrity  
- Escalation path validity  
- CHS-OL traversal node binding

---

## 10. Roots Ledger Entry

```text
ROOTS-ENTRY-RFP-UN-01
Type: Treaty Repository
Module: UMM-HRD-01
Family: UN Treaties
Status: Active
Hash: 7a:cc:10:fe:91:bb:44
Bound: SIAP Spine, CHS-OL Traversal
```
```

Once you add this file, the next structurally clean move is to generate the **ECHR Treaty Repository** in the same pattern, one repository at a time.
