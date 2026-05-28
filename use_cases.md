# Observability Maturity — Use Case Framework

This document describes the New Relic Foundational Use Case framework as it applies to the Observability Maturity Model (OMM). It maps each of the 54 rubric rules to the use case it primarily serves, providing a business-outcome lens on the technical scoring criteria.

The framework organises use cases into three groups. Every rubric rule is assigned a **primary** use case group and a specific use case within that group. This mapping appears in each rule's `_rule.md` file under `## Primary Use Case`.

---

## Use Case Groups

### Detect and Resolve

The ability to detect anomalies, failures, and regressions before they become customer-visible incidents, and to resolve them with minimum time and blast radius. Rules in this group measure the instrumentation, alerting, and incident response capabilities that determine how fast an organisation finds out something is wrong — and how fast it can fix it.

**26 rules** across Instrumentation Coverage, Alerting & Detection, Dashboards & Shared Insights, Incident Management, and OaC & Governance.

---

### Improve Quality

Ensuring that software systems are reliable, performant, and functionally correct from the user's perspective — and that quality is maintained or improved as systems evolve. Rules in this group measure the SLO discipline, digital experience monitoring, and organisational culture that translate technical reliability into sustained user trust.

**17 rules** across Service Level Management, Alerting & Detection, Digital Experience, Incident Management, and Business Alignment.

---

### Improve Efficiency

Reducing the operational overhead of running software systems — from infrastructure cost and deployment toil to developer cognitive load and engineering velocity. Rules in this group measure the platform engineering, observability governance, and developer experience practices that make engineering teams faster and less expensive to operate.

**11 rules** across Instrumentation Coverage, Platform Health & Infra SLM, OaC & Governance, and Developer Experience.

---

## Use Case Reference

### Detect and Resolve

#### Information Transparency & Supportability

The ability to explain what happened during any failure — from first alert to root cause. Requires complete telemetry, agreed operational views, and shared access to observability data across engineering roles. The absence of this use case means incidents are investigated by assembling context from scratch rather than opening a known, trusted view.

| Rule ID | Rule | Domain |
|---|---|---|
| IC-01 | APM Coverage Rate | Instrumentation Coverage |
| IC-09 | Service Inventory | Instrumentation Coverage |
| IC-10 | Team & Ownership Model | Instrumentation Coverage |
| IC-13 | Telemetry Coverage — Critical Path | Instrumentation Coverage |
| IC-14 | Instrumentation Standard | Instrumentation Coverage |
| DSI-03 | Dashboard Governance | Dashboards & Shared Insights |
| DSI-02 | Default Triage/Investigation Tools | Dashboards & Shared Insights |
| IM-07 | Workflow Automation | Incident Management |

---

#### Upstream & Downstream Dependencies

The ability to trace failures across service boundaries — synchronous and asynchronous — so that the originating cause of a cascading failure can be identified rather than just its symptoms. This use case is blocked at low maturity levels where trace context breaks at async boundaries and uninstrumented dependencies appear as unknown endpoints.

| Rule ID | Rule | Domain |
|---|---|---|
| IC-04 | Cloud Service Integration Coverage | Instrumentation Coverage |
| IC-07 | Distributed Trace Coverage | Instrumentation Coverage |
| IC-08 | Uninstrumented Dependencies | Instrumentation Coverage |
| IC-16 | Queue & Stream Visibility | Instrumentation Coverage |
| DSI-01 | Workload Count & Organisation | Dashboards & Shared Insights |
| IM-04 | Incident Response Process | Incident Management |
| IM-06 | MTTR Measurement | Incident Management |
| IM-08 | AI-Assisted Diagnostics (iRCA / SRE Agent) | Incident Management |

---

#### Configuration Drift & Environment Mismatch

The ability to detect and recover from unintended changes to system configuration, deployment environment, or observability artifacts that introduce failures not attributable to code changes. Tagging discipline is the foundation — without consistent entity tags, scoping and governance of alerts, dashboards, and scorecard rules breaks down.

