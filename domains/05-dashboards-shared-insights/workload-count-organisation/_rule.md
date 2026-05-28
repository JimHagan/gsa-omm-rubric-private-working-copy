# Workload Count & Organisation

**Domain:** Dashboards & Shared Insights  
**Rule ID:** DSI-01  
**Sheet Rule ID:** 14  

## Purpose

_To be completed._

## Primary Use Case

**Use Case Group:** Detect and Resolve  
**Use Case:** Upstream & Downstream Dependencies

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | No NR Workloads configured. On-call engineers have no agreed shared health view to open when an alert fires. |
| 2 | A small number of Workloads exist, created ad hoc. No naming convention. Most teams do not have a Workload for their services. |
| 3 | Every service team has a named NR Workload used as the standard health view in ops meetings. On-call engineer can open the correct Workload within 30 seconds of an alert firing — without asking a colleague. |
| 4 | All service groups and environments covered. NR Service Architecture Intelligence (SAI) configured with ownership and dependency context. Used as first-stop in incident blast-radius identification. |
| 5 | Workloads programmatically provisioned via NerdGraph API or Terraform. New service teams automatically receive a Workload on onboarding. |
