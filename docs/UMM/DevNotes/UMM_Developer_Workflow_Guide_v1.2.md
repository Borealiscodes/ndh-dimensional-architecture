# **UMM Developer Workflow Guide v1.2**  
**Stable, Naming‑Aligned, Governance‑Compliant Developer Workflow**

**Document ID:** WF‑UMM‑DEV‑01  
**Version:** 1.2  
**Owner:** Borealis S. Hedling  
**Domain:** Developer Plane → Workflow → Governance  
**Timestamp:** 2026‑07‑03 23:47 IST  

---

# **1. Purpose**

This workflow guide defines the **correct, stable, governance‑aligned workflow** for developers working within the UMM architecture.

It ensures:

- subsystem isolation  
- naming standard compliance  
- protocol/pin alignment  
- SID alignment  
- CI enforcement  
- drift prevention  
- safety stack integration  

Explore: **Governance Order Protocol**

---

# **2. Canonical Subsystem Names (Naming Standard Integrated)**

All subsystem references in this workflow follow **SUBSYS‑NAME‑STD‑01**:

| Subsystem | Canonical Name | Plane |
|----------|----------------|-------|
| CHS | **SYS‑CHS** | Subsystem |
| CHS‑OL | **TRV‑CHS‑OL** | Traversal |
| HBR | **ID‑HBR** | Identity |
| Play Engine | **NAR‑PE** | Narrative |
| SIAP | **GOV‑SIAP** | Governance |
| Safeguards | **GOV‑SAF** | Governance |
| Safety Net | **GOV‑SN** | Governance |

Explore: **Subsystem Naming Standard**

---

# **3. High‑Level Workflow Overview**

Developers must follow this sequence:

1. **Check Naming Standard Compliance**  
2. **Create or Update Protocol**  
3. **Pin Protocol Immediately**  
4. **Update SID**  
5. **Update CI Rules**  
6. **Run Test Suites**  
7. **Commit & Push**  
8. **Open PR**  
9. **CI Validation**  
10. **Merge**

Explore: **Immediate Pinning Protocol**

---

# **4. Detailed Workflow Steps**

## **4.1 Step 1 — Naming Standard Compliance**

Before any work begins:

- ensure subsystem names follow canonical prefixes  
- ensure documentation references canonical names  
- ensure directories follow canonical subsystem names  

If naming drift is detected:

- **GOV‑SAF** flags it  
- **GOV‑SN** quarantines it  
- CI fails the PR  

Explore: **Naming Drift**

---

## **4.2 Step 2 — Create or Update Protocol**

When creating a new governance rule:

- write the protocol in `docs/UMM/Protocols/`  
- follow naming rules  
- follow governance order  

Explore: **Protocols**

---

## **4.3 Step 3 — Pin Protocol Immediately**

Per **PROTO‑PIN‑IMMEDIATE‑01**:

- create a pin in `docs/UMM/Pins/`  
- reference the protocol ID  
- ensure naming compliance  
- ensure SID alignment  

Explore: **Pinning Protocol**

---

## **4.4 Step 4 — Update SID**

SID must be updated after every governance change:

- subsystem naming  
- protocol/pin pairs  
- safety stack integration  
- CI rules  

Explore: **SID**

---

## **4.5 Step 5 — Update CI Rules**

CI must enforce:

- naming standard  
- protocol/pin alignment  
- SID alignment  
- drift vector mitigation  
- hook safety  

Explore: **CI Naming Enforcement**

---

## **4.6 Step 6 — Run Test Suites**

Run:

- Drift Vector Mitigation Test Suite  
- Hook Safety Test Suite  
- Naming Drift Test Suite  

Explore: **Drift Vector Mitigation**

---

## **4.7 Step 7 — Commit & Push**

Commit messages must:

- reference protocol/pin IDs  
- reference SID updates  
- reference CI updates  
- be naming‑standard‑compliant  

---

## **4.8 Step 8 — Open PR**

PR must include:

- protocol  
- pin  
- SID update  
- CI update  
- test suite results  

---

## **4.9 Step 9 — CI Validation**

CI validates:

- naming standard  
- protocol/pin pairs  
- SID alignment  
- safety stack alignment  
- drift vector mitigation  
- hook safety  

---

## **4.10 Step 10 — Merge**

Merge only after:

- CI passes  
- Safeguards approve  
- Safety Net shows no quarantine  
- SIAP classification is correct  

---

# **5. Safety Stack Responsibilities**

### **5.1 GOV‑SAF (Safeguards)**  
Detects:

- naming drift  
- subsystem drift  
- governance drift  
- traversal drift  
- identity drift  

### **5.2 GOV‑SN (Safety Net)**  
Quarantines:

- misnamed subsystems  
- unsafe hooks  
- drift vectors  
- governance violations  

### **5.3 GOV‑SIAP**  
Classifies:

- subsystem plane  
- governance plane  
- traversal plane  
- identity plane  
- narrative plane  

Explore: **Safety Net**

---

# **6. Developer Responsibilities**

Developers must:

- follow naming rules  
- follow governance order  
- pin protocols immediately  
- update SID after governance changes  
- update CI rules  
- run test suites  
- ensure CI passes before merging  

Explore: **Developer Handbook**

---

# **7. Roots Ledger Binding**

```
ROOTS-ENTRY-WF-UMM-DEV-01
Type: Developer Workflow Guide
Module: UMM-WF-DEV-01
Status: Active
Hash: 7d:cc:41:cd:92:fa:55
Bound: UMM, SIAP, Safeguards, Safety Net, SYS-CHS, TRV-CHS-OL, ID-HBR, NAR-PE
```

---

# **8. Document Status**

**Status:** Active  
**Version:** 1.2  
**Hash:** 7d:cc:41:cd:92:fa:55  

---

