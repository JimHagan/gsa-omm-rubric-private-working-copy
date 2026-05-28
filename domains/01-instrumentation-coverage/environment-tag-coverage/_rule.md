# Environment Tag Coverage

**Domain:** Instrumentation Coverage  
**Rule ID:** IC-06  
**Sheet Rule ID:** 6  

## Purpose

_To be completed._

## Primary Use Case

**Use Case Group:** Detect and Resolve  
**Use Case:** Configuration Drift & Environment Mismatch

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | No environment tag standard. Production traffic not reliably separated from staging in NR queries. Coverage below 30%. |
| 2 | Production tagged for most primary services. Non-production environments inconsistently tagged or absent. Coverage 30–69%. |
| 3 | Production reliably tagged across all application services. Enables NR Scorecard rules to be scoped to production only. Coverage 70–89%. |
| 4 | All environments tagged (prod, staging, dev, canary). NRQL queries and scorecard rules reliably filtered by environment. Coverage 90–98%. |
| 5 | Environment tag auto-applied at deploy time. New entities inherit the correct environment tag on provision. Coverage 99%+. |
