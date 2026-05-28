# APM Coverage Rate

**Domain:** Instrumentation Coverage  
**Rule ID:** IC-01  
**Sheet Rule ID:** 1  

## Purpose

_To be completed._

## Primary Use Case

**Use Case Group:** Detect and Resolve  
**Use Case:** Information Transparency & Supportability

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | No coherent APM coverage. User-facing services mostly uninstrumented. Monitoring is ad hoc or engineer-dependent. |
| 2 | Core revenue-path services (checkout, login, payment) instrumented with APM agents. Services they call are visible only as spans within those traces — not independently monitored. |
| 3 | Revenue-path services and the downstream services they call are both fully covered with APM agents. Documented gap list with named owners and target dates for anything remaining. |
| 4 | All application services instrumented. Only explicitly documented exceptions remain, each with a stated rationale. |
| 5 | Fleet Control or Agent Control automatically deploys APM agents to new services on provision. No manual instrumentation steps required. |
