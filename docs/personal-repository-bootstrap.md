# OpenPD Personal Repository Bootstrap

## Status

Reference procedure / MVP.

This guide describes how to connect a clean personal professional repository to OpenPD.

OpenPD is an **external professional-development operating model**. The personal repository keeps its own profession context, professional state, evidence, hypotheses, bets, experiments, inspections, privacy rules, and strategic context.

OpenPD should not be copied wholesale into the consumer repository.

## Bootstrap outcome

A minimal repository may look like:

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

The exact layout is not normative. `openpd.yaml` declares the mapping.

## Step 1 — Inspect before creating structure

If the person already has professional notes or another system, inspect it before adding new machinery.

Identify:

- current role and profession scope;
- existing professional evidence;
- current development goals or unresolved direction questions;
- existing capability or competency models;
- current strategic/life context sources;
- privacy and employer-confidentiality boundaries;
- existing repositories, notes, trackers, or learning records that should remain authoritative.

Do not duplicate useful existing systems merely to match an example layout.

## Step 2 — Define local authorities

At minimum decide where the following live:

- professional state;
- profession/capability context;
- direction hypotheses;
- development bets;
- experiments/probes;
- evidence;
- inspections;
- strategic/sustainability context, if separate.

The personal repository is authoritative for these local records.

## Step 3 — Create `openpd.yaml`

Start from [`../templates/openpd-personal-binding.yaml`](../templates/openpd-personal-binding.yaml).

Pin OpenPD to an exact commit or intentionally managed version/tag. Do not silently follow an evolving `main` for consequential decisions.

The binding should describe local paths and sources rather than force the repository to adopt one fixed layout.

## Step 4 — Establish the initial professional state

Create the smallest useful baseline.

Do not attempt a complete biography.

Capture only decision-relevant state such as:

- current role / intended work scope;
- demonstrated capabilities relevant to the current decision;
- important UNKNOWNs;
- material constraints;
- current commitments;
- current pressures/opportunities;
- unresolved professional direction questions.

Separate fact, evidence, and inference.

## Step 5 — Form at most three direction hypotheses

Use:

```text
H1 — primary plausible direction
H2 — materially different alternative, if needed
H3 — another materially different alternative, if needed
```

Do not create alternatives merely to fill three slots.

A useful direction hypothesis should be:

- consequential enough to matter;
- distinguishable from the alternatives;
- testable through real-world evidence;
- provisional rather than a committed long-range plan.

## Step 6 — Identify the key uncertainty

Ask:

> What is the smallest unresolved question whose answer could materially change which direction or action is preferred?

Avoid solving many uncertainties at once.

## Step 7 — Choose one primary development bet

The primary bet should be bounded and tied to the current uncertainty or intended professional direction.

Record:

- why this bet is primary now;
- what it is expected to change or reveal;
- commitment cap;
- what would cause it to stop or change.

## Step 8 — Design the minimum useful probe

Before execution define:

- active hypotheses;
- key uncertainty;
- action;
- time / money / energy / organizational-commitment cap;
- expected evidence;
- strengthen / weaken criteria;
- inspection date or condition.

Prefer direct work-based evidence when it can resolve uncertainty more cheaply than a course, certification, or large role commitment.

## Step 9 — Run one real cycle

Bootstrap is not complete because files exist.

Validate the binding with one real professional-development cycle:

```text
question
→ hypotheses
→ uncertainty
→ bet / probe
→ real action
→ evidence
→ inspection
→ updated state
```

## Step 10 — Inspect the methodology boundary

For early OpenPD consumers, explicitly record whether any part of the core method felt profession-specific.

Useful observations include:

- concept missing from OpenPD core;
- concept present in core but irrelevant for this profession;
- profession-specific structure that should remain local;
- duplicated profession structure that may eventually justify a profession pack;
- privacy or organizational constraints not handled by the bootstrap.

These are methodology evidence candidates, not automatic core changes.

## Example: HR Business Partner

A clean HR BP repository should contain HR-specific ontology, evidence, work cases, role hypotheses, and professional sources locally.

It should **not** inherit Project Management ontology, PM publications, or another person's experiment/evidence history.

The reusable part is the OpenPD loop and evidence discipline, not the profession content.

## Example: existing OpenPM consumer

An existing mature repository may bind OpenPD without being reorganized immediately.

The binding can map its current professional-state, hypotheses/bets, experiments, evidence, inspections, and profession ontology to OpenPD concepts. Migration should be incremental and evidence-driven rather than a large structural rewrite.
