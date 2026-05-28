# Observability Artifact Management

**Domain:** OaC & Governance  
**Rule ID:** OAC-02  
**Sheet Rule ID:** 47  

## Purpose

_To be completed._

## Primary Use Case

**Use Case Group:** Detect and Resolve  
**Use Case:** Configuration Drift & Environment Mismatch

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | All artifacts created via UI. No VCS. |
| 2 | Some artifacts in VCS; most still UI-managed. |
| 3 | All new artifacts created through VCS (Terraform or NR CLI); UI artifacts being migrated. |
| 4 | Full OaC CI/CD pipeline; all artifacts version-controlled; PR approval required. |
| 5 | Self-healing configurations; drift detected and auto-remediated; Pipeline Control active. |
