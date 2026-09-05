# OpenPD AINEL Integration

## Purpose

OpenPD is itself developed as a methodology product. It consumes `den317/AINEL` as an external engineering operating model and uses OpenSpec as the carrier for durable current behavior and reviewable methodology changes.

AINEL is pinned in [`ainel.yaml`](../ainel.yaml). Updating that pin is a reviewable OpenPD change rather than an implicit adoption of future AINEL `main` behavior.

## Current, Change, History

OpenPD uses three distinct states:

```text
CURRENT
openspec/specs/
    current accepted OpenPD behavior

CHANGE
openspec/changes/<change>/
    proposed/in-flight delta

HISTORY
openspec/changes/archive/<dated-change>/
    accepted historical rationale, design, validation and provenance
```

A fresh-context reader answering a current-state question MUST start from `openspec/specs/`. Archived Changes are not required to reconstruct Current.

Versioned files under `methodology/` remain useful explanatory/release artifacts and preserve historical semantics. They are not a competing Current authority. If a versioned methodology document and current OpenSpec specs conflict, current specs govern current repository behavior and the inconsistency should be fixed explicitly.

## Local precedence

For material OpenPD work use this precedence:

1. explicit human intent for the current task;
2. safety, privacy, legal and confidentiality constraints;
3. `AGENTS.md`;
4. current `openspec/specs/`;
5. the relevant active `openspec/changes/<change>/` delta;
6. accepted local architecture/methodology documentation consistent with Current;
7. `ainel.yaml`;
8. pinned AINEL operating model;
9. generic model knowledge.

Historical archived Changes do not outrank Current merely because they contain more detail.

## What requires an OpenSpec Change

Use a Change for material modifications to durable OpenPD behavior, including:

- core professional-development semantics;
- evidence, hypothesis, bet, probe or inspection rules;
- methodology governance;
- personal-repository binding/bootstrap semantics;
- profession-pack extraction rules;
- durable template semantics;
- AINEL/OpenSpec integration behavior;
- upgrades of the pinned AINEL contract when they alter OpenPD operating behavior.

Pure typo fixes, broken links, formatting-only edits and other changes that do not alter durable behavior MAY be handled without a numbered methodology Change.

## Normal material-change flow

```text
human intent / issue
        ↓
read AGENTS.md + ainel.yaml
        ↓
recover relevant CURRENT specs
        ↓
create openspec/changes/<change>/
        ↓
proposal + delta specs + design as needed + tasks
        ↓
change methodology/docs/templates/examples as required
        ↓
validation.md with inspectable evidence
        ↓
synchronize accepted delta into openspec/specs/
        ↓
archive Change inside the same PR
        ↓
human maintainer review + merge
        ↓
main contains synchronized CURRENT + historical provenance
```

The repository uses **archive-inside-PR** by default because it is a small individual-maintainer methodology repository. The PR branch describes the intended post-merge state. Human maintainer merge is the final acceptance/authorization event.

If team topology or delivery enforcement changes later, this convention must be reviewed rather than assumed to remain correct.

## Change artifact expectations

A material Change normally contains:

```text
openspec/changes/<change>/
├── proposal.md
├── specs/
│   └── <affected-capability>/spec.md
├── design.md        # when alternatives/architecture need explicit rationale
├── tasks.md
└── validation.md
```

Do not create documents mechanically when they carry no useful decision information. A purely procedural change may not need a large design document; a behavior change must still make its normative delta explicit.

## Current baseline policy

OpenPD is an existing system, not greenfield. Therefore `openspec/specs/` must contain a materially usable baseline.

Current specs should answer, without replaying history:

- what the core operating model requires;
- what belongs in OpenPD versus a consumer repository;
- how consumer binding works;
- how OpenPD methodology itself is allowed to evolve.

Do not let Current become a zombie Source of Truth while new semantics accumulate only in README, methodology documents, PRs or archived Changes.

## Verification and close-loop rule

Before a material Change is ready for merge, verify as applicable:

1. current relevant specs were recovered;
2. the Change expresses the delta rather than silently rewriting history;
3. implementation/artifact changes match the delta;
4. validation evidence is inspectable;
5. accepted durable behavior is synchronized into Current;
6. the archived Change contains rationale/provenance;
7. a fresh reader can recover the resulting behavior from Current alone.

If accepted behavior exists only in an archived Change after merge, the Change is not complete.

## AINEL upgrade rule

`ainel.yaml` pins AINEL to an exact commit. Do not silently move to a newer AINEL ref.

Upgrade flow:

```text
new AINEL capability / fix
→ assess relevance to OpenPD
→ OpenSpec Change when operating behavior is affected
→ update pin
→ validate local binding
→ accept / reject
```

OpenPD remains authoritative for its product decisions; AINEL provides the external engineering operating model.