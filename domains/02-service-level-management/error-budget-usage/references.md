# References

## Site Reliability Engineering: How Google Runs Production Systems
**URL:** https://sre.google/sre-book/table-of-contents/
**Summary:** The canonical SRE reference from Google. Establishes the theoretical foundation for SLI/SLO/SLA frameworks, error budgets as a mechanism to balance reliability investment against feature velocity, and the four golden signals (latency, traffic, errors, saturation). Defines the principle that 100% reliability is the wrong target and that error budgets make risk explicit and negotiable.

## The Site Reliability Workbook: Practical Ways to Implement SRE
**URL:** https://sre.google/workbook/table-of-contents/
**Summary:** The practical companion to the SRE Book. Appendix B provides a worked example of a written error budget policy including consequence definitions, freeze conditions, escalation paths, and governance model. Covers the implementing-SLOs process and cadence for error budget reviews.

## Implementing SLOs: A Step-by-Step Recipe
**URL:** https://sre.google/workbook/implementing-slos/
**Summary:** Google SRE's practical guide to defining and implementing SLOs. Recommends using a P95 performance baseline derived from observed production traffic as the starting point for SLO targets rather than arbitrary round numbers. Defines a four-week rolling window as the standard error budget calculation period.

## Service Level Management: Optimize SLM Guide
**URL:** https://docs.newrelic.com/docs/new-relic-solutions/observability-maturity/uptime-performance-reliability/optimize-slm-guide/
**Summary:** New Relic's foundational SLM guide. Defines the three SLI types — output performance (error-free rate), input performance (connectivity), and client performance (user experience) — along with service boundary definition methodology and error budget calculation. The primary reference for SLM domain scoring criteria and NR-specific implementation patterns.

## Alerting on Service Levels: Fast-Burn and Slow-Burn
**URL:** https://docs.newrelic.com/docs/service-level-management/alerts-slm/
**Summary:** New Relic's implementation guide for burn-rate based SLO alerts. Documents how to configure fast-burn (2% error budget in 1 hour) and slow-burn (5% in 6 hours) alert conditions within the NR platform using the multi-window, multi-burn-rate approach.

## A Blueprint for Multi-Tiered Service Level Management
**URL:** https://newrelic.com/blog/observability/a-blueprint-for-multi-layer-service-level-management
**Summary:** A reference architecture for applying SLM across all five tiers of a modern stack: Layer 1 (Experience — Core Web Vitals and synthetic monitors), Layer 2 (Gatekeeper — CDN/load balancer edge health), Layer 3 (Service Domain — microservices using the RED Method with separate error rate and latency SLOs), Layer 4 (Foundation — infrastructure capacity and K8s health), and Layer 5 (Business Outcomes — conversion, revenue, engagement). Introduces the Observability Gap concept (infrastructure green, service degraded) and the Service Level Control Plane as the organizational governance model. Authored by Jim Hagan, Principal Solution Architect, New Relic.
