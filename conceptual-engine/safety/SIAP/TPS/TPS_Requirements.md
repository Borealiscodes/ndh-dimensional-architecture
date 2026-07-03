# **TPS Requirements (v1.0)**  
### *Eligibility Criteria for Map Pins and SIAP Pins*

**System:** UMA Universal  
**Subsystem:** SIAP — System Integrity Alignment Protocol  
**Document Type:** Requirements / Thresholds  
**Status:** Active  
**Last Updated:** 03 July 2026  
**Location:** `/conceptual-engine/safety/SIAP/TPS/`

---

## **1. Purpose**
The TPS Requirements define the **minimum conditions** a module must meet before it can be anchored using the Two‑Pin System.  
These requirements ensure:

- stability  
- pacing alignment  
- accessibility  
- render integrity  
- multi‑layer safety  
- SIAP compliance  

No module may be pinned unless it satisfies **all** TPS requirements.

---

## **2. Eligibility Requirements**

### **2.1 Stability Requirements**
A module must demonstrate:

- **Context Stability** — behaves consistently across environments  
- **Conceptual Stability** — fully scoped, no undefined regions  
- **Dependency Stability** — does not rely on unbuilt outer layers  
- **Semantic Stability** — terminology and roles are fixed  

**A module that shifts meaning or depends on future layers cannot be pinned.**

---

### **2.2 Accessibility Requirements**
A module must render cleanly across:

- GitHub Pages  
- GitHub Mobile  
- low‑power devices  
- narrow viewports  
- constrained layouts  

Accessibility failures include:

- ring bunching  
- quadrant collapse  
- label overlap  
- viewport compression  
- cosmic‑layer flattening  

**If the module collapses visually, it cannot be pinned.**

---

### **2.3 Pacing Requirements**
A module must be at the correct stage of development.

- Inner instruments may be pinned early  
- Outer cosmic layers may only be pinned after their prerequisites exist  
- No module may be anchored out of sequence  
- SIAP must confirm pacing alignment  

**Premature anchoring is automatically vetoed.**

---

### **2.4 Cognitive Load Requirements**
A module must maintain:

- interpretability  
- legibility  
- bounded complexity  
- safe navigation  
- non‑overwhelming structure  

If anchoring the module would:

- increase cognitive load  
- collapse conceptual layers  
- create navigational confusion  

…it cannot be pinned.

---

### **2.5 Render Integrity Requirements**
A module must:

- preserve aspect ratio  
- maintain ring spacing  
- avoid compression  
- avoid collapse under scaling  
- remain legible under zoom  

Render integrity is mandatory for Map Pins.

---

### **2.6 SIAP Governance Requirements**
A module must pass SIAP review:

- stability check  
- accessibility check  
- pacing check  
- cognitive load check  
- render integrity check  
- dependency check  

SIAP may veto any pin that fails a requirement.

---

## **3. Pin Pairing Requirements**
Every anchored module must have:

1. **Map Pin** — structural anchor  
2. **SIAP Pin** — governance anchor  

Both must reference each other.

A module with only one pin is considered **unanchored**.

---

## **4. Veto Conditions**
A pin is vetoed if:

- the module is unstable  
- the module is incomplete  
- the viewport collapses  
- the cosmic architecture is not ready  
- pacing alignment fails  
- accessibility fails  
- SIAP detects risk  

Example: **CP‑00 Cosmic Architecture Pin vetoed.**

---

## **5. Activation Requirements**
A pin becomes active only when:

- all TPS requirements are met  
- both pins exist  
- SIAP approves alignment  
- the module is ready for dependency anchoring  

Example: **AP‑01 Astrolabe Pin activated.**

---

## **6. Compliance**
All UMA modules must comply with TPS Requirements.  
Non‑compliant modules cannot be anchored and cannot serve as dependencies.

TPS Requirements are part of UMA’s core governance.

---

