# References

## OpenTelemetry Specification Overview
**URL:** https://opentelemetry.io/docs/specs/otel/overview/
**Summary:** The normative specification for MELT telemetry signals (Metrics, Events, Logs, Traces), W3C Trace Context propagation headers, and the OTLP wire protocol. Defines what 'OTel standards adopted' means at L3 and the semantic attributes required for L4.

## OpenTelemetry Traces: Best Practices in New Relic
**URL:** https://docs.newrelic.com/docs/opentelemetry/best-practices/opentelemetry-best-practices-traces/
**Summary:** New Relic's best practices guide for OTel trace data. Covers span link configuration for preserving trace context across async queue boundaries (Kafka, SQS, RabbitMQ) where standard header propagation is not possible. Authority for L4/L5 criteria on async boundary trace context preservation.

## New Relic Now+ 2025: Innovation Roundup
**URL:** https://newrelic.com/blog/nerdlog/new-relic-now-2025-innovation-roundup
**Summary:** Comprehensive roundup of NR capabilities announced at Now+ 2025. Key features: Database Performance Monitoring GA for MySQL/PostgreSQL/MSSQL, Queues & Streams with Kafka bi-directional consumer lag drill-down, Service Architecture Intelligence topology maps, Cloud Cost Intelligence, and Pipeline Control for ingest governance.
