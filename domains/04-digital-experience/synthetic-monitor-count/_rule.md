# Synthetic Monitor Count

**Domain:** Digital Experience  
**Rule ID:** DE-02  
**Sheet Rule ID:** 13  

## Purpose

_To be completed._

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | No synthetic monitors. Service availability and user journey health discovered reactively. |
| 2 | Ping/availability monitors exist for primary service URLs. Monitors confirm a URL responds — not mapped to specific user journeys. Single-location execution. |
| 3 | Scripted browser monitors covering all critical user journeys (checkout, login, account creation). Multi-location execution from at least 3 locations. Monitor names correspond to journey names. |
| 4 | All critical user journeys and primary API contracts covered. SLOs defined on synthetic success rate. Monitors included in pre-release validation. |
| 5 | Journey SLOs with error budgets govern deployment gates. Synthetic monitor provisioning automated — new journey additions trigger monitor creation. |
