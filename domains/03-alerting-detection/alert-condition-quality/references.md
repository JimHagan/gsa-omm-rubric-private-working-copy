# References

## Site Reliability Engineering: How Google Runs Production Systems
**URL:** https://sre.google/sre-book/table-of-contents/
**Summary:** The canonical SRE reference from Google. Establishes the theoretical foundation for SLI/SLO/SLA frameworks, error budgets as a mechanism to balance reliability investment against feature velocity, and the four golden signals (latency, traffic, errors, saturation). Defines the principle that 100% reliability is the wrong target and that error budgets make risk explicit and negotiable.

## Alerting on SLOs: Fast-Burn and Slow-Burn Rates
**URL:** https://sre.google/workbook/alerting-on-slos/
**Summary:** Google SRE's definitive guide to burn-rate based SLO alerting. Defines the fast-burn threshold (2% error budget consumed in one hour) and slow-burn threshold (5% in six hours) that provide both detection speed and resistance to false positives. These specific thresholds are the L4 scoring anchors for burn-rate alert deployment.

## Alert Quality Management: Implementation Guide
**URL:** https://docs.newrelic.com/docs/new-relic-solutions/observability-maturity/uptime-performance-reliability/alert-quality-management-guide/
**Summary:** New Relic's primary AQM implementation guide. Defines the four KPIs — incident count, accumulated incident duration, mean time to close, and flappy rate (incidents closing in under 5 minutes). Provides the NRQL queries for NrAiIncident event data that calculate each metric and documents the AQM review cadence.

## Alert Quality Management — Manage Alert Quality
**URL:** https://docs.newrelic.com/docs/new-relic-solutions/observability-maturity/uptime-performance-reliability/alert-quality-management-guide/
**Summary:** New Relic's guide to the ongoing AQM improvement process. Covers the alert policy review cadence, identifying high-volume alert conditions, and the iterative tuning process for reducing noise while maintaining signal fidelity. Authority for the L3 scoring criterion requiring an active, sustained noise reduction program.

## Alerting on Service Levels: Fast-Burn and Slow-Burn
**URL:** https://docs.newrelic.com/docs/service-level-management/alerts-slm/
**Summary:** New Relic's implementation guide for burn-rate based SLO alerts. Documents how to configure fast-burn (2% error budget in 1 hour) and slow-burn (5% in 6 hours) alert conditions within the NR platform using the multi-window, multi-burn-rate approach.

## A Blueprint for Enterprise Alert Management
**URL:** https://newrelic.com/blog/observability/a-blueprint-for-enterprise-alert-management
**Summary:** A reference architecture for enterprise alert management that maps the incident lifecycle through three domains: System of Knowledge (observability/detection), System of Action (notification and routing), and System of Record (incident management and audit history). Introduces the data gravity concept — the architectural advantage of keeping detection, routing, and record-keeping on a single data plane. Defines the human escalation ladder (L1 NOC → L2 responder → L3 engineer → Incident Commander) with explicit role ownership and two cultural failure modes to avoid: L3 bypass and IC role collapse. Authored by Jim Hagan, Principal Solution Architect, New Relic.
