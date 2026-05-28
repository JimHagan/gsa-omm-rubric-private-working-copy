# References

## Site Reliability Engineering: How Google Runs Production Systems
**URL:** https://sre.google/sre-book/table-of-contents/
**Summary:** The canonical SRE reference from Google. Establishes the theoretical foundation for SLI/SLO/SLA frameworks, error budgets as a mechanism to balance reliability investment against feature velocity, and the four golden signals (latency, traffic, errors, saturation). Defines the principle that 100% reliability is the wrong target and that error budgets make risk explicit and negotiable.

## Postmortem Culture: Learning from Failure
**URL:** https://sre.google/sre-book/postmortem-culture/
**Summary:** Google SRE's chapter on blameless postmortem culture. Defines the principles of psychological safety in incident reviews, the 'do not celebrate heroism' guideline, and the structure of an effective postmortem document. Provides the theoretical foundation for blameless post-incident review scoring criteria.

## A Blueprint for Enterprise Alert Management
**URL:** https://newrelic.com/blog/observability/a-blueprint-for-enterprise-alert-management
**Summary:** A reference architecture for enterprise alert management that maps the incident lifecycle through three domains: System of Knowledge (observability/detection), System of Action (notification and routing), and System of Record (incident management and audit history). Introduces the data gravity concept — the architectural advantage of keeping detection, routing, and record-keeping on a single data plane. Defines the human escalation ladder (L1 NOC → L2 responder → L3 engineer → Incident Commander) with explicit role ownership and two cultural failure modes to avoid: L3 bypass and IC role collapse. Authored by Jim Hagan, Principal Solution Architect, New Relic.
