# Validation plan

## Research question

Under controlled evaluation, does a provenance-preserving, recursive-memory monitor identify inconsistent or degraded system records with useful lead time and traceable evidence, compared with ordinary alarms and conventional statistical baselines?

This is a hypothesis. The plan does not assume that EFMW improves detection or safety.

## System boundary

The monitor receives authorized, read-only copies of records. It produces evidence-linked findings for engineering review. It has no write path to operational systems and cannot recommend or execute traffic-control actions. The evaluation must verify that isolation technically holds, not merely rely on a written promise.

## Stages

### 0. Protocol and data governance

Before any run, define data ownership, permitted use, security controls, retention, access roles, de-identification where appropriate, and incident-response procedures. Publish a versioned protocol with frozen code, inputs, and scoring rules. An independent evaluator should control hidden cases and preserve an audit log.

### 1. Historical replay

Use authorized incident, recovery, and ordinary-operation records. Include clean periods and known degraded periods where ground truth can be independently established. Keep event labels and holdout periods from the development team. Compare the monitor with existing alarms, fixed thresholds, and conventional change-detection baselines such as EWMA and CUSUM where appropriate.

### 2. Simulation or hardware-in-the-loop

Exercise timestamp drift, message delay, loss, duplication, stale records, disagreement across independent channels, load spikes, failover transitions, and mixed legacy/new configurations. Include benign anomalies and correlated noise so that a monitor cannot pass by alerting on every change. Do not inject faults into operational air-traffic systems.

### 3. Optional shadow observation

Only after independent review of prior stages, the FAA may consider a limited, authorized shadow study using copied data. Confirm one-way isolation and cybersecurity controls before connection. The monitor remains advisory and disconnected from command pathways. Personnel retain all existing operational authority and procedures.

## Pre-registered measures

- **Detection:** sensitivity and miss rate by fault class, including confidence intervals.
- **Timeliness:** detection delay from independently established fault onset.
- **Nuisance burden:** false alerts per defined operating interval, severity distribution, and alert clustering.
- **Evidence traceability:** fraction of alerts with reproducible source records, timestamps, and triggering rule.
- **Uncertainty calibration:** whether `unresolved` or confidence labels reflect actual ambiguity; report calibration separately from detection.
- **Robustness:** performance across load, configuration, missingness, time drift, and data-quality conditions.
- **Isolation and security:** verified absence of operational write paths; documented access, tampering, spoofing, and dependency risks.
- **Human factors:** blinded reviewer usefulness, comprehension, and time-to-triage; no assumption that an alert improves decisions.

Report results per event class and dataset, not only as pooled averages. Separate seeded faults from naturally occurring events. A clean case that appears suspicious must be represented in the evaluation.

## Decision gates

1. **Stop before testing** if data authorization, threat model, independence, or scope is unresolved.
2. **Stop or redesign** if isolation fails, alerts cannot be traced to source evidence, false-alert burden is unacceptable to the designated reviewers, or performance does not add value over baselines under pre-agreed criteria.
3. **Advance to the next research stage only** after independent review confirms protocol compliance and results meet pre-registered criteria.
4. **No operational deployment conclusion** follows from replay, simulation, or shadow results alone. Any future operational use would require separate FAA safety assurance, cybersecurity review, procurement and governance decisions, and any required regulatory approvals.

## Reporting

Publish the protocol, versions, baseline definitions, exclusions, limitations, and aggregate results where permitted. Preserve negative and inconclusive findings. Distinguish observed evidence from interpretation; do not describe correlation as causation or a research monitor as an FAA-approved safety system.
