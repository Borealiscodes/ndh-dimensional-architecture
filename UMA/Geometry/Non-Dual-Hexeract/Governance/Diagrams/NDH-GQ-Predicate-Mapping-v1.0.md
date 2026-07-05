# ⭐ NDH Gating Questions → Predicate Mapping Diagram v1.0  
### Placement  
`/UMA/Geometry/Non-Dual-Hexeract/Governance/Diagrams/NDH-GQ-Predicate-Mapping-v1.0.md`

---

# ⭐ 1. Diagram Overview  
This diagram shows the **direct mapping** between:

- **Gating Questions (GQ‑1 … GQ‑9)**  
- **Boolean Predicates (G … P)**  
- **State Machine Transitions (σᵢ → σᵢ₊₁)**  
- **SID Activation Layers (AFL, CLB, DSR)**  

It is the **visual bridge** between conceptual governance and mathematical governance.

---

# ⭐ 2. Diagram (Structured NDH Format)

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                         NDH Gating Questions → Predicate Map                 │
└──────────────────────────────────────────────────────────────────────────────┘

GQ‑1: Is the geometry valid?
    → Predicate: G
    → Transition: σ1 → σ2
    → SID Layer: AFL

GQ‑2: Is divergence within safe branching limits?
    → Predicate: D
    → Transition: σ2 → σ3
    → SID Layer: AFL

GQ‑3: Did convergence successfully merge branches?
    → Predicate: C
    → Transition: σ3 → σ4
    → SID Layer: AFL

───────────────────────────────────────────────────────────────────────────────
(End of AFL domain — early‑stage adaptivity)
───────────────────────────────────────────────────────────────────────────────

GQ‑4: Are braids valid and cycles within limits?
    → Predicate: B
    → Transition: σ4 → σ5
    → SID Layer: CLB

GQ‑5: Is tangle density within allowable bounds?
    → Predicate: T
    → Transition: σ5 → σ6
    → SID Layer: CLB

GQ‑6: Are all paths resolved into Detect?
    → Predicate: R
    → Transition: σ6 → σ7
    → SID Layer: CLB

───────────────────────────────────────────────────────────────────────────────
(End of CLB domain — mid‑stage stability)
───────────────────────────────────────────────────────────────────────────────

GQ‑7: Is the Workflow Spine binding contract valid?
    → Predicate: S
    → Transition: σ7 → σ8
    → SID Layer: DSR

GQ‑8: Is temporal drift within tolerance?
    → Predicate: A
    → Transition: σ8 → σ9
    → SID Layer: DSR

GQ‑9: Is lineage valid and Production binding successful?
    → Predicate: P
    → Transition: σ9 → ACCEPT
    → SID Layer: DSR

───────────────────────────────────────────────────────────────────────────────
(End of DSR domain — late‑stage dimensional stability)
───────────────────────────────────────────────────────────────────────────────

Unified Gating Question:
    → “Is the entire NDH run correct, safe, temporally coherent, and lineage‑preserving?”
    → Unified Predicate: 𝓤 = G ∧ D ∧ C ∧ B ∧ T ∧ R ∧ S ∧ A ∧ P
    → SID Validity: SID_valid = 𝓤
```

---

# ⭐ 3. Synthesis  
> **This diagram is the authoritative mapping between NDH’s conceptual gating questions and its mathematical predicates, state transitions, and SID activation layers.  
> It is the visual governance spine of the entire NDH correctness system.**

---

