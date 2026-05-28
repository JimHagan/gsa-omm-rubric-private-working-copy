# Telemetry Coverage — Critical Path

**Domain:** Instrumentation Coverage  
**Rule ID:** IC-13  
**Sheet Rule ID:** 26  

## Purpose

_To be completed._

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | Cannot demonstrate end-to-end telemetry for any critical business path. Coverage is ad hoc — telemetry depends on which engineer last worked on a service. |
| 2 | Revenue-path services have metrics and logs. Trace context breaks at async boundaries. Infrastructure layer not correlated with the application layer. |
| 3 | Complete MELT coverage (metrics, events, logs, traces) for revenue-path services and the services they call. OTel semantic attributes present. Async boundaries no longer diagnostic dead ends. A complete distributed trace waterfall for the critical path is demonstrable during the session. |
| 4 | Critical path telemetry correlated across all service layers — a single NR Workload or dashboard provides the full picture. Business outcome metrics (order volume, conversion rate) tracked alongside service metrics. |
| 5 | Agent Control or Fleet Control auto-instruments new services joining the critical path. Anomaly detection active on critical path signals — degradation surfaces before threshold breach. |
