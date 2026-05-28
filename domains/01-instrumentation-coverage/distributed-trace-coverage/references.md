# References

## OpenTelemetry Specification Overview
**URL:** https://opentelemetry.io/docs/specs/otel/overview/
**Summary:** The normative specification for MELT telemetry signals (Metrics, Events, Logs, Traces), W3C Trace Context propagation headers, and the OTLP wire protocol. Defines what 'OTel standards adopted' means at L3 and the semantic attributes required for L4.

## OpenTelemetry Semantic Conventions — Traces, Metrics, Logs
**URL:** https://opentelemetry.io/docs/concepts/semantic-conventions/
**Summary:** Defines standardized attribute keys for HTTP (http.route, http.method, http.status_code), database (db.system, db.statement), messaging (messaging.system, messaging.destination), and RPC (rpc.method, rpc.service) telemetry. These specific attribute names are the L4 scoring criteria for semantic attribute completeness.

## W3C Trace Context: Traceparent and Tracestate Headers
**URL:** https://opentelemetry.io/docs/specs/otel/context/api-propagators/
**Summary:** The specification for distributed trace context propagation using W3C traceparent and tracestate headers. Defines how trace context must be preserved across synchronous HTTP calls and injected/extracted across async queue boundaries. Authority for the L3 criterion requiring end-to-end trace context propagation including across async boundaries.

## Introduction to OpenTelemetry and New Relic
**URL:** https://docs.newrelic.com/docs/opentelemetry/opentelemetry-introduction/
**Summary:** New Relic's guide to the OTel integration architecture. Covers OTLP ingest, auto-instrumentation agent configuration, and NR-specific collector patterns. Validates the 'OTel standards adopted' criterion at L3 and documents W3C trace context propagation within the NR platform.

## OpenTelemetry Traces: Best Practices in New Relic
**URL:** https://docs.newrelic.com/docs/opentelemetry/best-practices/opentelemetry-best-practices-traces/
**Summary:** New Relic's best practices guide for OTel trace data. Covers span link configuration for preserving trace context across async queue boundaries (Kafka, SQS, RabbitMQ) where standard header propagation is not possible. Authority for L4/L5 criteria on async boundary trace context preservation.
