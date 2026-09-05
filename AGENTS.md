# AGENTS.md — OpenPD repository contract

OpenPD is a **profession-agnostic methodology repository** for evidence-driven professional development. It is not a person's professional system of record and not the canonical repository for any one profession.

## 1. Preserve the methodology / personal-state boundary

OpenPD may contain reusable methods, contracts, templates, sanitized examples, and methodology evidence.

Do not add:

- identifiable personal career history;
- a person's current capability state, gaps, bets, or trajectory hypotheses;
- employer-confidential material;
- profession-specific conclusions presented as universal rules.

Personal professional state belongs in a consumer repository bound to OpenPD.

## 2. Evidence discipline

Preserve these distinctions:

- source != claim != evidence != inference;
- trend != personal relevance != gap != action;
- unknown != false;
- absence of evidence != weakness;
- current-scope evidence != future-scope proof;
- unproven-at-required-scope != demonstrated deficiency;
- experiment != capability proof;
- model inference != external evidence.

Do not convert a plausible interpretation into a durable fact without reviewable evidence.

## 3. WIP limits

Default OpenPD decision discipline:

- active direction hypotheses: maximum 3;
- primary development bets: 1;
- probes: use the minimum set of cheap evidence-producing probes that can realistically be executed now.

Prefer one probe that discriminates several hypotheses over several parallel initiatives.

## 4. Probe contract

Before a material probe define:

- H1/H2/H3 as applicable;
- key uncertainty;
- action;
- time / money / energy / organizational-commitment cap;
- expected evidence;
- strengthen / weaken criteria;
- inspection date or condition.

A failed probe is useful if it reduces uncertainty. A successful probe does not prove an entire long-term trajectory.

## 5. Inspection discipline

Start inspection from observed facts:

```text
done
→ observed result
→ metrics / evidence
→ surprises / constraints
→ preregistered criteria
→ update hypotheses / gaps
→ next bounded bet
```

For each hypothesis use one of: `STRENGTHEN`, `KEEP`, `WEAKEN`, `DROP`.

Distinguish capability problems from role-design, work-system, strategic, and sustainability constraints.

## 6. Consumer precedence

OpenPD is an external operating model.

A consumer repository keeps authority over its own:

- professional state;
- profession ontology and capability model;
- accepted evidence;
- local policies and privacy boundaries;
- strategic context;
- tooling and repository layout.

`openpd.yaml` records the binding. OpenPD should adapt to the consumer repository rather than silently replacing useful local mechanisms.

## 7. Methodology evolution

Do not change the core method after every disappointing answer.

Prefer changes at inspection/review boundaries using:

```text
recurrent defect
→ evidence
→ cause hypothesis
→ protocol change
→ expected effect
→ next validation cycles
```

Preserve prior versions. Do not silently rewrite historical methodology semantics.

A single profession or single person's experience may create a methodology hypothesis, but does not establish a universal rule.

## 8. Profession-specific packs

Do not create profession packs speculatively.

Extract a reusable profession-specific layer only after repeated evidence shows that multiple independent consumers need substantially the same profession ontology, capability model, radar, or source structure.

## 9. Privacy and safety

Keep examples sanitized. Do not add secrets, credentials, personal sensitive data, or identifiable employer-confidential cases.

## 10. Minimal-change principle

Keep OpenPD lightweight and inspectable. Prefer Markdown/YAML and explicit contracts over frameworks, databases, services, or automation without a demonstrated workflow need.

For repository changes, use a branch + pull request by default. Do not merge unless explicitly requested.
