# NDH Unified Navigation Map — v1.0
### *Spatial-Conceptual Routing Across UMA → UMM → NDH → Companion → Geometry*
### *Anchored to:* NDH-Integration-Spec-v1.0

---

## 0. Purpose

This document defines the **Unified Navigation Map** for the UMA-Universal Meta-Architecture:

- how a reader moves from global ROOT into NDH
- how NDH artifacts are grouped and traversed
- how geometry, governance, and companions interlock
- how mobile/desktop rendering affects navigation

It is the “**You Are Here**” system for the NDH manifold.

---

## 1. Layered Navigation Overview

### 1.1 Global Entry (Repo Root)

- **Start:** `/README.md` (Top-Level README v3.0)
- **Role:** Explains UMA / UMM / NDH at a high level
- **Primary action:** Jump into NDH via the NDH section

### 1.2 NDH Root

- **File:** `/UMA/Root/README.md` (NDH Root README v2.1)
- **Role:** NDH subsystem entrypoint
- **Primary action:** Use the NDH Artifact Index to select a dimension or companion

---

## 2. NDH Dimensional Navigation

From `/UMA/Root/README.md`, NDH is navigated via its **six dimensions**:

- Identity
- Behavior
- Continuity
- Cosmology
- Narrative
- Teleology

Each dimension has:

- a **primary MD codex/atlas**
- corresponding **SVG geometry**
- corresponding **PNG fallback**

### 2.1 Identity

- MD: `NDH-Dimensional-Identity-Atlas-v1.0.md`
- SVG: `svg/NDH-Dimensional-Identity-Atlas-v1.0.svg`
- PNG: `png/NDH-Dimensional-Identity-Atlas-v1.0.png`

### 2.2 Behavior

- MD: `NDH-Dimensional-Behavior-Codex-v1.0.md`
- SVG: `svg/NDH-Dimensional-Behavior-Codex-v1.0.svg`
- PNG: `png/NDH-Dimensional-Behavior-Codex-v1.0.png`

### 2.3 Continuity

- MD: `NDH-Dimensional-Continuity-Codex-v1.0.md`
- SVG: `svg/NDH-Dimensional-Continuity-Codex-v1.0.svg`
- PNG: `png/NDH-Dimensional-Continuity-Codex-v1.0.png`

### 2.4 Cosmology

- MD: `NDH-Myth-Engineering-Cosmology-Map-v1.0.md`
- SVG: `svg/NDH-Myth-Engineering-Cosmology-Map-v1.0.svg`
- PNG: `png/NDH-Myth-Engineering-Cosmology-Map-v1.0.png`

### 2.5 Narrative

- MD: `NDH-Narrative-Spine-v1.1.md`
- SVG: `svg/NDH-Narrative-Spine-v1.1.svg`
- PNG: `png/NDH-Narrative-Spine-v1.1.png`

### 2.6 Teleology

- MD: `NDH-Teleology-Map-v1.1.md`
- SVG: `svg/NDH-Teleology-Map-v1.1.svg`
- PNG: `png/NDH-Teleology-Map-v1.1.png`

---

## 3. Companion Navigation

Companion files extend NDH beyond pure geometry:

- `NDH-Technical-Engineering-Architectural-v1.0.md`
- `NDH-PEP-TC-Technical-Companion-v1.0.md`
- `NDH-Pin-Registry-v1.1.md`
- `PEP-Traversal-Class-v1.0.md`
- `NDH-Emergent-Case-Study-and-Analysis-v1.0.md`
- `NDH-Myth-Engineering-Companion-Stargate-v1.0.md`
- `NDH-Myth-Engineering-Integration-Companion-v1.0.md`
- `NDH-Race-Archetype-Matrix-v1.0.md`
- `NDH-PNG-Fallback-Standard-v1.0.md`
- `NDH-Visual-Compendium-v1.0.md`

### 3.1 Governance & Traversal Cluster

- Traversal Protocol: `PEP-Traversal-Class-v1.0.md`
- Pin Registry: `NDH-Pin-Registry-v1.1.md`
- PEP‑TC Companion: `NDH-PEP-TC-Technical-Companion-v1.0.md`
- Technical Companion: `NDH-Technical-Engineering-Architectural-v1.0.md`

**Use case:**  
When working on movement, pins, or geometry integration, start here.

---

## 4. Rendering-Aware Navigation

### 4.1 Desktop

- Prefer SVG in `svg/`
- Use PNG in `png/` as fallback

### 4.2 Mobile

- Prefer PNG in `png/`
- If SVG appears blank, open the corresponding PNG

Navigation instructions in NDH docs should always:

- mention both SVG and PNG paths
- indicate which is primary for the current context

---

## 5. Recommended Navigation Flows

### 5.1 Conceptual Onboarding Flow

1. `/README.md` → global overview  
2. `/UMA/Root/README.md` → NDH overview  
3. `NDH-Visual-Compendium-v1.0.md` → visual manifold  
4. Dimensional codices (Identity, Behavior, Continuity, Cosmology, Narrative, Teleology)

### 5.2 Engineering / Governance Flow

1. `/UMA/Root/README.md` → NDH artifact index  
2. `NDH-Technical-Engineering-Architectural-v1.0.md`  
3. `PEP-Traversal-Class-v1.0.md`  
4. `NDH-Pin-Registry-v1.1.md`  
5. Geometry SVG/PNG in `svg/` and `png/`

---

## 6. Versioning

```text
Version: v1.0
Status: Active
Class: NDH / Navigation / Map
Anchor: NDH-Integration-Spec-v1.0
