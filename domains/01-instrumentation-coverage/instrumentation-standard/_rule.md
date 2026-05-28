# Instrumentation Standard

**Domain:** Instrumentation Coverage  
**Rule ID:** IC-14  
**Sheet Rule ID:** 27  

## Purpose

_To be completed._

## Primary Use Case

**Use Case Group:** Detect and Resolve  
**Use Case:** Information Transparency & Supportability

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | No instrumentation standard. Agent configuration, log format, attribute naming, and transaction naming decided independently by each team. |
| 2 | An instrumentation standard document exists. Compliance is voluntary — engineers are expected to follow it but there is no enforcement mechanism. |
| 3 | Instrumentation compliance is a required gate in the deployment pipeline for new services. Gate includes a defined checklist: agent deployed, required tags, at least one alert condition. Existing non-compliant services have a documented remediation backlog. |
| 4 | CI gate validates compliance on every deploy. NR Scorecards provide continuous monitoring of standard adherence between deploys — not just at deploy time. |
| 5 | NR Agent Control enforces instrumentation configuration declaratively. Drift auto-detected and auto-remediated. New service setup requires zero manual instrumentation decisions. |
