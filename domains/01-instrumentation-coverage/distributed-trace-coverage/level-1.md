# Level 1

## Criteria

No distributed trace context propagation. Each service call is an isolated span. Engineers cannot follow a request across service boundaries during triage.

## Evidence Signals

### Signal 1

**Type:** `question`

Maybe possible to find services that have no other entities in their traces, indicating poor trace propagation


## Relevant Scorecard Rules

"(L0) Distributed Trace Coverage" - offers very basic check on ensureing entity itself is generating spans but doesnt adequately identify if the entity is part of a trace with >1 entity
Criticality scorecard could be useful here for identifying revnue impacting services

## Guidance to reach Level 2

_To be completed._
