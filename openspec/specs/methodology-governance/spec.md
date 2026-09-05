# OpenPD Methodology Governance Specification

## Purpose

Define how OpenPD itself evolves as a methodology product while preserving one recoverable Current state, explicit change deltas and historical provenance.

## Requirements

### Requirement: Current OpenPD behavior is authoritative in OpenSpec current specs

`openspec/specs/` SHALL be the normative Current authority for accepted durable OpenPD behavior.

A fresh-context reader SHALL be able to recover current methodology behavior from Current specs without replaying archived Changes.

#### Scenario: Current-state question is asked

- GIVEN a reader needs to know what OpenPD currently requires
- WHEN current repository state is inspected
- THEN the reader SHALL start from `openspec/specs/`
- AND SHALL NOT need to reconstruct current behavior from README history, pull requests or archived Changes.

### Requirement: Material methodology changes use explicit OpenSpec deltas

Material modifications to durable OpenPD semantics SHALL be carried through an OpenSpec Change before becoming Current.

Material changes include core operating rules, consumer-binding semantics, methodology governance, durable template semantics and AINEL/OpenSpec integration behavior.

Purely editorial changes that do not alter durable behavior MAY be performed without a numbered methodology Change.

#### Scenario: Core probe semantics are changed

- GIVEN a proposal would change how OpenPD defines or selects evidence-producing probes
- WHEN the modification is prepared
- THEN an OpenSpec Change SHALL identify the affected Current capability
- AND SHALL express the normative delta before the new behavior becomes Current.

### Requirement: Accepted deltas are synchronized into Current before archive completion

When an accepted Change contains durable specification deltas, the resulting behavior SHALL be synchronized into `openspec/specs/` before or as part of archive completion.

#### Scenario: Change is accepted but Current remains stale

- GIVEN a material methodology Change has been reviewed and its artifact edits are ready
- BUT its accepted behavior is absent from Current specs
- WHEN completion is evaluated
- THEN the Change SHALL NOT be considered complete.

### Requirement: Archived Changes are historical provenance

`openspec/changes/archive/` SHALL contain historical proposal, rationale, design, validation and delta provenance.

Archived Changes SHALL NOT automatically override or supplement Current when answering current-behavior questions.

#### Scenario: Archived requirement conflicts with Current

- GIVEN an archived Change contains behavior later superseded in Current
- WHEN a current-state question is answered
- THEN Current SHALL take precedence
- AND the archive MAY be consulted only for rationale/history unless the task explicitly requires historical analysis.

### Requirement: OpenPD uses archive-inside-PR by default

OpenPD SHALL use an archive-inside-PR convention by default while it remains an individually maintained lightweight methodology repository.

The pull request SHALL contain the intended post-merge Current state plus the archived Change provenance. Human maintainer merge SHALL be the final acceptance and Engineering Intent Authorization event.

#### Scenario: Material Change is ready for review

- GIVEN artifact work and validation are complete
- AND accepted durable deltas have been synchronized into Current specs on the branch
- WHEN the Change is prepared for final review
- THEN its historical Change artifacts MAY be located under the archive path in the same PR
- AND merging the PR SHALL make the synchronized Current and its provenance authoritative on `main` atomically.

### Requirement: Versioned methodology documents preserve historical semantics without competing with Current

Files under `methodology/` MAY provide versioned explanatory or release-oriented descriptions of OpenPD.

They SHALL preserve the semantics of the version they represent and SHALL NOT silently replace `openspec/specs/` as the Current authority.

#### Scenario: Versioned document disagrees with Current

- GIVEN a versioned methodology document and Current spec disagree about present OpenPD behavior
- WHEN the discrepancy is detected
- THEN Current SHALL govern present repository behavior
- AND the discrepancy SHALL be resolved explicitly without silently rewriting historical semantics.

### Requirement: Methodology evolution remains evidence-disciplined

OpenPD SHOULD prefer methodology changes at explicit inspection/review boundaries using the sequence `recurrent defect → evidence → cause hypothesis → protocol change → expected effect → validation in subsequent cycles`.

A single person's or single profession's experience MAY create a methodology hypothesis but SHALL NOT by itself establish a universal OpenPD rule unless explicit human intent deliberately changes the product contract.

#### Scenario: One consumer reports a friction point

- GIVEN one consumer reports a methodology friction point
- WHEN OpenPD evaluates a core change
- THEN the observation MAY be recorded as evidence or a candidate issue
- AND OpenPD SHOULD inspect whether the defect recurs or generalizes before promoting a universal rule.

### Requirement: AINEL is pinned and upgrades are reviewable

OpenPD SHALL consume AINEL through `ainel.yaml` using an exact or intentionally managed ref.

OpenPD SHALL NOT silently follow changes to AINEL `main`. A material AINEL upgrade that changes OpenPD operating behavior SHALL be reviewed through an OpenSpec Change.

#### Scenario: AINEL publishes a new bootstrap rule

- GIVEN AINEL evolves after the pinned OpenPD ref
- WHEN OpenPD considers adopting the new rule
- THEN the new behavior SHALL be assessed against local needs and authority
- AND the pin SHALL change only through a reviewable repository decision.

### Requirement: Local OpenPD authority remains above external AINEL guidance

AINEL SHALL remain an external engineering operating model and SHALL NOT override explicit human intent, safety/privacy constraints, `AGENTS.md`, Current OpenPD specs or accepted local decisions.

#### Scenario: Generic AINEL guidance conflicts with OpenPD methodology boundary

- GIVEN pinned AINEL guidance suggests a generic engineering mechanism
- AND the mechanism would violate OpenPD's accepted methodology/personal-state boundary
- WHEN the conflict is resolved
- THEN OpenPD's accepted local contract SHALL prevail
- AND any deviation or AINEL upgrade MAY be raised as a reviewable change rather than applied silently.