# OpenPD Methodology Evolution

OpenPD should evolve from repeated evidence, not from preference for abstraction or from one unsatisfying interaction.

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

## Cross-profession validation priority

The initial OpenPD program should prioritize learning from at least two materially different professions before extracting more framework layers.

The first HR Business Partner consumer is therefore not just an adopter; it is an evidence-producing probe of OpenPD's profession-agnostic boundary.
