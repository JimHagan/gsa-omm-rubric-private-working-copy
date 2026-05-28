# Level 1

## Criteria

No coherent APM coverage. User-facing services mostly uninstrumented. Monitoring is ad hoc or engineer-dependent.

## Evidence Signals

### Signal 1

**Type:** `question`

Need to understand which services should exist - requires external data from customer to properly evaluate


## Relevant Scorecard Rules

- "(L0) Uninstrumented Entities" scorecard offers some insight into some uninstrumented entities. But it only ocvers those seen by new relic and not isolated subsystems
- ": '(L2) APM Criticality Tag Cover" - this rule checks for tag presence, it could be used similary to identify revenue impacting services too when exploring dependent services.
- the state of "(L0) Distributed Trace Coverage" may also be useful here, a low score would suggest leve l3 might be unobtainable
A rule that scores the instrumentation level of dependent services to those tagged revenue impacting/critical would be useful

## Guidance to reach Level 2

_To be completed._
