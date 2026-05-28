# References

## Observability as Code — Technology Radar Recommendation
**URL:** https://www.thoughtworks.com/radar/techniques/observability-as-code
**Summary:** Thoughtworks Technology Radar's entry recommending Observability as Code as an industry best practice. Provides independent third-party authority for the principle that dashboards, alert policies, SLOs, and synthetic monitors should be managed as versioned code artifacts rather than UI-created configurations.

## Observability as Code Guide
**URL:** https://docs.newrelic.com/docs/new-relic-solutions/observability-maturity/operational-efficiency/observability-as-code-guide/
**Summary:** New Relic's primary OaC guide. Covers Terraform and NerdGraph provisioning approaches for dashboards, alert policies, SLOs, and synthetics; CI/CD pipeline design; and drift detection patterns. Defines the OaC maturity levels that map directly to OaC & Governance domain L2–L5 scoring criteria.

## Automate Configuration with Observability as Code (Terraform Series)
**URL:** https://newrelic.com/blog/observability/examples-observability-as-code-part-one
**Summary:** Practical Terraform implementation guide for NR configurations. Demonstrates modular Terraform modules for dashboards, alert policies, synthetic monitors, entity tags, and workloads. Validates the 'no exceptions for UI-only creation' principle at L3.

## Getting Started with New Relic and Terraform
**URL:** https://docs.newrelic.com/docs/infrastructure-as-code/terraform/terraform-intro/
**Summary:** New Relic's introductory Terraform guide. Covers provider configuration, four golden signals alert setup via Terraform, and the complete set of NR Terraform resource types (alerts, dashboards, synthetics, SLOs, workloads).

## New Relic Observability as Code — Open Source Hub
**URL:** https://newrelic.github.io/observability-as-code/
**Summary:** New Relic's open-source OaC toolkit hub. Covers the NR CLI for configuration management, the Terraform provider, and community-contributed OaC templates. Entry point for teams implementing version-controlled artifact management at L3 and CI/CD pipeline automation at L4.
