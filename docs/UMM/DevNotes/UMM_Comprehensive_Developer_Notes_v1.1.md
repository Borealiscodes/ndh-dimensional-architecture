# **UMM Comprehensive Developer Notes v1.1**  
**Core reference notes for developers working inside the UMM architecture**

**Document ID:** DEV‑NOTES‑UMM‑01  
**Version:** 1.1  
**Owner:** Borealis S. Hedling  
**Domain:** Developer Plane → Notes → Governance  
**Timestamp:** 2026‑07‑03 23:55 IST  

---

# **1. Purpose**

These notes provide a **complete, stable, governance‑aligned overview** of how developers should understand and interact with the Universal Modular Mind (UMM) architecture.

They ensure:

- subsystem naming compliance  
- protocol/pin alignment  
- SID alignment  
- CI enforcement  
- drift‑free development  
- safety stack awareness  

Explore: **Subsystem Naming Standard**

---

# **2. Canonical Subsystem Names**

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

Explore: **SID v1.2**

---

# **3. UMM Architectural Overview**

UMM is composed of five planes:

- **Subsystem Plane** — core cognitive systems  
- **Traversal Plane** — movement between subsystems  
- **Identity Plane** — identity modeling  
- **Narrative Plane** — narrative generation  
- **Governance Plane** — rules, safety, classification  

Each plane contains one or more subsystems with strict isolation rules.

Explore: **Governance Order Protocol**

---

# **4. Developer Responsibilities**

Developers must:

- follow naming rules  
- follow governance order  
- pin protocols immediately  
- update SID after governance changes  
- update CI rules  
- run test suites  
- ensure CI passes before merging  

Explore: **Workflow Guide v1.2**

---

# **5. Protocols**

Protocols define governance rules.

They must:

- be placed in `docs/UMM/Protocols/`  
- follow naming standard  
- follow governance order  
- be pinned immediately  

Explore: **Protocols**

---

# **6. Pins**

Pins enforce protocols.

They must:

- be placed in `docs/UMM/Pins/`  
- reference protocol IDs  
- be naming‑standard‑compliant  
- be SID‑aligned  
- be created immediately after protocol creation  

Explore: **Pinning Protocol**

---

# **7. SID (Systems Integration Document)**

SID is the master integration document.

It must be updated after:

- naming changes  
- protocol creation  
- pin creation  
- safety stack updates  
- CI updates  

SID lives at:

```
docs/UMM/Integration/UMM_Systems_Integration_Document.md
```

Explore: **SID v1.2**

---

# **8. CI Enforcement**

CI enforces:

- naming standard  
- protocol/pin alignment  
- SID alignment  
- drift vector mitigation  
- hook safety  

Explore: **CI Naming Enforcement**

---

# **9. Safety Stack**

### **GOV‑SAF (Safeguards)**  
Detects drift.

### **GOV‑SN (Safety Net)**  
Quarantines drift.

### **GOV‑SIAP**  
Classifies subsystem plane.

Explore: **Safety Net**

---

# **10. Drift Types**

Developers must avoid:

- naming drift  
- subsystem drift  
- governance drift  
- traversal drift  
- identity drift  
- narrative drift  

Explore: **Naming Drift**

---

# **11. Directory Structure**

Correct structure:

```
docs/UMM/Protocols/
docs/UMM/Pins/
docs/UMM/Patches/
docs/UMM/Integration/
docs/UMM/DevNotes/
systems/UMM/<CanonicalSubsystemName>/
```

Explore: **Repo Structure**

---

# **12. Roots Ledger Binding**

```
ROOTS-ENTRY-DEV-NOTES-UMM-01
Type: Developer Notes
Module: UMM-DEV-NOTES-01
Status: Active
Hash: 4b:cc:41:cd:92:fa:77
Bound: UMM, SIAP, Safeguards, Safety Net, SYS-CHS, TRV-CHS-OL, ID-HBR, NAR-PE
```

---

# **13. Document Status**

**Status:** Active  
**Version:** 1.1  
**Hash:** 4b:cc:41:cd:92:fa:77  

---

