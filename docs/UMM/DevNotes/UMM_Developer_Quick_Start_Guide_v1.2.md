# **UMM Developer Quick Start Guide v1.2**  
**Rapid onboarding for developers working inside the UMM architecture**

**Document ID:** QSG‑UMM‑DEV‑01  
**Version:** 1.2  
**Owner:** Borealis S. Hedling  
**Domain:** Developer Plane → Quick Start → Governance  
**Timestamp:** 2026‑07‑03 23:53 IST  

---

# **1. Purpose**

This Quick Start Guide provides a **fast, safe, governance‑aligned entry point** for developers working within the Universal Modular Mind (UMM) architecture.

It ensures:

- subsystem naming compliance  
- protocol/pin alignment  
- SID alignment  
- CI enforcement  
- drift‑free development  
- safety stack integration  

Explore: **Naming Standard**

---

# **2. Canonical Subsystem Names (Mandatory)**

All subsystem references must follow **SUBSYS‑NAME‑STD‑01**:

| Subsystem | Canonical Name | Plane |
|----------|----------------|-------|
| CHS | **SYS‑CHS** | Subsystem |
| CHS‑OL | **TRV‑CHS‑OL** | Traversal |
| HBR | **ID‑HBR** | Identity |
| Play Engine | **NAR‑PE** | Narrative |
| SIAP | **GOV‑SIAP** | Governance |
| Safeguards | **GOV‑SAF** | Governance |
| Safety Net | **GOV‑SN** | Governance |

Explore: **SID**

---

# **3. Quick Start Workflow**

This is the **minimum required workflow** for any developer action inside UMM.

---

## **Step 1 — Clone the Repository**

Clone the repo and navigate to the UMM docs:

```
git clone https://github.com/Borealiscodes/uma-universal.git
cd uma-universal/docs/UMM
```

Check the structure:

- `Protocols/`  
- `Pins/`  
- `Patches/`  
- `Integration/`  
- `DevNotes/`

Explore: **Repo Structure**

---

## **Step 2 — Verify Naming Standard Compliance**

Before making any change:

- ensure subsystem names follow canonical prefixes  
- ensure documentation references canonical names  
- ensure directories follow canonical subsystem names  

If drift is found:

- **GOV‑SAF** flags it  
- **GOV‑SN** quarantines it  
- CI fails the PR  

Explore: **Naming Drift**

---

## **Step 3 — Create or Update a Protocol**

Protocols define governance rules.

Place new protocols in:

```
docs/UMM/Protocols/
```

Protocol requirements:

- clear purpose  
- subsystem alignment  
- naming standard compliance  
- governance order compliance  

Explore: **Protocols**

---

## **Step 4 — Pin the Protocol Immediately**

Per **PROTO‑PIN‑IMMEDIATE‑01**, every protocol must be pinned immediately.

Place pins in:

```
docs/UMM/Pins/
```

Pins must:

- reference the protocol ID  
- enforce the protocol  
- be naming‑standard‑compliant  
- be SID‑aligned  

Explore: **Pinning Protocol**

---

## **Step 5 — Update SID**

SID must be updated after every governance change.

SID lives at:

```
docs/UMM/Integration/UMM_Systems_Integration_Document.md
```

SID updates must include:

- subsystem naming  
- protocol/pin pairs  
- safety stack integration  
- CI rules  

Explore: **SID v1.2**

---

## **Step 6 — Update CI Rules**

CI must enforce:

- naming standard  
- protocol/pin alignment  
- SID alignment  
- drift vector mitigation  
- hook safety  

Explore: **CI Naming Enforcement**

---

## **Step 7 — Run Test Suites**

Run:

- Drift Vector Mitigation Test Suite  
- Hook Safety Test Suite  
- Naming Drift Test Suite  

Explore: **DVM Protocol**

---

## **Step 8 — Commit & Push**

Commit messages must:

- reference protocol/pin IDs  
- reference SID updates  
- reference CI updates  
- be naming‑standard‑compliant  

---

## **Step 9 — Open PR**

PR must include:

- protocol  
- pin  
- SID update  
- CI update  
- test suite results  

---

## **Step 10 — CI Validation & Merge**

CI validates:

- naming standard  
- protocol/pin pairs  
- SID alignment  
- safety stack alignment  
- drift vector mitigation  
- hook safety  

Merge only after:

- CI passes  
- Safeguards approve  
- Safety Net shows no quarantine  
- SIAP classification is correct  

---

# **4. Safety Stack Summary**

### **GOV‑SAF (Safeguards)**  
Detects drift.

### **GOV‑SN (Safety Net)**  
Quarantines drift.

### **GOV‑SIAP**  
Classifies subsystem plane.

Explore: **Safety Net**

---

# **5. Developer Responsibilities**

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

# **6. Roots Ledger Binding**

```
ROOTS-ENTRY-QSG-UMM-DEV-01
Type: Developer Quick Start Guide
Module: UMM-QSG-DEV-01
Status: Active
Hash: 9f:cc:41:cd:92:fa:66
Bound: UMM, SIAP, Safeguards, Safety Net, SYS-CHS, TRV-CHS-OL, ID-HBR, NAR-PE
```

---

# **7. Document Status**

**Status:** Active  
**Version:** 1.2  
**Hash:** 9f:cc:41:cd:92:fa:66  

---

