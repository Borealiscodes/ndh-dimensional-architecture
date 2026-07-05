# 📘 UMA Adjacency Matrix — Version 1.1  
**Path:** `/UMA/Governance/Adjacency/AdjacencyMatrix-v1.1.md`  
**Status:** Active  
**Mode:** Expansion (adds CHS‑OL, Play Engine, HRD)  
**Maintainer:** Borealis S. Hedling  
**Last Updated:** 2026‑07‑05  

---

## 1. Overview

Adjacency Matrix v1.1 extends v1.0 by explicitly mapping relationships between:

- UMA Core  
- SIAP Spine  
- CHS / CHS‑OL  
- UMM / HRD  
- Play Engine  
- Roots / Ledger  
- Lifecycle Chain  

It encodes **who touches whom**, **under what rules**, and **through which pins**, so traversal and containment remain predictable.

---

## 2. Subsystem list

- **UMA:** Core lattice (`PIN‑001`)  
- **SIAP:** Routing spine (`PIN‑002`)  
- **CHS:** Base hypercube (`PIN‑003`)  
- **CHS‑OL:** Operational layer (`PIN‑004`)  
- **UMM:** Structural frame (`PIN‑005`)  
- **HRD:** Protection layer (`PIN‑021`)  
- **PlayEngine:** Containment + narrative (`PIN‑050–052`, `PIN‑024`)  
- **Roots:** Registry + Ledger (`PIN‑060–061`)  
- **Adjacency:** Matrix itself (`PIN‑070–071`)  
- **Lifecycle:** Chain (`PIN‑080–081`)  

---

## 3. High‑level adjacency table

```markdown
Subsystem    | Adjacent To                 | Mode              | Notes
-------------|-----------------------------|-------------------|-------------------------------
UMA          | SIAP, CHS, UMM, Roots       | Structural        | Core lattice; ancestor of most
SIAP         | UMA, CHS, PlayEngine        | Routing           | Governs traversal + message flow
CHS          | UMA, CHS‑OL, SIAP           | Geometric         | Base hypercube; partial completion ok
CHS‑OL       | CHS, Lifecycle, PlayEngine  | Operational       | Traversal plane; hooks into IC/OC
UMM          | UMA, HRD, Roots             | Structural        | Meta‑model envelope
HRD          | UMM, Myth‑Engineering       | Protective        | Human‑Relevant Design constraints
PlayEngine   | SIAP, CHS‑OL, Lifecycle     | Containment       | IC/OOC boundary + bleed‑control
Roots        | UMA, UMM, Adjacency         | Provenance        | Lineage + registry alignment
Adjacency    | All subsystems              | Mapping           | Defines allowed edges + constraints
Lifecycle    | CHS‑OL, PlayEngine, UMA     | Temporal          | Evolution + activation sequencing
```

---

## 4. Key adjacency rules

- **UMA ↔ SIAP:**  
  **Rule:** All subsystem routing must pass through SIAP; UMA defines allowed structural endpoints.  

- **CHS ↔ CHS‑OL:**  
  **Rule:** CHS‑OL may operate on partial CHS geometry as long as adjacency + containment pins are respected.  

- **PlayEngine ↔ CHS‑OL:**  
  **Rule:** IC/OOC traversal uses CHS‑OL as an operational plane; Play Engine enforces bleed‑control (`PIN‑024`).  

- **UMM ↔ HRD:**  
  **Rule:** Any UMM extension must pass HRD constraints before becoming active in traversal or governance.  

- **Roots ↔ Adjacency:**  
  **Rule:** No new adjacency edge is valid unless it can be traced in Roots lineage.  

- **Lifecycle ↔ PlayEngine / CHS‑OL:**  
  **Rule:** Subsystem activation/deactivation must respect lifecycle pins and containment rules.

---

## 5. 5D traversal note

Even without full CHS cube completion:

- SIAP provides **routing spine**.  
- Adjacency Matrix v1.1 provides **edge constraints**.  
- CHS‑OL provides **operational traversal plane**.  
- Play Engine provides **containment + bleed‑control**.  
- Roots + Lifecycle provide **provenance + temporal coherence**.

Result:  
**5D traversal is allowed within defined subsystems (e.g., Play Engine) as long as adjacency and containment rules are obeyed.**

---

## 6. Tag

`adjacency`, `siap`, `chs`, `play-engine`, `hrd`, `roots`, `lifecycle`, `the-spine-works`
