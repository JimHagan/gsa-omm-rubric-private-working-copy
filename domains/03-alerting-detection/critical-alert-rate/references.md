# References

## Alert Quality Management: Implementation Guide
**URL:** https://docs.newrelic.com/docs/new-relic-solutions/observability-maturity/uptime-performance-reliability/alert-quality-management-guide/
**Summary:** New Relic's primary AQM implementation guide. Defines the four KPIs — incident count, accumulated incident duration, mean time to close, and flappy rate (incidents closing in under 5 minutes). Provides the NRQL queries for NrAiIncident event data that calculate each metric and documents the AQM review cadence.

## Alert Quality Management — Manage Alert Quality
**URL:** https://docs.newrelic.com/docs/new-relic-solutions/observability-maturity/uptime-performance-reliability/alert-quality-management-guide/
**Summary:** New Relic's guide to the ongoing AQM improvement process. Covers the alert policy review cadence, identifying high-volume alert conditions, and the iterative tuning process for reducing noise while maintaining signal fidelity. Authority for the L3 scoring criterion requiring an active, sustained noise reduction program.

## Alert Quality Management — Hands-On Lab
**URL:** https://learn.newrelic.com/hands-on-lab-alert-quality-management
**Summary:** New Relic University hands-on lab for AQM process setup. Covers AQM dashboard deployment, baseline metric collection, and the iterative alert tuning workflow. The recommended practitioner enablement resource for teams working to reduce flappy rate.

## Elevate Your Alerts: Alert Quality Management Course
**URL:** https://learn.newrelic.com/elevate-your-alerts-alert-quality-management
**Summary:** New Relic University structured course on AQM dashboard setup, alert quality KPIs, and the iterative improvement process. The primary enablement resource for Alerting & Detection domain acceleration at L2→L3.

## A Blueprint for Enterprise Alert Management
**URL:** https://newrelic.com/blog/observability/a-blueprint-for-enterprise-alert-management
**Summary:** A reference architecture for enterprise alert management that maps the incident lifecycle through three domains: System of Knowledge (observability/detection), System of Action (notification and routing), and System of Record (incident management and audit history). Introduces the data gravity concept — the architectural advantage of keeping detection, routing, and record-keeping on a single data plane. Defines the human escalation ladder (L1 NOC → L2 responder → L3 engineer → Incident Commander) with explicit role ownership and two cultural failure modes to avoid: L3 bypass and IC role collapse. Authored by Jim Hagan, Principal Solution Architect, New Relic.
