# OpenPD Architecture

## Purpose

OpenPD separates reusable professional-development methodology from personal and profession-specific state.

The key boundary is:

```text
METHOD
  OpenPD
    ↓ binding
PERSONAL SYSTEM OF RECORD
  person's professional repository
```

OpenPD is the **producer of reusable professional-development practice**. Personal repositories are **consumers and proving grounds**.

## Responsibilities

### OpenPD owns

- the generic adaptive development loop;
- evidence and inference discipline;
- hypothesis / uncertainty / bet / probe / inspection semantics;
- default WIP limits;
- bootstrap and binding rules;
- reusable templates;
- methodology evolution rules.

### Consumer repositories own

- current professional state;
- profession ontology and capability models;
- accepted personal evidence;
- personal hypotheses and bets;
- profession-specific sources and trends;
- local strategic context;
- private/employer-sensitive material;
- local repository layout and tooling.

## External operating model

A consumer connects through `openpd.yaml` rather than copying OpenPD into the repository.

```text
Human professional question
        ↓
Consumer repository state
        ↓
OpenPD binding
        ↓
Relevant professional context
        ↓
Hypotheses + key uncertainty
        ↓
Bounded bet / probe
        ↓
Real-world result
        ↓
Evidence
        ↓
Inspection
        ↓
Consumer repository update
```

The consumer repository remains authoritative for its personal state. OpenPD provides method, not personal truth.

## Current two-layer model

For v0.1 use only:

```text
OpenPD Core
    ↓
personal professional repository
```

Do not create a profession layer just because two professions differ.

A reusable profession pack becomes justified only when repeated independent consumers show that the same profession-specific ontology, capability model, radar, or source structure is being duplicated.

Possible future shape, if evidence warrants it:

```text
OpenPD Core
    ↓
Profession Pack
    ↓
Personal Repository
```

Until then, profession-specific material remains local to the person's repository.

## Cross-profession validation

The first architectural test is whether a Project Manager and an HR Business Partner can use the same OpenPD core loop while keeping materially different profession content local.

Evidence that strengthens the architecture:

- both can represent state, hypotheses, uncertainty, bets, probes, evidence, and inspections without PM-specific concepts;
- profession-specific differences remain local;
- methodology changes triggered by one case improve or at least do not distort the other case.

Evidence that weakens it:

- recurring need for PM-specific concepts in the core;
- large amounts of per-profession conditional logic in OpenPD;
- consumer repositories cannot express required state without copying methodology internals;
- the same profession-specific structures are repeatedly duplicated across independent users.
