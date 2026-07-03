# **TPS — Two‑Pin System Specification (v1.0)**  
### *Dual‑Anchor Stability Model for UMA Multi‑Layer Architecture*

**Document Type:** Structural Specification  
**Applies To:** All UMA modules capable of anchoring  
**Author:** Borealis S. Hedling  
**Date:** 03 July 2026  
**Status:** Active  
**Scope:** Conceptual Engine / Safety / Navigation

---

## **1. Purpose**
The Two‑Pin System (TPS) defines how UMA anchors stability across both the **conceptual architecture** and the **governance integrity layer**.  
TPS prevents premature cosmic anchoring, ensures pacing alignment, and maintains render integrity across constrained viewports (GitHub Pages, mobile, low‑power devices).

TPS is required for all modules that serve as **navigational**, **structural**, or **safety‑critical** components.

---

## **2. Overview**
TPS establishes **two distinct pins**:

1. **Map Pin** — anchors the module inside the architecture  
2. **SIAP Pin** — anchors the module inside the integrity ledger

These pins operate on different planes and must always be paired for any module that is formally anchored.

---

## **3. Pin Types**

### **3.1 Map Pin (Structural Anchor)**  
**Purpose:**  
Anchors the module inside the conceptual architecture.  
Provides a stable reference point for diagrams, mechanics, navigation, and module relationships.

**Characteristics:**  
- Lives inside the module’s own directory  
- Defines the module’s canonical role  
- Prevents conceptual drift  
- Supports multi‑layer navigation  
- Must be created before any outer‑layer expansion

**Location:**  
```
/conceptual-engine/visuals/<module>/pins/
```

**Example:**  
`AP‑01_Astrolabe_Pin.md`

---

### **3.2 SIAP Pin (Integrity Anchor)**  
**Purpose:**  
Anchors the module inside the System Integrity Alignment Protocol (SIAP).  
Records approval, rationale, pacing alignment, accessibility checks, and safety considerations.

**Characteristics:**  
- Lives inside the SIAP ledger  
- Documents the decision process  
- Prevents governance drift  
- Ensures pacing and accessibility alignment  
- Required for any module that becomes canonical

**Location:**  
```
/conceptual-engine/safety/SIAP/logs/
```

**Example:**  
`AP‑01_Astrolabe_Pin_Log.md`

---

## **4. Why TPS Exists**
TPS is required because UMA operates across **multiple conceptual planes**:

- Navigation (Astrolabe)  
- Containment (Heliosphere)  
- Infrastructure (Dyson Sphere)  
- Development (Luna Base)  
- Meta‑Index (Cosmic Forest)  
- Traversal (Thoroughfare)  
- Governance (SIAP)

Anchoring on only one plane creates instability:

- Map‑only pins → governance drift  
- SIAP‑only pins → conceptual drift  
- No pins → cosmic collapse  
- Single cosmic pin → premature anchoring + viewport bunching

TPS ensures **dual stability** across both architecture and governance.

---

## **5. Pin Lifecycle**

### **5.1 Creation**
A module may be pinned only when:

- It is fully scoped  
- It is stable across contexts  
- It renders cleanly across devices  
- It does not depend on unbuilt outer layers  
- SIAP approves pacing alignment

### **5.2 Pairing**
Every Map Pin **must** have a corresponding SIAP Pin.  
Every SIAP Pin **must** reference a Map Pin.

### **5.3 Veto**
SIAP may veto a pin if:

- the module is not yet stable  
- the viewport collapses or bunches  
- the cosmic architecture is incomplete  
- pacing alignment fails  
- accessibility fails

Example: **Cosmic Pin CP‑00 vetoed**.

### **5.4 Activation**
A pin becomes active only when:

- both pins exist  
- SIAP confirms alignment  
- the module is ready for dependency anchoring

Example: **Astrolabe Pin AP‑01 activated**.

---

## **6. Current TPS State (as of 03 July 2026)**

### **Active Pins**
- **AP‑01 Astrolabe Pin**  
  - Map Pin: `/conceptual-engine/visuals/astrolabe/pins/AP-01_Astrolabe_Pin.md`  
  - SIAP Pin: `/conceptual-engine/safety/SIAP/logs/AP-01_Astrolabe_Pin_Log.md`

### **Vetoed Pins**
- **CP‑00 Cosmic Architecture Pin**  
  - Veto logged in SIAP  
  - Deferred until outer layers exist

---

## **7. Forward Requirements**
Before any cosmic‑scale pin can be approved, the following must be built:

- Heliosphere Layer  
- Dyson Sphere Infrastructure  
- Luna Base Lab  
- Cosmic Forest Index

Only then can the cosmic architecture be safely anchored.

---

## **8. TPS Compliance**
All future UMA modules must follow TPS.  
No module may be anchored without:

- a Map Pin  
- a SIAP Pin  
- a SIAP alignment check  
- an accessibility check  
- pacing verification

TPS is now part of UMA’s core governance.

---


