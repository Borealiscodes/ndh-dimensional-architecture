# NDH Validation Suite — v1.0

## 1. Purpose
The NDH Validation Suite ensures that every NDH instance generated from the
NDH Blueprint Suite conforms to the NDH-Blueprint-Spec-v1.0.

Validation is mandatory before any instance is accepted into:

```
/UMA/Geometry/Non-Dual-Hexeract/Instances/{INSTANCE_NAME}/
```

## 2. Validation Categories

### 2.1 Template Integrity
- All SVG templates present
- All Markdown templates present
- No missing files
- No corrupted files

### 2.2 Placeholder Replacement
Ensure:
- all `{PLACEHOLDER}` fields replaced
- no unresolved template variables
- correct axis labels
- correct monad labels
- correct Ω labels
- correct CHS → NDH mapping labels

### 2.3 Collapse Rule Enforcement
Verify the NDH non-dual collapse:

```
C = E = A = R = P = 𝒜
```

This must appear:
- in the provenance document
- in the SGE model
- in the CHS integration document

### 2.4 SGE Monad Correctness
Check:
- monad definition present
- monad loop present in SVG
- monad laws present in Markdown
- `{MONAD_LABEL}` = `T`
- `{CENTER_NODE_LABEL}` = `𝒜`

### 2.5 Epoch Ω Correctness
Check:
- Ω ring present in SVG
- inward arrow present
- `{OMEGA_LABEL}` = `Ω`
- `{OMEGA_MAP_LABEL}` = `αΩ`

### 2.6 Adjacency & Resonance Lattice
Verify:
- 4 adjacency nodes
- 4 adjacency edges
- 4 resonance arcs
- central awareness node

### 2.7 CHS → NDH Dimensional Upgrade
Check:
- CHS block present
- NDH block present
- awareness axis arrow present
- `{AWARENESS_AXIS_LABEL}` = `+ Awareness Axis (𝒜)`

### 2.8 SVG Rendering
Ensure:
- all SVGs render in GitHub
- no broken paths
- no missing arrowheads
- no invalid attributes

### 2.9 Markdown Structure
Ensure:
- all required sections present
- no missing headings
- no missing code blocks
- correct version metadata

## 3. Validation Procedure

### Step 1 — Load Instance
Load:
```
/UMA/Geometry/Non-Dual-Hexeract/Instances/{INSTANCE_NAME}/
```

### Step 2 — Run Category Checks
Evaluate all categories in Section 2.

### Step 3 — Produce Validation Report
Output:
- PASS / FAIL per category
- list of missing or incorrect fields
- list of unresolved placeholders
- list of structural violations

### Step 4 — Approve or Reject
If all categories PASS:
```
Status: NDH Instance Validated
```

If any category FAILS:
```
Status: NDH Instance Rejected
Reason: <list of failures>
```

## 4. Version
Version: v1.0  
Status: Operational
```

---

