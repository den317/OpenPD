# OpenPD Methodology Governance — Delta Specification

## Requirement: Current OpenPD behavior is authoritative in OpenSpec current specs

`openspec/specs/` SHALL be the normative Current authority for accepted durable OpenPD behavior.

A fresh-context reader SHALL be able to recover current methodology behavior from Current specs without replaying archived Changes.

### Scenario: Current-state question is asked

- GIVEN a reader needs to know what OpenPD currently requires
- WHEN current repository state is inspected
- THEN the reader SHALL start from `openspec/specs/`
- AND SHALL NOT need to reconstruct current behavior from README history, pull requests or archived Changes.

## Requirement: Material methodology changes use explicit OpenSpec deltas

Material modifications to durable OpenPD semantics SHALL be carried through an OpenSpec Change before becoming Current.

Purely editorial changes that do not alter durable behavior MAY be performed without a numbered methodology Change.

### Scenario: Core methodology semantics are changed

- GIVEN a proposal would change durable OpenPD professional-development behavior
- WHEN the modification is prepared
- THEN an OpenSpec Change SHALL identify the affected Current capability
- AND SHALL express the normative delta before the new behavior becomes Current.

## Requirement: Accepted deltas are synchronized into Current before archive completion

When an accepted Change contains durable specification deltas, the resulting behavior SHALL be synchronized into `openspec/specs/` before or as part of archive completion.

### Scenario: Artifact edit lands but Current is stale

- GIVEN artifact edits implement an accepted durable methodology change
- BUT the behavior is absent from Current specs
- WHEN completion is evaluated
- THEN the Change SHALL NOT be considered complete.

## Requirement: Archived Changes are historical provenance

`openspec/changes/archive/` SHALL contain historical proposal, rationale, design, validation and delta provenance and SHALL NOT be treated as automatically current requirements.

### Scenario: Archive conflicts with Current

- GIVEN an archived Change contains behavior later superseded in Current
- WHEN a current-state question is answered
- THEN Current SHALL take precedence
- AND archive SHALL be consulted only for rationale/history unless explicitly required.

## Requirement: OpenPD uses archive-inside-PR by default

OpenPD SHALL use archive-inside-PR while it remains an individually maintained lightweight methodology repository.

The pull request SHALL contain intended post-merge Current plus archived Change provenance, and human maintainer merge SHALL be the final acceptance/authorization event.

### Scenario: Change is ready for final review

- GIVEN artifact work and validation are complete
- AND accepted durable deltas are synchronized into Current on the branch
- WHEN the PR is prepared for merge
- THEN the Change MAY already be under the archive path in that PR
- AND merge SHALL make Current and provenance authoritative atomically on `main`.

## Requirement: Versioned methodology documents do not compete with Current

Versioned files under `methodology/` MAY preserve explanatory/release semantics but SHALL NOT replace `openspec/specs/` as Current authority.

### Scenario: Versioned document disagrees with Current

- GIVEN a versioned methodology artifact conflicts with Current
- WHEN present behavior is determined
- THEN Current SHALL govern
- AND the discrepancy SHALL be fixed explicitly without silently rewriting historical semantics.

## Requirement: AINEL is pinned and subordinate to local authority

OpenPD SHALL consume AINEL through an exact or intentionally managed ref in `ainel.yaml`, SHALL NOT silently follow AINEL `main`, and SHALL preserve explicit human intent, safety/privacy constraints, `AGENTS.md`, Current specs and accepted local decisions above generic AINEL guidance.

### Scenario: AINEL evolves upstream

- GIVEN AINEL changes after OpenPD's pinned ref
- WHEN OpenPD considers adopting that behavior
- THEN adoption SHALL be a reviewable local decision
- AND a material operating change SHALL use an OpenSpec Change.