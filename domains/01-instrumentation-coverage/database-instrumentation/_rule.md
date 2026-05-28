# Database Instrumentation

**Domain:** Instrumentation Coverage  
**Rule ID:** IC-11  
**Sheet Rule ID:** 22  

## Purpose

_To be completed._

## Primary Use Case

**Use Case Group:** Improve Efficiency  
**Use Case:** Data Access & Persistence Efficiency

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | No DB instrumentation in NR. DBA uses a separate tool. |
| 2 | DB calls visible as APM trace spans; no independent DB-side telemetry. |
| 3 | Database OHI deployed for critical DBs; saturation and query metrics independent of APM. |
| 4 | DBA operates autonomously within NR; deep query analysis deployed. |
| 5 | N+1 patterns and excessive DB calls surfaced automatically via Performance Risks Inbox. |
