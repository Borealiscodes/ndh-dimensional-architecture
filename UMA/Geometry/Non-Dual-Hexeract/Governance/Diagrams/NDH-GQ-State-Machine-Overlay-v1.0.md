### NDH Gating Questions → State Machine Overlay v1.0  
**Placement:**  
`/UMA/Geometry/Non-Dual-Hexeract/Governance/Diagrams/NDH-GQ-State-Machine-Overlay-v1.0.md`

---

### 1. Purpose  
This overlay ties **each Gating Question (GQ‑1…GQ‑9)** directly onto the **Algebraic State Machine** \(\sigma_1 \rightarrow \sigma_9\), so you can see:

- which **state** each question lives on  
- which **predicate** answers it  
- which **transition** it gates  

---

### 2. Overlay diagram (structured)

```text
┌──────────────────────────────────────────────────────────────────────────────┐
│                 NDH Gating Questions → Algebraic State Machine Overlay       │
└──────────────────────────────────────────────────────────────────────────────┘

[Start]
  |
  |  GQ‑1: "Is the geometry valid?"
  |   → Predicate: G
  v
σ1 GeometryActivated
  |
  |  If G = true  → σ2
  |  If G = false → σE


σ2 DivergenceApplied
  |
  |  GQ‑2: "Is divergence within safe branching limits?"
  |   → Predicate: D
  |
  |  If D = true  → σ3
  |  If D = false → σE


σ3 ConvergenceApplied
  |
  |  GQ‑3: "Did convergence successfully merge branches?"
  |   → Predicate: C
  |
  |  If C = true  → σ4
  |  If C = false → σE


σ4 BraidApplied
  |
  |  GQ‑4: "Are braids valid and cycles within limits?"
  |   → Predicate: B
  |
  |  If B = true  → σ5
  |  If B = false → σE


σ5 DensityEvaluated
  |
  |  GQ‑5: "Is tangle density within allowable bounds?"
  |   → Predicate: T
  |
  |  If T = true  → σ6
  |  If T = false → σE


σ6 ResolvedToDetect
  |
  |  GQ‑6: "Are all paths resolved into Detect?"
  |   → Predicate: R
  |
  |  If R = true  → σ7
  |  If R = false → σE


σ7 SpineBound
  |
  |  GQ‑7: "Is the Workflow Spine binding contract valid?"
  |   → Predicate: S
  |
  |  If S = true  → σ8
  |  If S = false → σE


σ8 TemporalBound
  |
  |  GQ‑8: "Is temporal drift within tolerance?"
  |   → Predicate: A
  |
  |  If A = true  → σ9
  |  If A = false → σE


σ9 ProductionBound
  |
  |  GQ‑9: "Is lineage valid and Production binding successful?"
  |   → Predicate: P
  |
  |  If P = true  → [ACCEPT]
  |  If P = false → σE


σE ErrorState
  |
  |  Any failed GQ (any false predicate)
  |  → Terminal error, no further transitions
```

---

### 3. Unified view  

- **Every state** has exactly **one gating question**.  
- **Every transition** is controlled by that question’s **predicate**.  
- Any **“no”** answer (predicate = false) routes to **σE** and halts the run.

This overlay is the clean visual proof that NDH is entirely **question‑gated, predicate‑driven, state‑machine‑controlled**.
