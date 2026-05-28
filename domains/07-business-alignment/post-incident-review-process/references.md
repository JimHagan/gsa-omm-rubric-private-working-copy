# References

## Postmortem Culture: Learning from Failure
**URL:** https://sre.google/sre-book/postmortem-culture/
**Summary:** Google SRE's chapter on blameless postmortem culture. Defines the principles of psychological safety in incident reviews, the 'do not celebrate heroism' guideline, and the structure of an effective postmortem document. Provides the theoretical foundation for blameless post-incident review scoring criteria.

## Observability Center of Excellence: Creating Your OCoE
**URL:** https://docs.newrelic.com/docs/new-relic-solutions/observability-maturity/operational-efficiency/observability-coe/
**Summary:** New Relic's guide to establishing an Observability Center of Excellence. Defines the three-tier OCoE model (core team, council, guild), operating cadences, and the champion network model for scaling observability culture across large organizations.

## A Blueprint for Enterprise Alert Management
**URL:** https://newrelic.com/blog/observability/a-blueprint-for-enterprise-alert-management
**Summary:** A reference architecture for enterprise alert management that maps the incident lifecycle through three domains: System of Knowledge (observability/detection), System of Action (notification and routing), and System of Record (incident management and audit history). Introduces the data gravity concept — the architectural advantage of keeping detection, routing, and record-keeping on a single data plane. Defines the human escalation ladder (L1 NOC → L2 responder → L3 engineer → Incident Commander) with explicit role ownership and two cultural failure modes to avoid: L3 bypass and IC role collapse. Authored by Jim Hagan, Principal Solution Architect, New Relic.
