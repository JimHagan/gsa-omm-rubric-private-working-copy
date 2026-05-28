# References

## Site Reliability Engineering: How Google Runs Production Systems
**URL:** https://sre.google/sre-book/table-of-contents/
**Summary:** The canonical SRE reference from Google. Establishes the theoretical foundation for SLI/SLO/SLA frameworks, error budgets as a mechanism to balance reliability investment against feature velocity, and the four golden signals (latency, traffic, errors, saturation). Defines the principle that 100% reliability is the wrong target and that error budgets make risk explicit and negotiable.

## Kubernetes Monitoring Integration
**URL:** https://docs.newrelic.com/docs/kubernetes-pixie/kubernetes-integration/get-started/introduction-kubernetes-integration/
**Summary:** New Relic's Kubernetes integration documentation. Covers cluster-level metrics (node health, pod scheduling latency, control plane components), namespace-level resource utilization, and integration with NR Service Architecture Intelligence for K8s workload topology.

## OpenTelemetry Kubernetes Monitoring — Generally Available
**URL:** https://docs.newrelic.com/whats-new/2025/07/whats-new-7-01-k8s-otel-monitoring/
**Summary:** Announcement of GA for OTel-based Kubernetes monitoring in New Relic (July 2025). Covers the OTel Collector-based K8s monitoring approach enabling GitOps-native cluster observability configuration. Supports L3/L4 criteria for platform teams adopting OTel-native infrastructure monitoring.

## Engineering Excellence: Maturity Framework Introduction
**URL:** https://docs.newrelic.com/docs/new-relic-solutions/observability-maturity/engineering-excellence/introduction/
**Summary:** New Relic's Engineering Excellence value driver framework. Covers operational efficiency, proactive change management, and enhanced security posture. Provides NR-specific framing for Developer Experience and Platform Engineering domain rubric design and PE Track acceleration path activities.

## A Blueprint for Multi-Tiered Service Level Management
**URL:** https://newrelic.com/blog/observability/a-blueprint-for-multi-layer-service-level-management
**Summary:** A reference architecture for applying SLM across all five tiers of a modern stack: Layer 1 (Experience — Core Web Vitals and synthetic monitors), Layer 2 (Gatekeeper — CDN/load balancer edge health), Layer 3 (Service Domain — microservices using the RED Method with separate error rate and latency SLOs), Layer 4 (Foundation — infrastructure capacity and K8s health), and Layer 5 (Business Outcomes — conversion, revenue, engagement). Introduces the Observability Gap concept (infrastructure green, service degraded) and the Service Level Control Plane as the organizational governance model. Authored by Jim Hagan, Principal Solution Architect, New Relic.
