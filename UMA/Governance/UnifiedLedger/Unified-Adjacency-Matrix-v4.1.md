### 📘 Unified Adjacency Matrix v4.1

**Path:** `/UMA/Governance/UnifiedLedger/Unified-Adjacency-Matrix-v4.1.md`  
**Tier:** Governance / Spatial Relations  
**Status:** Active  
**Epoch:** PEP Epoch  
**Maintainer:** Borealis S. Hedling  

---

#### 1. Matrix identity

```text
Matrix-ID: ADJ-v4.1
Previous: ADJ-v1.1
Genesis: ADJ-v1.0
Scope: Full UMA subsystem adjacency under UnifiedLedger-v4.1
Function: Canonical adjacency map for all planes, pins, and protocols
Epoch: PEP
```

---

#### 2. Embedded pin

```text
PIN: 093
Pin-Type: Protocol-Embedded
Name: Unified Adjacency Matrix v4.1
Version: 4.1
Tier: Constitutional / Spatial Governance
Status: Active

Authority:
  This pin defines the canonical adjacency relations for UMA.
  All subsystems, pins, and protocols must resolve adjacency through this matrix.

Path:
  /UMA/Governance/UnifiedLedger/Unified-Adjacency-Matrix-v4.1.md

Anchors:
  - Unified Ledger v4.1 (PIN-092)
  - Unified Ledger v4.0 (PIN-090)
  - Unified POSITION Taxonomy v4.0 (PIN-091)
  - Boundary Layer v2.0
  - SIAP Spine
  - CHS Core
  - UMM Structural Frame

Continuity-Guarantees:
  - No adjacency melt across planes
  - No orphaned subsystems
  - No conflicting adjacency definitions
  - PEP Epoch stability preserved
```

---

#### 3. Planes and adjacency

**Plane STR (Structural)**  
- **Adjacency:**  
  - STR‑CHS ↔ STR‑SIAP (routing of hypercube flows)  
  - STR‑CHS ↔ STR‑UMM (model envelope)  
  - STR‑SIAP ↔ GOV‑LED (governance routing)

**Plane GOV (Governance)**  
- **Adjacency:**  
  - GOV‑LED ↔ GOV‑CON (ledger ↔ constitution)  
  - GOV‑LED ↔ PRT‑MIG (migration protocols)  
  - GOV‑EPC ↔ PRT‑PEP (epoch markers ↔ PEPs)

**Plane STB (Stability & Containment)**  
- **Adjacency:**  
  - STB‑CNT ↔ EXD‑PLY (containment ↔ play dynamics)  
  - STB‑HRD ↔ GOV‑CON (human‑relevant constraints ↔ constitution)  
  - STB‑BL2 ↔ ADJ‑UNI (boundary layer ↔ unified adjacency)

**Plane EXD (Expressive Dynamics)**  
- **Adjacency:**  
  - EXD‑EMR ↔ STR‑CHS (emergent behavior ↔ structure)  
  - EXD‑DSC ↔ GOV‑LED (descriptors ↔ governance spine)  
  - EXD‑PLY ↔ STB‑CNT (play ↔ containment)

**Plane PRT (Protocol‑Embedded)**  
- **Adjacency:**  
  - PRT‑PEP ↔ GOV‑LED (PEPs ↔ ledger)  
  - PRT‑MIG ↔ GOV‑LED (migration ↔ ledger)  
  - PRT‑STD ↔ GOV‑CON (PEP standard ↔ constitution)

**Meta‑Plane ADJ (Adjacency)**  
- **Adjacency:**  
  - ADJ‑MTR ↔ all planes (root matrix)  
  - ADJ‑EXP ↔ EXD, STB (expanded dynamics/containment)  
  - ADJ‑UNI ↔ UnifiedLedger‑v4.1 (this matrix as canonical)

---

#### 4. Example adjacency entries

```text
Adjacency:
  STR-CHS-ROOT-01  <->  GOV-LED-EPC-UNI-01
  EXD-EMR-ROOT-01  <->  STR-CHS-GEO-01
  STB-CNT-PLY-01   <->  EXD-PLY-CORE-01
  PRT-PEP-EXD-01   <->  GOV-LED-EPC-UNI-01
  PRT-MIG-GOV-01   <->  GOV-LED-EPC-UNI-01
  ADJ-UNI-ROOT-01  <->  STB-BL2-CORE-01
```

---

#### 5. Continuity guarantees

- **No adjacency melt:** All subsystem relationships are explicit and unified.  
- **No fragmentation:** Old adjacency maps (v1.0, v1.1) are superseded but preserved as history.  
- **No drift:** POSITION and adjacency are locked together via UnifiedLedger‑v4.1.  
- **No collapse:** Boundary Layer v2.0 is anchored into ADJ‑UNI.

---

