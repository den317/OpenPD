# Proposal — Bootstrap OpenPD with AINEL and OpenSpec Current

## Problem

OpenPD has become a methodology product, but after Change 001 its accepted behavior is distributed across `README.md`, `docs/`, `methodology/` and templates. That is readable for a human, but it does not yet provide one explicit normative Current state or a disciplined delta lifecycle for future methodology evolution.

Without a dedicated Current authority, future failure modes are likely:

1. methodology semantics drift across several documents;
2. pull requests become the only place where a change can be reconstructed;
3. agents read old documents or archived decisions as if they were current;
4. a future OpenPD consumer cannot reliably determine which behavior is accepted now;
5. methodology changes are made directly in prose without an explicit reviewable delta.

AINEL already defines the required pattern for an existing OpenSpec-bound system: current specs are the accepted Source of Truth, active Changes are deltas, archive is provenance, and accepted deltas must reach Current before closure.

## Proposed change

Bootstrap OpenPD as an AINEL consumer and make OpenSpec the specification/change provider for OpenPD itself.

The resulting product-development model is:

```text
human intent / issue
        ↓
CURRENT: openspec/specs/
        ↓
CHANGE: openspec/changes/<change>/
        ↓
methodology/docs/templates artifact work
        ↓
validation
        ↓
sync accepted durable delta into CURRENT
        ↓
archive Change in the same PR
        ↓
human maintainer merge
        ↓
main = synchronized CURRENT + historical provenance
```

## Current baseline

OpenPD is an existing system, not greenfield. This Change therefore establishes a usable Current baseline from already accepted Change 001 behavior in three capabilities:

- `core-operating-model`;
- `consumer-binding`;
- `methodology-governance`.

The first two primarily formalize already accepted behavior. `methodology-governance` introduces the new durable behavior for developing OpenPD through AINEL/OpenSpec.

## AINEL binding

OpenPD will pin AINEL to commit:

`8fdce08bce17aadb40a176c6e59669832a78bd15`

AINEL remains external and subordinate to OpenPD local authority.

## Archive convention

Use `archive-inside-PR` while OpenPD remains an individually maintained lightweight methodology repository.

Rationale:

- merged `main` immediately contains synchronized Current;
- no post-merge window exists where a completed Change is merged but Current remains stale;
- the PR shows the intended post-merge state atomically;
- historical rationale remains inspectable without becoming Current authority.

Human maintainer merge is the final acceptance/authorization event.

## Scope

In scope:

- `ainel.yaml` ProjectBinding;
- OpenSpec configuration;
- Current baseline specs;
- OpenPD AINEL integration/precedence documentation;
- repository contract updates;
- explicit Change/archive/current-state semantics;
- historical Change 002 provenance and validation.

Out of scope:

- Beads/runtime task orchestration;
- automation or CI for OpenSpec;
- profession-specific packs;
- changing OpenPD's substantive professional-development loop beyond formalizing accepted v0.1 behavior;
- changing personal consumer repositories;
- automatically upgrading AINEL in the future.

## Expected effect

After acceptance, a fresh-context reader should be able to answer:

- What does OpenPD currently require?
- Which behavior is only proposed/in-flight?
- Where is historical rationale?
- How does a new material methodology change become Current?
- Which AINEL contract governs OpenPD engineering behavior?

without replaying repository history or guessing precedence.