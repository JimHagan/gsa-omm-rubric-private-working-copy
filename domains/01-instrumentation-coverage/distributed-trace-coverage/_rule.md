# Distributed Trace Coverage

**Domain:** Instrumentation Coverage  
**Rule ID:** IC-07  
**Sheet Rule ID:** 7  

## Purpose

_To be completed._

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | No distributed trace context propagation. Each service call is an isolated span. Engineers cannot follow a request across service boundaries during triage. |
| 2 | Trace context propagated across synchronous calls between revenue-path services. Context breaks when a request hits an async boundary (Kafka, SQS, event stream) or crosses into a downstream service. |
| 3 | End-to-end trace context propagated across revenue-path services and the services they call, including async queue boundaries using W3C trace context headers. A complete distributed trace waterfall for the critical path is demonstrable during the session. |
| 4 | Trace context propagated across all application service layers. OTel semantic attributes (http.route, db.statement, rpc.method) present on critical spans. Near-complete coverage.  Trace sampling strategy designed and implemented. |
| 5 | Full trace context preserved across the entire estate. New services automatically validated for span emission on deployment. |
