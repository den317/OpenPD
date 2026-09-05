# Project Manager — OpenPD consumer example

This example shows how a mature Project Management professional-development repository can consume OpenPD without turning OpenPD into a PM-specific framework.

## Keep PM-specific material local

A PM consumer may keep locally:

- PM ontology and capability models;
- PM-specific external radar and source corpus;
- personal evidence, gaps, hypotheses, bets, and experiments;
- publication or educational workflows specific to that repository;
- wider strategic context and sustainability constraints.

These are consumer concerns, not OpenPD Core concerns.

## Bind rather than migrate wholesale

An existing mature repository should introduce `openpd.yaml` that maps its current locations to OpenPD concepts:

```text
professional state
hypotheses
primary development bet
experiments / probes
evidence
inspections
profession ontology
strategic context
```

Do not reorganize a mature repository merely to resemble the bootstrap example.

## Methodology extraction rule

If a rule originated in PM practice, ask:

1. Is it useful only for this person? Keep it local.
2. Is it reusable across several PMs? Consider a future PM profession pack.
3. Is it reusable across materially different professions? Consider OpenPD Core.

The burden of proof is on promotion toward the more universal layer.