| Rule ID | Rule | Domain |
|---|---|---|
| IC-05 | Team Tag Coverage | Instrumentation Coverage |
| IC-06 | Environment Tag Coverage | Instrumentation Coverage |
| IC-15 | Tagging Strategy & Governance | Instrumentation Coverage |
| IM-01 | Change Tracking Coverage | Incident Management |
| OAC-01 | Observability Silos & Fragmentation | OaC & Governance |
| OAC-02 | Observability Artifact Management | OaC & Governance |
| OAC-03 | Configuration Drift & Change Control | OaC & Governance |

---

#### Logic & Functional Regressions

The ability to detect when a code or configuration change has introduced incorrect behaviour — a function that previously worked correctly now produces wrong results, fails, or behaves differently under specific conditions. Alert quality is the primary lever: high noise ratios bury regression signals in fatigue.

| Rule ID | Rule | Domain |
|---|---|---|
| AD-02 | Critical Alert Rate | Alerting & Detection |
| AD-03 | Weekly Alert Volume | Alerting & Detection |
| IM-02 | Customer Impact Detection | Incident Management |
| IM-03 | On-Call Structure & Rotation | Incident Management |
| IM-05 | MTTD Measurement | Incident Management |

---

#### Scale-Induced Degradation

The ability to detect and diagnose performance failures that occur only under load — non-linear degradation, queue saturation, and resource exhaustion that static thresholds miss because they do not account for seasonality or baseline variance. Dynamic and anomaly-based alert conditions are the primary unlock.

| Rule ID | Rule | Domain |
|---|---|---|
| AD-04 | Alert Condition Quality | Alerting & Detection |

---

### Improve Quality

#### Perceived Performance & UX

Ensuring that the end-user experience meets performance standards that directly influence satisfaction, engagement, and conversion — measured by real user interactions under real-world conditions, not just server-side metrics. Core Web Vitals at the 75th percentile are the scoring anchors.

| Rule ID | Rule | Domain |
|---|---|---|
| IC-02 | Browser Coverage Rate | Instrumentation Coverage |
| IC-03 | Native Mobile Coverage Rate | Instrumentation Coverage |
| DE-01 | Browser / RUM Deployment | Digital Experience |
| DE-03 | Core Web Vitals Governance | Digital Experience |

---

#### Service Availability & Consistency

Ensuring that services meet defined reliability targets expressed as SLOs, and that degradation is detected and addressed before error budgets are exhausted. The progression from informal uptime checks through to burn-rate alerts and auto-calibrating SLOs is the core arc of this use case.

| Rule ID | Rule | Domain |
|---|---|---|
| SLM-01 | SLI Coverage Rate | Service Level Management |
| SLM-02 | SLO Existence & Enforcement | Service Level Management |
| SLM-03 | Error Budget Usage | Service Level Management |
| AD-01 | Alert Noise — Flappy Rate | Alerting & Detection |
| DE-02 | Synthetic Monitor Count | Digital Experience |
| BA-01 | Critical Business Journeys | Business Alignment |
| BA-04 | Business Future State Ambition | Business Alignment |

---

#### Release Integrity & Stability

Ensuring that new deployments maintain or improve service reliability — validated by observability signals before, during, and after each release. At its highest maturity, SLOs and error budgets are gate conditions in the deployment pipeline, not post-hoc health checks.

| Rule ID | Rule | Domain |
|---|---|---|
| SLM-04 | Error Budget Policy | Service Level Management |
| OAC-04 | New Service Onboarding | OaC & Governance |

---

#### Functional Correctness

Ensuring that software produces correct results — not just that it responds, but that responses are accurate, complete, and consistent with business rules. At L4, this use case requires SLIs tied directly to business outcome metrics (conversion rate, revenue, NPS) rather than only to technical signals.

| Rule ID | Rule | Domain |
|---|---|---|
| SLM-05 | SLI Data Quality & Types | Service Level Management |
| BA-02 | Business KPIs in Observability | Business Alignment |

---

#### Information Transparency & Supportability *(Quality dimension)*

