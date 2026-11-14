# Keeping the Airspace Coherent
## A bounded EFMW proposal for FAA modernization

**Draft addressed to Secretary Sean P. Duffy**  
**Matthew Chenoweth Wright, Monolithic LLC**  
**November 14, 2026**

Secretary Duffy,

The nationwide ground stop on November 13 showed both the value of trained people and established safety procedures, and the risk carried by an air traffic system whose communications and radar data can become inconsistent under load. Your briefing described instability across centers and TRACONs, with legacy telecommunications equipment and routers overloaded as new systems were being integrated. The FAA halted departures, aircraft already airborne landed safely, and departures resumed after the agency tested system stability.

Modernization is necessary. The question is how to make the transition itself observable, testable, and reversible. I propose that the FAA consider a tightly bounded, independent **EFMW-inspired coherence-monitoring pilot** alongside its modernization work.

EFMW—Entangled Field Memory Waveform—is a research program developed by Monolithic LLC. It is not an FAA-approved system, has not been validated for aviation safety, and should not be placed in the live control path. The proposal is narrower: test whether a separate monitor can help engineers detect and explain contradictions among time-stamped communications, radar, flight-data, and system-health records while new infrastructure is being integrated.

### What the monitor would do

The monitor would read authorized copies of existing telemetry and logs. It would preserve source identity, timestamps, sequence, and uncertainty, then compare each incoming record with both its recent history and independent records that should agree with it. It would flag patterns such as:

- data that arrives late, is duplicated, or disappears;
- disagreement between independent radar, communications, and flight-data records;
- a sudden change in error patterns as load or a software configuration changes;
- a failover that appears successful in one component while a dependent component remains stale or inconsistent.

The EFMW contribution would be recursive memory with provenance: the monitor retains a bounded record of what each channel reported, how reliable that channel has been, and where the current evidence conflicts with the record. It should make uncertainty more visible, not smooth it away. Every alert should point to the underlying records and the rule that triggered it.

This monitor would not issue clearances, select aircraft routes, replace controller judgment, or tell the FAA to keep the airspace open. It would be isolated from operational command systems. Its outputs would be advisory findings for engineers and safety staff, with clear states such as **consistent**, **degraded**, and **unresolved**. Existing FAA procedures would remain responsible for operational decisions.

### How to test it

The pilot should proceed in stages, with acceptance criteria agreed before any results are examined.

First, replay historical incident and recovery records, where available, alongside ordinary traffic periods. Compare the EFMW monitor with existing alarms and conventional statistical baselines, including simple thresholds and change-detection methods. The question is not whether EFMW can produce an alert; it is whether it adds useful, traceable information.

Second, use a hardware-in-the-loop or faithful simulation environment to test intermittent communications, radar-data gaps, timestamp drift, stale or duplicated messages, load spikes, failover behavior, and mixed old/new configurations. Include benign disruptions that should not trigger an emergency response. An independent evaluator should hold the fault schedule and score the system against pre-registered measures: missed critical inconsistencies, detection delay, nuisance alerts, traceability, and recovery behavior.

Third, if the earlier stages justify it, run the monitor in shadow mode on a carefully selected operational segment. It would observe copied data only; it would have no route to alter live instructions or equipment. FAA safety engineers and controllers would review its findings. A separate security review should assess data access, tampering, spoofed inputs, and whether the monitor itself creates a new dependency or attack surface.

A result that does not beat the baseline, cannot explain its alerts, or creates excessive false alarms should stop the pilot or send it back for redesign. A result that looks promising should still require independent replication and FAA safety approval before any operational use.

### Why this belongs beside modernization

The Government Accountability Office has described widespread sustainability concerns across FAA’s legacy systems and has called for stronger cost and schedule planning for the modernization program. A separate GAO review identified aviation communications risks involving spoofing, jamming, and weaknesses in authentication and data protection. Those findings do not establish that either issue caused the November 13 outage. They do show why modernization needs clear evidence that components work together, preserve trusted records, and fail in understood ways.

An EFMW monitor cannot repair aging copper, replace overloaded switches, or supply missing redundancy. Funding and completing the modernization remain the primary remedies. A bounded observer could help answer a different question: during a complex, rapid transition, can the FAA see early enough when the system’s records stop agreeing—and can it trace that warning to the component and configuration that produced it?

My request is modest: designate a technical point of contact to review this proposal and identify a non-operational dataset or simulation environment suitable for an initial comparison. Monolithic would provide a written pilot protocol, threat model, output schema, and independent-evaluation plan for review before any test begins. No access to live control systems is needed for that first review.

The objective is not to add another unproven layer to air traffic control. It is to test, under strict isolation, whether recursive memory and provenance checks can make modernization safer to evaluate. If the evidence says no, the pilot should end. If the evidence says yes, the FAA would have a concrete, independently reviewable result to consider.

Respectfully,

**Matthew Chenoweth Wright**  
Founder, Monolithic LLC

### Sources

- [U.S. Department of Transportation: Duffy’s November 13 update on the nationwide ground stop](https://www.transportation.gov/briefing-room/icymi-us-transportation-secretary-sean-p-duffy-announces-lifting-nationwide-ground)
- [FAA: Statement on the nationwide ground stop](https://www.faa.gov/newsroom/faa-statement-nationwide-ground-stop)
- [GAO-26-107992: Air Traffic Control Systems—Modernization planning](https://files.gao.gov/reports/GAO-26-107992/index.html)
- [GAO-26-108439: Aviation Cybersecurity—Threats to aircraft communications](https://www.gao.gov/products/gao-26-108439)
