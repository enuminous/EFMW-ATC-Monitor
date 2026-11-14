# Repository index

A guide to the EFMW-ATC-Monitor proposal, its scope, and its evaluation plan.

**Project stage:** proposal-stage research concept. The repository currently contains documentation; implementation, datasets, tests, and experimental results are not yet included.

## Document map

| Document | Purpose |
|---|---|
| [README.md](README.md) | Project overview, research question, safety boundary, and proposed first step. |
| [PROPOSAL_FOR_SECRETARY_DUFFY.md](PROPOSAL_FOR_SECRETARY_DUFFY.md) | Draft proposal addressed to Secretary Sean P. Duffy: intended monitor behavior, staged evaluation, modernization context, and cited sources. |
| [SAFETY_AND_SCOPE.md](SAFETY_AND_SCOPE.md) | Intended users, prohibited functions, threat and failure considerations, safeguards, and limits on claims. |
| [VALIDATION_PLAN.md](VALIDATION_PLAN.md) | Research question, evaluation stages, conventional baselines, measures, decision gates, and reporting requirements. |
| [INDEX.md](INDEX.md) | This repository guide and topic index. |

## Suggested reading paths

| Reader or task | Reading order |
|---|---|
| First visit | [Overview](README.md) → [Proposal](PROPOSAL_FOR_SECRETARY_DUFFY.md) → [Validation plan](VALIDATION_PLAN.md) |
| Policy or program review | [Proposal](PROPOSAL_FOR_SECRETARY_DUFFY.md) → [Safety and scope](SAFETY_AND_SCOPE.md) → [Decision gates](VALIDATION_PLAN.md#decision-gates) |
| Technical evaluation | [System boundary](VALIDATION_PLAN.md#system-boundary) → [Evaluation stages](VALIDATION_PLAN.md#stages) → [Measures](VALIDATION_PLAN.md#pre-registered-measures) → [Reporting](VALIDATION_PLAN.md#reporting) |
| Safety and security review | [Threats and failures](SAFETY_AND_SCOPE.md#threat-and-failure-considerations) → [Required safeguards](SAFETY_AND_SCOPE.md#required-safeguards-before-any-data-access) → [Decision gates](VALIDATION_PLAN.md#decision-gates) |

## Topic index

| Topic | Where to read |
|---|---|
| Research question and hypothesis | [Validation plan — Research question](VALIDATION_PLAN.md#research-question) |
| Proposed monitor inputs, findings, and evidence traceability | [Proposal — What the monitor would do](PROPOSAL_FOR_SECRETARY_DUFFY.md#what-the-monitor-would-do) |
| Intended engineering users | [Safety and scope — Intended use](SAFETY_AND_SCOPE.md#intended-use) |
| Read-only isolation and operational boundaries | [Validation plan — System boundary](VALIDATION_PLAN.md#system-boundary); [Safety and scope — Prohibited functions](SAFETY_AND_SCOPE.md#prohibited-functions-in-this-proposal) |
| Authorization, data ownership, and protocol freeze | [Stage 0 — Protocol and data governance](VALIDATION_PLAN.md#0-protocol-and-data-governance) |
| Historical replay and ordinary baselines, including EWMA and CUSUM | [Stage 1 — Historical replay](VALIDATION_PLAN.md#1-historical-replay) |
| Simulation, fault cases, and benign controls | [Stage 2 — Simulation or hardware-in-the-loop](VALIDATION_PLAN.md#2-simulation-or-hardware-in-the-loop) |
| Conditions for optional shadow observation | [Stage 3 — Optional shadow observation](VALIDATION_PLAN.md#3-optional-shadow-observation) |
| Detection, delay, nuisance alerts, calibration, and reviewer usefulness | [Validation plan — Pre-registered measures](VALIDATION_PLAN.md#pre-registered-measures) |
| Spoofing, tampering, missing records, and monitor failures | [Safety and scope — Threat and failure considerations](SAFETY_AND_SCOPE.md#threat-and-failure-considerations) |
| Stop, redesign, and advancement conditions | [Validation plan — Decision gates](VALIDATION_PLAN.md#decision-gates) |
| Negative results, limitations, and publication | [Validation plan — Reporting](VALIDATION_PLAN.md#reporting) |
| Evidence limits and claims discipline | [Safety and scope — Claims discipline](SAFETY_AND_SCOPE.md#claims-discipline); [README — What this repository does not claim](README.md#what-this-repository-does-not-claim) |
| Modernization context and external references cited by the proposal | [Proposal — Why this belongs beside modernization](PROPOSAL_FOR_SECRETARY_DUFFY.md#why-this-belongs-beside-modernization); [Sources](PROPOSAL_FOR_SECRETARY_DUFFY.md#sources) |
| Proposed next step | [README — Proposed first step](README.md#proposed-first-step) |

## Inventory and maintenance

The source scan covered every tracked file at [commit `e9f1557`](https://github.com/enuminous/EFMW-ATC-Monitor/tree/e9f155783d237f08813ed9505cd3b33a77e4cac6) on November 14, 2026: four Markdown documents at the repository root. This index is the fifth document.

Update the document map and topic links when files or headings change. Add future code, data schemas, reproducibility instructions, and result records only when they are actually present, preserving the distinction between proposed work and demonstrated results.
