# Design — AINEL/OpenSpec Bootstrap for OpenPD

## Decision summary

OpenPD adopts a three-state specification model:

```text
CURRENT  = openspec/specs/
CHANGE   = openspec/changes/<change>/
HISTORY  = openspec/changes/archive/<dated-change>/
```

`CURRENT` is normative. `CHANGE` is a delta. `HISTORY` is provenance.

OpenPD consumes AINEL externally through a pinned `ainel.yaml` ProjectBinding.

## Current baseline decomposition

The initial Current baseline is split by stable concern rather than mirroring files:

1. `core-operating-model` — profession-agnostic adaptive development behavior;
2. `consumer-binding` — boundary and bootstrap semantics for personal repositories;
3. `methodology-governance` — how OpenPD itself evolves and preserves Current/history.

This decomposition is intended to keep future changes focused. A change may affect one or more capability specs without requiring a monolithic rewrite of the whole methodology.

## Authority model

Current-state precedence is:

```text
human intent
→ safety/privacy/legal constraints
→ AGENTS.md
→ openspec/specs/
→ relevant active Change
→ accepted local explanatory docs
→ ainel.yaml
→ pinned AINEL
→ generic model knowledge
```

`methodology/*.md` remains versioned explanatory/release material. It is not a second normative Current store.

## Archive timing

### Chosen: archive inside PR

The branch contains both:

- synchronized intended post-merge Current specs;
- archived Change provenance.

Human maintainer merge is the final acceptance event.

This is appropriate for the current individual-maintainer topology and minimizes a stale-Current window after merge.

### Alternative: archive after merge

Rejected for now because it would require a second housekeeping step after every material methodology PR and temporarily leave `main` with accepted artifact changes while Current/archive closure is incomplete.

Revisit this choice if OpenPD becomes a team-maintained product with enforced multi-party review gates.

## Work tracking

GitHub Issues are the work-item provider and GitHub Pull Requests are the delivery/review carrier.

Beads is deliberately not introduced. The current need is specification/current-state discipline, not runtime multi-agent work coordination. Adding Beads without a demonstrated execution problem would violate OpenPD's minimal-change principle.

## AINEL versioning

AINEL is pinned to exact commit `8fdce08bce17aadb40a176c6e59669832a78bd15`.

A later pin update is explicit and reviewable. OpenPD does not follow AINEL `main` implicitly.

## Pattern Decision Trace

AINEL's Pattern Library is not loaded for this Change. The change concerns methodology/specification governance and does not intersect the current software-engineering pattern domains in a way that would improve the decision. `include_relevant_ainel_patterns` is therefore `false` in the ProjectBinding.

## Validation strategy

Bootstrap validation checks two things separately:

### Structural connection

- `AGENTS.md` discovers AINEL/OpenSpec rules;
- `ainel.yaml` pins AINEL and maps providers;
- OpenSpec config exists;
- Current/change/archive paths have explicit semantics.

### Semantic connection

- Current contains a materially usable baseline for the existing OpenPD product;
- Change 002 expresses the new governance behavior as a delta;
- the resulting accepted behavior is already synchronized into Current on the PR branch;
- Change provenance is retained in archive;
- a fresh-context reader can recover current behavior without reading the archive.

The final acceptance event is human merge. If the PR is not merged, none of this branch state becomes accepted Current.