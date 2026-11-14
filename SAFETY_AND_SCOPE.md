# Safety and scope

## Intended use

Research whether an isolated monitor can help engineers inspect consistency across system records during controlled evaluation of modernization. The intended users are authorized engineering and safety reviewers, not air traffic controllers making live control decisions.

## Prohibited functions in this proposal

The prototype must not issue or change clearances, routes, separation instructions, departure permissions, ground stops, equipment commands, or alerts that directly control operational systems. It must not replace existing FAA procedures or be treated as an authoritative source of truth.

## Threat and failure considerations

The evaluation should examine corrupted or spoofed inputs, timestamp manipulation, replayed or duplicated messages, missing or delayed records, compromised credentials, malicious configuration changes, denial of service, alert flooding, and failures of the monitor itself. It should assess whether the monitor could create a new dependency, disclose sensitive data, or cause automation bias.

## Required safeguards before any data access

- Written authorization and a named data owner.
- Data minimization, access control, secure storage, retention limits, and an audit trail.
- A documented threat model and independent security review.
- Technical verification of read-only isolation and separation from command networks.
- Human review of findings with uncertainty and source evidence visible.
- Predefined stop conditions, rollback plan, and independent evaluation.

## Claims discipline

EFMW-ATC-Monitor is a research proposal, not a certified product. No efficacy, safety, or incident-causation claim is established by this repository. Any future claim must be tied to a reproducible protocol and independently reviewed evidence.
