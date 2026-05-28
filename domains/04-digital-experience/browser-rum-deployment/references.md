# References

## Core Web Vitals — LCP, INP, CLS Technical Reference
**URL:** https://web.dev/vitals/
**Summary:** Google's authoritative definition of Core Web Vitals and their 'Good' thresholds at the 75th percentile: LCP <2.5s (load performance), INP <200ms (responsiveness), CLS <0.1 (visual stability). INP replaced First Input Delay as the interactivity metric in March 2024. These p75 thresholds are the direct scoring anchors for Digital Experience domain criteria.

## Introduction to Digital Experience with New Relic
**URL:** https://docs.newrelic.com/docs/new-relic-solutions/observability-maturity/digital-experience/introduction/
**Summary:** New Relic's Digital Experience maturity framework. Defines the three-stage progression (Reactive → Proactive → Mastery) for digital experience monitoring, covering Browser error tracking at L1, CWV performance optimization at L2/L3, and business outcome correlation at L4.

## PageViewTiming: LCP, INP, CLS Technical Reference
**URL:** https://docs.newrelic.com/docs/browser/new-relic-browser/page-load-timing-resources/pageviewtiming-async-or-dynamic-page-details/
**Summary:** Technical reference for the NR PageViewTiming event type, which captures Core Web Vitals for asynchronous and dynamic page loads. Documents the specific NRQL query patterns for calculating p75 LCP, INP, and CLS from raw browser agent data.

## Introduction to Digital Experience Monitoring
**URL:** https://docs.newrelic.com/docs/new-relic-solutions/observability-maturity/digital-experience/introduction/
**Summary:** New Relic's Digital Experience Monitoring introduction. Maps the Reactive → Proactive → Mastery progression: Browser error tracking (L1), CWV performance optimization with targets (L2/L3), and business outcome correlation with experience SLOs (L4).

## A Blueprint for Multi-Tiered Service Level Management
**URL:** https://newrelic.com/blog/observability/a-blueprint-for-multi-layer-service-level-management
**Summary:** A reference architecture for applying SLM across all five tiers of a modern stack: Layer 1 (Experience — Core Web Vitals and synthetic monitors), Layer 2 (Gatekeeper — CDN/load balancer edge health), Layer 3 (Service Domain — microservices using the RED Method with separate error rate and latency SLOs), Layer 4 (Foundation — infrastructure capacity and K8s health), and Layer 5 (Business Outcomes — conversion, revenue, engagement). Introduces the Observability Gap concept (infrastructure green, service degraded) and the Service Level Control Plane as the organizational governance model. Authored by Jim Hagan, Principal Solution Architect, New Relic.
