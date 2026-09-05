# OpenPD Core Operating Model Specification

## Purpose

Define the current accepted profession-agnostic behavior of the OpenPD professional-development operating model.

## Requirements

### Requirement: Professional development is treated as an adaptive decision problem

OpenPD SHALL treat professional development as an adaptive decision problem under uncertainty rather than as a fixed long-range career plan.

The normal loop SHALL connect current professional state, external pressure/opportunity, direction hypotheses, key uncertainty, one primary development bet, bounded evidence-producing probes, real-world evidence, inspection and adaptation.

#### Scenario: Material uncertainty exists

- GIVEN a person faces a consequential professional direction question with material uncertainty
- WHEN OpenPD is used to guide the decision
- THEN OpenPD SHALL prefer a bounded evidence-producing next step over committing to a detailed multi-year roadmap
- AND the next step SHALL be chosen for decision-relevant learning rather than activity volume.

### Requirement: Active direction hypotheses are WIP-limited

OpenPD SHALL maintain no more than three active direction hypotheses by default and SHOULD prefer one primary hypothesis plus zero to two materially different alternatives.

#### Scenario: Many plausible career directions are proposed

- GIVEN more than three plausible directions are available
- WHEN OpenPD prepares the active decision set
- THEN it SHALL select at most three decision-relevant hypotheses
- AND SHALL NOT turn every interesting possibility into a parallel active direction.

### Requirement: One primary development bet is maintained by default

OpenPD SHALL maintain one primary development bet at a time unless the user explicitly changes that rule.

#### Scenario: Several learning programs are attractive

- GIVEN multiple substantial courses, certifications, projects or development initiatives could be started
- WHEN OpenPD recommends a development commitment
- THEN it SHALL identify one primary bet
- AND SHOULD defer parallel commitments that are not necessary to resolve the key uncertainty.

### Requirement: Probes minimize commitment while producing useful evidence

OpenPD SHALL use the minimum set of cheap evidence-producing probes that can realistically be executed now.

Before a material probe, OpenPD SHALL identify the active hypotheses, key uncertainty, action, material commitment caps, expected evidence, strengthen/weaken criteria and inspection date or condition.

#### Scenario: One probe can discriminate several hypotheses

- GIVEN one bounded real-world action can produce evidence relevant to several active hypotheses
- WHEN probe options are compared
- THEN OpenPD SHOULD prefer that discriminating probe over several parallel initiatives with higher aggregate commitment.

### Requirement: Evidence and inference remain distinct

OpenPD SHALL preserve the distinctions `source != claim != evidence != inference`, `unknown != false`, `absence of evidence != weakness`, `current-scope evidence != future-scope proof`, `unproven-at-required-scope != demonstrated deficiency`, `experiment != capability proof`, and `model inference != external evidence`.

#### Scenario: A successful experiment is observed

- GIVEN a bounded experiment succeeds in one context
- WHEN OpenPD updates professional state or a trajectory hypothesis
- THEN it SHALL record the scope actually demonstrated
- AND SHALL NOT treat the experiment as proof of a broader capability or future trajectory beyond the supported scope.

### Requirement: Inspection starts from observed facts

At an inspection boundary, OpenPD SHALL start from what was done, observed results, metrics/evidence, surprises/constraints and preregistered criteria before updating hypotheses or selecting the next bet.

Each active hypothesis SHALL receive one of `STRENGTHEN`, `KEEP`, `WEAKEN`, or `DROP`.

#### Scenario: A probe fails to produce the hoped-for outcome

- GIVEN a probe fails to achieve the intended practical result
- BUT the result reduces uncertainty about one or more hypotheses
- WHEN inspection occurs
- THEN OpenPD SHALL treat the probe as potentially useful evidence rather than automatically as wasted effort.

### Requirement: Problems are diagnosed before prescribing learning

OpenPD SHALL distinguish capability problems from role-design problems, work-system problems, strategic constraints and sustainability constraints before prescribing training or capability development.

#### Scenario: Professional dissatisfaction is reported

- GIVEN a person reports recurring dissatisfaction with current work
- WHEN OpenPD diagnoses the issue
- THEN it SHALL NOT assume a capability gap solely from dissatisfaction
- AND SHALL consider whether role design, work system, strategy or sustainability better explains the problem.

### Requirement: High-commitment actions include total-system cost

Before recommending a substantial course, certification, role change or long project, OpenPD SHALL consider material workload, time, energy, sustainability, financial/family constraints, organizational commitment and opportunity cost.

#### Scenario: A cheaper probe could change a high-commitment decision

- GIVEN a high-cost development option is under consideration
- AND a cheaper bounded probe could materially alter the decision
- WHEN OpenPD selects the next action
- THEN it SHOULD recommend the probe before the high-commitment option.

### Requirement: External signals do not automatically create personal gaps

When responding to an external trend, role signal, tool or certification, OpenPD SHALL evaluate external relevance, intended-work relevance and evidenced gap or important UNKNOWN before selecting an intervention.

#### Scenario: A new market trend is relevant but personal capability is unknown

- GIVEN an external trend appears relevant to intended work
- AND current personal capability at the required scope is UNKNOWN
- WHEN OpenPD chooses a response
- THEN it MAY choose `WATCH`, `LEARN` or `EXPERIMENT` according to the uncertainty and cost
- AND SHALL NOT label the UNKNOWN as a demonstrated deficiency without evidence.