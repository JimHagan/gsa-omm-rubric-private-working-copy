# Change Tracking Coverage

**Domain:** Incident Management  
**Rule ID:** IM-01  
**Sheet Rule ID:** 15  

## Purpose

_To be completed._

## Primary Use Case

**Use Case Group:** Detect and Resolve  
**Use Case:** Configuration Drift & Environment Mismatch

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | Deployments invisible in NR. Engineers must manually check CI/CD logs or ask the deploying team during incident triage. |
| 2 | NR Change Tracking configured for revenue-path services via NerdGraph API or CI/CD plugin. Not yet part of the standard deployment process — some services still missing. |
| 3 | NR Change Tracking integrated into the CI/CD pipeline for revenue-path services and their primary dependencies as a standard step. Deployment markers visible as timeline events in APM, dashboards, and SLM views. |
| 4 | All application services tracked. Infrastructure changes (K8s rollouts, config changes) also captured. Change markers used as the first diagnostic step in every incident triage workflow. |
| 5 | All change types tracked: deployments, infrastructure changes, feature flag toggles (e.g., LaunchDarkly), and database schema migrations. Rollback events captured. |
