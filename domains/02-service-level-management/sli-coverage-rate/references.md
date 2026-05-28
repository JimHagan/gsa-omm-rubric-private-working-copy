# References

## Site Reliability Engineering: How Google Runs Production Systems
**URL:** https://sre.google/sre-book/table-of-contents/
**Summary:** The canonical SRE reference from Google. Establishes the theoretical foundation for SLI/SLO/SLA frameworks, error budgets as a mechanism to balance reliability investment against feature velocity, and the four golden signals (latency, traffic, errors, saturation). Defines the principle that 100% reliability is the wrong target and that error budgets make risk explicit and negotiable.

## Service Level Management: Optimize SLM Guide
**URL:** https://docs.newrelic.com/docs/new-relic-solutions/observability-maturity/uptime-performance-reliability/optimize-slm-guide/
**Summary:** New Relic's foundational SLM guide. Defines the three SLI types — output performance (error-free rate), input performance (connectivity), and client performance (user experience) — along with service boundary definition methodology and error budget calculation. The primary reference for SLM domain scoring criteria and NR-specific implementation patterns.

## Get Started with New Relic Service Levels (SLI/SLO)
**URL:** https://docs.newrelic.com/docs/service-level-management/intro-slm/
**Summary:** New Relic's introductory SLM documentation. Covers the distinction between SLI definitions using NRDB transaction events (preferred for accuracy) versus metric rollup tables, and the tradeoffs of each approach. Authority for SLI data source quality criteria at L3.

## A Blueprint for Multi-Tiered Service Level Management
**URL:** https://newrelic.com/blog/observability/a-blueprint-for-multi-layer-service-level-management
**Summary:** A reference architecture for applying SLM across all five tiers of a modern stack: Layer 1 (Experience — Core Web Vitals and synthetic monitors), Layer 2 (Gatekeeper — CDN/load balancer edge health), Layer 3 (Service Domain — microservices using the RED Method with separate error rate and latency SLOs), Layer 4 (Foundation — infrastructure capacity and K8s health), and Layer 5 (Business Outcomes — conversion, revenue, engagement). Introduces the Observability Gap concept (infrastructure green, service degraded) and the Service Level Control Plane as the organizational governance model. Authored by Jim Hagan, Principal Solution Architect, New Relic.