The organisational dimension of observability quality — ensuring that teams have the culture, processes, and shared context to learn from failures and continuously improve. Blameless post-incident reviews with improvement actions tracked to closure are the primary expression of this use case in the Quality group.

| Rule ID | Rule | Domain |
|---|---|---|
| BA-03 | Post-Incident Review Process | Business Alignment |

---

### Improve Efficiency

#### Data Access & Persistence Efficiency

Optimising how applications interact with databases and data stores — reducing query latency, connection pool saturation, and unnecessary data access patterns. Requires independent DB-side telemetry beyond what APM trace spans surface, enabling DBA teams to operate autonomously within the observability platform.

| Rule ID | Rule | Domain |
|---|---|---|
| IC-11 | Database Instrumentation | Instrumentation Coverage |

---

#### Algorithmic & Code-Level Optimization

Identifying and resolving performance inefficiencies at the code level — N+1 queries, excessive API calls, AI token overuse, and algorithmic bottlenecks — using observability data surfaced at the point of development or via proactive inbox-style signals.

| Rule ID | Rule | Domain |
|---|---|---|
| IC-12 | AI / LLM Application Monitoring | Instrumentation Coverage |
| DX-03 | MCP Server & AI Developer Tooling | Developer Experience |

---

#### Infrastructure Right-Sizing & Elasticity

Ensuring that infrastructure resources are provisioned at the right scale — neither over-provisioned (wasted cost) nor under-provisioned (degraded performance) — and that capacity adapts to demand. Platform SLOs replace informal CPU/memory dashboard watching with formal commitments and governance.

| Rule ID | Rule | Domain |
|---|---|---|
| PH-01 | Platform Engineering Team | Platform Health & Infra SLM |
| PH-02 | Platform SLOs | Platform Health & Infra SLM |

---

#### Build & Deployment Pipeline Efficiency

Reducing the time, cost, and failure rate of the path from code commit to production. Measured by the DORA metric set: deployment frequency, lead time for changes, change failure rate, and failed deployment recovery time. Also includes the ingest governance and internal scorecard practices that make the observability platform itself efficient to operate.

| Rule ID | Rule | Domain |
|---|---|---|
| OAC-05 | Internal Scorecard / Engineering Health | OaC & Governance |
| OAC-06 | Pipeline Control / Ingest Governance | OaC & Governance |
| DX-01 | DORA Metrics Tracking | Developer Experience |

---

#### Communication & Architectural Paradigm Shifts

Using observability data and platform conventions to inform architectural decisions and reduce the cognitive load of building on shared platform infrastructure. The golden path concept — a paved, opinionated route for common developer tasks — is the primary expression of this use case.

| Rule ID | Rule | Domain |
|---|---|---|
| DX-02 | Golden Path Adoption | Developer Experience |

---

## Summary by Use Case Group

| Group | Use Case | Rule Count |
|---|---|---|
| Detect and Resolve | Information Transparency & Supportability | 8 |
| Detect and Resolve | Upstream & Downstream Dependencies | 8 |
| Detect and Resolve | Configuration Drift & Environment Mismatch | 7 |
| Detect and Resolve | Logic & Functional Regressions | 5 |
| Detect and Resolve | Scale-Induced Degradation | 1 |
| **Detect and Resolve total** | | **29** |
| Improve Quality | Service Availability & Consistency | 7 |
| Improve Quality | Perceived Performance & UX | 4 |
| Improve Quality | Functional Correctness | 2 |
| Improve Quality | Release Integrity & Stability | 2 |
| Improve Quality | Information Transparency & Supportability | 1 |
| **Improve Quality total** | | **16** |
| Improve Efficiency | Build & Deployment Pipeline Efficiency | 3 |
| Improve Efficiency | Infrastructure Right-Sizing & Elasticity | 2 |
| Improve Efficiency | Algorithmic & Code-Level Optimization | 2 |
| Improve Efficiency | Data Access & Persistence Efficiency | 1 |
| Improve Efficiency | Communication & Architectural Paradigm Shifts | 1 |
| **Improve Efficiency total** | | **9** |
| **Grand total** | | **54** |
