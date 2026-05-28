# SLI Coverage Rate

**Domain:** Service Level Management  
**Rule ID:** SLM-01  
**Sheet Rule ID:** 9  

## Purpose

_To be completed._

## Primary Use Case

**Use Case Group:** Improve Quality  
**Use Case:** Service Availability & Consistency

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | No SLIs defined. Reliability measured by uptime ping or not at all. |
| 2 | A handful of exploratory SLIs defined for some revenue-path services. Not tied to business journeys and not reviewed in operational meetings. |
| 3 | SLIs defined for all revenue-path services and their primary dependencies. Targets derived from observed performance baselines — not arbitrary round numbers. Reviewed in engineering ops cadence. |
| 4 | SLI coverage extends across service and business outcome layers: output performance (error-free rate, latency), and at least one SLI tied directly to a business outcome metric (conversion rate, revenue, NPS). |
| 5 | All significant service boundaries have SLIs. SLOs programmatically managed via NerdGraph API or Terraform. SLI targets auto-calibrate following deployments. |
