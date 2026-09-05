# OpenPD — Open Professional Development

OpenPD is an external, profession-agnostic operating model for **evidence-driven professional development**.

It is not a personal career repository and not a repository for any one profession. OpenPD defines the reusable method by which a person can inspect professional reality, maintain a small set of trajectory hypotheses, choose one bounded development bet, run cheap evidence-producing probes, inspect the result, and adapt.

Personal repositories remain the durable system of record for that person's professional state, evidence, hypotheses, bets, experiments, inspections, and profession-specific context.

## Core loop

```text
current professional state
→ pressure / opportunity
→ ≤3 direction hypotheses
→ key uncertainty
→ 1 primary development bet
→ minimum useful evidence-producing probe set
→ real work / reality
→ evidence
→ inspect
→ adapt
→ next bounded bet
```

Canonical optimization target:

```text
maximum decision-relevant learning
per unit of time / energy / money / commitment
```

OpenPD prefers a short probe that can materially change the decision over a detailed long-range roadmap created under high uncertainty.

## OpenPD and personal repositories

OpenPD follows an external-operating-model pattern:

```text
                    OpenPD
          methodology + bootstrap
                    │
          ┌─────────┼─────────┐
          ▼         ▼         ▼
      PM personal  HRBP      future
         repo      personal  personal
                    repo      repo
```

A personal repository **consumes** OpenPD through an explicit `openpd.yaml` binding. It does not copy OpenPD wholesale and does not inherit another person's professional history.

Minimal personal repository after bootstrap:

```text
personal-professional-repo/
├── AGENTS.md
├── openpd.yaml
├── profession/
├── professional-state/
├── hypotheses/
├── bets/
├── experiments/
├── evidence/
├── inspections/
└── insights/
```

The exact layout is local. The binding records how local artifacts map to OpenPD concepts.

## What belongs here

OpenPD contains only reusable professional-development machinery:

- operating principles and decision rules;
- evidence discipline;
- hypothesis / bet / probe / inspection semantics;
- bootstrap and binding guidance;
- reusable templates;
- methodology evolution rules;
- examples that are sanitized and non-authoritative.

OpenPD must not contain a person's private career history, employer-confidential material, personal assessments, personal hypotheses, or profession-specific conclusions presented as universal truth.

## Current architecture

The current model deliberately has only two layers:

```text
OpenPD Core
    ↓
personal professional repository
```

A reusable profession-specific pack (for example `openpd-hrbp`) should be extracted only after repeated use demonstrates that multiple people in the same profession need the same ontology, radar, capability model, or source structure. Do not create profession packs speculatively.

## Bootstrap

See [`docs/personal-repository-bootstrap.md`](docs/personal-repository-bootstrap.md).

The machine-readable binding template is [`templates/openpd-personal-binding.yaml`](templates/openpd-personal-binding.yaml).

## Methodology status

OpenPD starts as an **experimental operating model**. The first important validation is cross-profession use: whether the same core loop works for materially different professions without silently importing Project Management assumptions.

Methodology changes should be driven by observed recurrent defects at inspection boundaries, not by rewriting the method after every unsatisfying answer.

See [`methodology/openpd-operating-model-v0.1.md`](methodology/openpd-operating-model-v0.1.md) and [`docs/methodology-evolution.md`](docs/methodology-evolution.md).
