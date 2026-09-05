# OpenPD Methodology Evolution

OpenPD should evolve from repeated evidence, not from preference for abstraction or from one unsatisfying interaction.

## Current authority and change carrier

OpenPD is developed through AINEL with OpenSpec as the specification/change provider.

Use:

```text
CURRENT
openspec/specs/

CHANGE
openspec/changes/<change>/

HISTORY
openspec/changes/archive/<dated-change>/
```

`openspec/specs/` is the normative Current accepted methodology behavior. A material durable methodology change must be expressed as an OpenSpec Change and, when accepted, synchronized into Current before or as part of archive completion.

OpenPD currently uses archive-inside-PR: the PR carries synchronized intended post-merge Current plus archived Change provenance; human maintainer merge is the final acceptance event.

Versioned files under `methodology/` preserve explanatory/release semantics and historical versions. They do not replace Current as the normative present-state authority.

See [`ainel-integration.md`](ainel-integration.md).

## Change trigger

Prefer methodology changes at explicit inspection/review boundaries.

Use:

```text
recurrent defect
→ evidence
→ cause hypothesis
→ protocol change
→ expected effect
→ validation in subsequent cycles
```

A single observation may be recorded as a candidate issue. It does not automatically justify changing the core.

Explicit human product intent may still deliberately introduce a change; the evidence threshold governs the strength of the methodology claim, not whether the human owner is allowed to change the product contract.

## Evidence threshold

A core-method change becomes stronger when one or more of these are true:

- the same defect recurs across several cycles;
- the defect appears across materially different professions;
- the current rule causes predictable decision-quality or usability harm;
- a simpler rule preserves the intended evidence discipline with lower cost;
- several independent consumers require the same missing concept.

A change becomes weaker when it only makes one profession's local model easier to express.

## Preserve history

Methodology files are versioned artifacts.

Do not silently rewrite old versions after they have been used for consequential decisions. Create a new version or an explicit superseding record when semantics materially change.

OpenSpec Current is intentionally different from versioned methodology history:

- Current answers **what OpenPD requires now**;
- versioned methodology artifacts answer **what a named methodology version described**;
- archived Changes answer **why/how Current evolved**.

Consumer repositories should pin the OpenPD version/commit used for a decision cycle when reproducibility matters.

## Profession-specific extraction

Do not move a profession-specific concept into OpenPD Core merely because it is useful.

Use this decision:

```text
useful for one person
→ keep personal/local

reused by several people in one profession
→ candidate profession pack

reused across materially different professions
→ candidate OpenPD Core concept
```

Profession packs are optional future architecture, not a v0.1 requirement.

## Review questions

At a methodology inspection ask:

1. What actually failed or created unnecessary cost?
2. Is the defect in OpenPD Core, the consumer binding, profession-specific modeling, or execution discipline?
3. What evidence supports that diagnosis?
4. What is the smallest protocol change that could fix it?
5. What behavior should improve if the change is correct?
6. In which next cycles will that effect be inspected?
7. Which Current OpenSpec capability is affected?
8. Has the accepted delta been synchronized into Current before closure?

## Cross-profession validation priority

The initial OpenPD program should prioritize learning from at least two materially different professions before extracting more framework layers.

The first HR Business Partner consumer is therefore not just an adopter; it is an evidence-producing probe of OpenPD's profession-agnostic boundary.
