# SpecScript DSL — Executable Architecture Contracts (Planned)

This crate defines the **planned domain-specific language (DSL)** for expressing **Executable Architecture Contracts** in SpecScript.

The DSL is intended to provide a concise, declarative way to specify:
- architectural components and their hierarchy,
- architectural rules (allowed / forbidden / optional dependencies),
- and mapping intent between implementation elements and architecture.

---

## Status

**Planned — Thesis Phase Only**

This crate currently contains **design documentation only**.

Parsing, grammar definition, and tooling support are intentionally **deferred to the thesis phase**.

No DSL implementation is used by the current SpecScript pipeline.

---

## Design Goals

- **Declarative**: focus on *what* the architecture is, not *how* to compute it
- **Deterministic**: order-independent and reproducible semantics
- **Tool-agnostic**: independent of SEE, with GXL as one backend
- **CI-friendly**: designed to produce precise diagnostics and traces
- **Composable**: supports versioning and incremental evolution of contracts

---

## Conceptual Structure (Design-Level)
```
ContractFile
├── system declaration
├── architecture
│   ├── components / modules
│   └── hierarchy (optional)
├── rules
│   ├── allow
│   ├── forbid
│   └── optional
├── mapping
│   ├── explicit mappings
│   └── overrides
└── metadata
    ├── version
    └── annotations
```

This structure is illustrative and may evolve during the thesis.

---

## Relationship to SEE

The DSL does **not** perform reflexion analysis.

Instead, DSL inputs are planned to be:
1. validated,
2. translated into standard GXL artifacts,
3. and consumed by SEE, which runs reflexion analysis and visualization.

SEE remains the execution and visualization environment.

---

## Future Work (Thesis Phase)

Planned thesis contributions include:
- formal grammar and parser
- AST with source spans
- DSL-level diagnostics
- evaluation of expressiveness and usability

---

