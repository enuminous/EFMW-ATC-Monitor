# EFMW-ATC-Monitor

**Status: proposal-stage research concept. No operational software or validated safety capability is included.**

EFMW-ATC-Monitor is a proposed, independently evaluated observer for air-traffic-system modernization. Its research question is whether recursive memory and provenance checks can help engineers detect and explain inconsistencies among authorized copies of communications, surveillance, flight-data, and system-health records.

## Safety boundary

- Read-only access to approved copied telemetry and logs.
- No connection to operational command paths; no ability to issue, alter, or suppress clearances, routing, equipment states, or ground-stop decisions.
- No replacement for controllers, FAA procedures, existing safety systems, cybersecurity controls, or modernization investment.
- Outputs would be evidence-linked engineering findings, with uncertainty preserved and states such as `consistent`, `degraded`, or `unresolved`.
- Any operational shadow study would require FAA authorization, security and privacy review, independent evaluation, and a stop rule.

## Repository contents

- `PROPOSAL_FOR_SECRETARY_DUFFY.md` — the accompanying bounded pilot proposal.
- `VALIDATION_PLAN.md` — staged comparisons, measures, and decision gates.
- `SAFETY_AND_SCOPE.md` — system boundary, misuse risks, and governance requirements.

## What this repository does not claim

This repository does not establish that EFMW is validated for aviation, that it detects faults better than existing methods, or that it would have prevented or diagnosed any specific outage. No causal claim about the November 13 event is made here. The proposal is to test a research hypothesis against conventional baselines under controlled conditions.

## Proposed first step

Review the protocol with an FAA technical contact and identify a non-operational historical dataset or simulation environment. Freeze the data, baselines, scoring rules, and stop criteria before running comparisons.
