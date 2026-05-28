# Observability Rubric

A structured rubric for assessing observability maturity across customer environments. Each rule is scored from Level 1 (initial / absent) to Level 5 (optimised / automated).

## Domains

| # | Domain | Rules | Description |
|---|--------|-------|-------------|
| 01 | [Instrumentation Coverage](domains/01-instrumentation-coverage/_domain.md) | 16 | Breadth and quality of telemetry collection |
| 02 | [Service Level Management](domains/02-service-level-management/_domain.md) | 5 | SLI/SLO coverage, error budgets, and data quality |
| 03 | [Alerting & Detection](domains/03-alerting-detection/_domain.md) | 4 | Alert noise, quality, and condition governance |
| 04 | [Digital Experience](domains/04-digital-experience/_domain.md) | 3 | Browser, synthetic, and Core Web Vitals |
| 05 | [Dashboards & Shared Insights](domains/05-dashboards-shared-insights/_domain.md) | 3 | Workloads, triage tooling, and dashboard governance |
| 06 | [Incident Management](domains/06-incident-management/_domain.md) | 8 | On-call, response process, MTTD/MTTR, and automation |
| 07 | [Business Alignment](domains/07-business-alignment/_domain.md) | 4 | Business journeys, KPIs, and post-incident reviews |
| 08 | [Platform Health & Infra SLM](domains/08-platform-health-infra-slm/_domain.md) | 2 | Platform engineering team and platform SLOs |
| 09 | [OaC & Governance](domains/09-oac-governance/_domain.md) | 6 | Observability-as-code, onboarding, and ingest control |
| 10 | [Developer Experience](domains/10-developer-experience/_domain.md) | 3 | DORA metrics, golden paths, and AI developer tooling |

**Total: 54 rules**

## Scoring Model

Each rule is independently scored 1–5:

| Level | Description |
|---|---|
| 1 | Absent or entirely manual |
| 2 | Exploratory / partial coverage |
| 3 | Consistent coverage of critical paths |
| 4 | Business-outcome aligned |
| 5 | Automated, programmatic, self-calibrating |

An overall domain score is the modal score across its rules — the level most commonly achieved. An overall rubric score is the modal score across all rules in the rubric.

## Contributing

See [STRUCTURE.md](STRUCTURE.md) for folder conventions, file templates, and authoring guidelines.
