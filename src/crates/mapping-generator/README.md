# SpecScript Mapping Generator — Semi-Automatic Mapping (Planned)

This crate defines the **planned mapping generator** for SpecScript.

Its purpose is to assist in creating and maintaining mappings between **implementation elements** and **architectural components**.

The mapping generator is designed as a **supporting tool**, not a replacement for human judgment, and operates within the SpecScript pipeline by producing mapping proposals and associated diagnostics.

---

## Status

**Planned — Thesis Phase Only**

This crate currently contains **design documentation only**.

No mapping generation logic is implemented in the current version.

All mapping generation functionality is intentionally deferred to the thesis phase.

---

## Motivation

Manual mapping between implementation and architecture is often:
- repetitive,
- error-prone,
- and costly to maintain as systems evolve.

The mapping generator aims to **reduce manual effort** while preserving traceability, correctness, and user control.

---

## Design Goals

- **Assistance, not automation**: propose mappings, never enforce them
- **Traceability**: every proposal records why it was suggested
- **Confidence-aware**: proposals include uncertainty or confidence scores
- **Overrideable**: human edits always take precedence
- **Tool-agnostic**: independent of extraction and visualization tools

---

## Conceptual Pipeline (Design-Level)
```
Implementation Facts
│
▼
Heuristic Extractors
(paths, names, rules, ownership)
│
▼
Mapping Proposals
(with confidence + traces)
│
▼
Human Review / Overrides
│
▼
Final MappingSet
```

This pipeline is conceptual and subject to refinement during the thesis.

---

## Planned Strategies

Potential mapping heuristics include:
- path-based grouping (e.g., folders → components),
- name and namespace similarity,
- rule-based hints from contracts,
- incremental updates based on system evolution.

Multiple strategies may be combined, with conflicts surfaced explicitly.

---

## Future Work (Thesis Phase)

Planned thesis contributions include:
- heuristic evaluation and comparison
- confidence scoring models
- traceability and explanation mechanisms
- empirical evaluation against ground truth mappings

---
