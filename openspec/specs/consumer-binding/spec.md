# OpenPD Consumer Binding Specification

## Purpose

Define the current accepted boundary between reusable OpenPD methodology and the personal professional repositories that consume it.

## Requirements

### Requirement: OpenPD is consumed as an external operating model

OpenPD SHALL be consumed by a personal professional repository as an external operating model rather than copied wholesale into the consumer repository.

A consumer repository SHALL remain authoritative for its own professional state, personal evidence, hypotheses, bets, experiments, inspections, strategic context, privacy rules and profession-specific context.

#### Scenario: A new HR Business Partner adopts OpenPD

- GIVEN an HR Business Partner wants to use OpenPD
- WHEN a personal professional repository is bootstrapped
- THEN the repository SHALL contain the person's own professional state and evidence
- AND SHALL reference OpenPD externally instead of inheriting another person's repository history.

### Requirement: Consumer binding is explicit and pinned

A consumer repository using OpenPD SHALL record an explicit `openpd.yaml` binding or an equivalent local contract that identifies the OpenPD repository/ref and maps local professional-development artifacts to OpenPD concepts.

When reproducibility matters, the consumer SHALL pin an exact OpenPD commit or intentionally managed version/tag rather than implicitly following moving `main` behavior.

#### Scenario: OpenPD evolves upstream

- GIVEN a consumer is pinned to an accepted OpenPD ref
- WHEN OpenPD `main` changes
- THEN the consumer's operating behavior SHALL NOT silently change
- AND adopting the newer OpenPD behavior SHALL remain a reviewable local decision.

### Requirement: Bootstrap preserves useful local systems

OpenPD consumer bootstrap SHALL inspect existing professional notes, evidence stores, capability models, strategic-context repositories and privacy boundaries before creating new structure.

Bootstrap SHALL map suitable existing mechanisms instead of duplicating them merely to match an example repository layout.

#### Scenario: Consumer already has a strategic-context repository

- GIVEN a person already maintains a suitable strategic-context repository
- WHEN OpenPD bootstrap maps strategic context
- THEN the existing repository MAY remain authoritative
- AND OpenPD SHALL NOT require copying all strategic context into the professional repository.

### Requirement: Profession-specific state remains outside OpenPD Core

OpenPD Core SHALL NOT require one universal profession ontology or capability model.

Profession-specific role models, capability taxonomies, radar structures and source collections SHALL remain local to consumers unless repeated evidence justifies extraction of a reusable profession pack.

#### Scenario: HR and Project Management capability models differ

- GIVEN HR Business Partner and Project Manager consumers need materially different capability models
- WHEN both use OpenPD Core
- THEN each capability model SHALL remain local or profession-specific
- AND the difference SHALL NOT by itself justify conditional profession logic in OpenPD Core.

### Requirement: Profession packs are extracted only after repeated reuse evidence

A reusable profession pack SHOULD be introduced only after multiple independent consumers demonstrate substantially the same profession-specific ontology, capability model, radar or source structure.

#### Scenario: Only one HR Business Partner consumer exists

- GIVEN a single HR Business Partner consumer has created a useful local capability structure
- WHEN OpenPD reviews whether to create an HRBP profession pack
- THEN the local structure MAY be treated as candidate evidence
- BUT SHALL NOT be promoted to a reusable profession pack solely from that one case.

### Requirement: Personal and confidential material is excluded from OpenPD

OpenPD SHALL NOT store identifiable personal career history, personal capability assessments, employer-confidential material or personal trajectory hypotheses as reusable methodology content.

Sanitized examples MAY be stored when they illustrate the method without turning local facts into universal rules.

#### Scenario: A consumer produces a useful private case

- GIVEN a personal repository contains a useful professional-development case with identifiable or confidential details
- WHEN the case is considered for OpenPD reuse
- THEN OpenPD SHALL keep the private details outside the methodology repository
- AND MAY accept only a sanitized, methodology-relevant abstraction after review.

### Requirement: Consumer bootstrap creates a usable decision loop, not ceremonial folders

Consumer bootstrap SHALL establish enough local authority that the person can recover professional state, active hypotheses, current primary bet, probes/experiments, evidence and inspection results according to the local binding.

#### Scenario: Repository folders exist but current state is unknown

- GIVEN a consumer repository contains template directories
- BUT a fresh reader cannot identify current professional state or active decision artifacts
- WHEN bootstrap is evaluated
- THEN bootstrap SHALL be considered structurally incomplete rather than validated merely because the directory layout exists.