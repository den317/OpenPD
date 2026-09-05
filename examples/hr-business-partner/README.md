# HR Business Partner — OpenPD consumer example

This is a **sanitized structural example**, not a ready-made HR competency model and not a personal repository.

The purpose is to demonstrate the OpenPD boundary for the first cross-profession validation case.

## What remains local to the HRBP repository

An HR Business Partner consumer should keep locally:

- HR-specific professional ontology and competency/capability models;
- current role context;
- personal work cases and evidence;
- HR market/profession sources and trends;
- personal direction hypotheses;
- current development bet and probes;
- inspections and insights;
- employer confidentiality rules;
- strategic/sustainability context relevant to that person.

OpenPD does not provide a universal HRBP capability model in v0.1.

## What comes from OpenPD

The reusable layer is:

```text
current professional state
→ pressure / opportunity
→ ≤3 direction hypotheses
→ key uncertainty
→ 1 primary development bet
→ minimum useful probe
→ real-world evidence
→ inspection
→ adapt
```

plus the evidence-discipline and methodology-evolution rules.

## Suggested clean repository shape

```text
hrbp-professional-development/
├── AGENTS.md
├── openpd.yaml
├── profession/
│   ├── role-context.md
│   └── capability-model.md
├── professional-state/
│   └── current.md
├── hypotheses/
├── bets/
├── experiments/
├── evidence/
├── inspections/
└── insights/
```

This is only a starting layout. A mature existing system should be mapped through `openpd.yaml` rather than reorganized for cosmetic consistency.

## First validation cycle

The first HRBP use should explicitly test this hypothesis:

> OpenPD Core can support evidence-driven professional development for HR Business Partner work without importing Project Management concepts into the core methodology.

Useful methodology evidence includes:

- core concepts that transfer cleanly;
- concepts that feel PM-specific despite generic wording;
- missing concepts required across professions;
- HR-specific structures that correctly remain local;
- recurring HR structures that could eventually justify an HR profession pack if independent consumers repeat them.
