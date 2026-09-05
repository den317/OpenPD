# Validation — Bootstrap OpenPD with AINEL and OpenSpec Current

## Status

**READY FOR HUMAN ACCEPTANCE.**

This Change uses the repository's chosen archive-inside-PR convention. The branch represents the intended post-merge state. Human maintainer merge is the final acceptance/authorization event and therefore remains pending while the PR is open.

## Inputs inspected

- current `den317/OpenPD` `AGENTS.md`;
- current OpenPD README, architecture and operating-model v0.1;
- AINEL `docs/project-bootstrap-and-usage.md`;
- AINEL `docs/providers/openspec-project-binding.md`;
- AINEL ProjectBinding template;
- AINEL current Project Bootstrap specification;
- AINEL OpenSpec configuration conventions;
- pinned AINEL commit `8fdce08bce17aadb40a176c6e59669832a78bd15`.

## Structural validation

### ProjectBinding discovery

PASS — `ainel.yaml` identifies:

- repository `den317/OpenPD`;
- exact AINEL ref;
- OpenSpec current/change/archive paths;
- `existing-system` baseline state;
- GitHub Issues work-item provider;
- GitHub Pull Requests delivery provider;
- individual collaboration topology;
- human maintainer as material authorization/acceptance authority.

### Provider semantics

PASS — the binding explicitly distinguishes:

```text
openspec/specs/              Current
openspec/changes/            in-flight delta workspace
openspec/changes/archive/    historical provenance
```

PASS — accepted durable deltas are required to reach Current before/as part of archive completion.

PASS — archive-inside-PR timing and final human merge acceptance are documented.

## Existing-system baseline validation

OpenPD already had accepted behavior from Change 001, so an empty baseline would have been invalid.

PASS — Current now contains materially usable specifications for:

- `core-operating-model`;
- `consumer-binding`;
- `methodology-governance`.

The first two specs formalize accepted repository behavior already present in README/docs/methodology. The third includes the new governance behavior introduced by this Change.

## Delta validation

PASS — Change 002 records a dedicated `methodology-governance` delta specification rather than relying only on prose edits.

PASS — the new durable governance behavior has been synchronized into `openspec/specs/methodology-governance/spec.md` on the same branch.

## Authority validation

PASS — local precedence is explicit in `docs/ainel-integration.md`.

PASS — Current OpenSpec specs outrank archived Change history for current-state questions.

PASS — versioned `methodology/` artifacts are preserved as explanatory/release artifacts rather than a competing normative Current source.

PASS — AINEL is external and subordinate to explicit human intent, safety/privacy constraints, local repository contract and Current OpenPD specs.

## Fresh-context recovery test

A fresh reader starting from:

1. `AGENTS.md`;
2. `ainel.yaml`;
3. `openspec/specs/`;

can answer the following without reading the archived Change:

- OpenPD uses an adaptive hypothesis/bet/probe/inspection loop;
- active direction hypotheses are limited to at most three by default;
- one primary development bet is maintained by default;
- evidence and inference remain distinct;
- consumer repositories own personal/profession-specific state;
- OpenPD is consumed through an explicit external binding;
- Current OpenPD behavior is authoritative in `openspec/specs/`;
- material methodology changes use OpenSpec deltas;
- accepted deltas must reach Current before closure;
- archive is historical provenance;
- archive-inside-PR is the current local convention;
- AINEL is pinned and upgrades are reviewable.

Result: **PASS**.

## Scope integrity

PASS — no personal career history or profession-specific capability model was introduced into OpenPD Core.

PASS — Beads, CI automation and additional framework layers were not introduced without a demonstrated need.

## Remaining acceptance condition

The only remaining gate is the declared human-governed one:

```text
human maintainer reviews PR
→ accepts intended Current + provenance
→ merges PR
→ Change 002 becomes accepted on main
```

If the PR is rejected or not merged, this branch does not become OpenPD Current.