# Queue & Stream Visibility

**Domain:** Instrumentation Coverage  
**Rule ID:** IC-16  
**Sheet Rule ID:** 30  

## Purpose

_To be completed._

## Primary Use Case

**Use Case Group:** Detect and Resolve  
**Use Case:** Upstream & Downstream Dependencies

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | No queue monitoring in NR. Kafka/SQS/RabbitMQ health is a blind spot. Consumer lag discovered only when downstream services start failing. |
| 2 | Queue depth visible for primary queues as a basic metric. Consumer lag not tracked independently of the latency observed on services consuming the queue. |
| 3 | NR Queues & Streams deployed for queues that serve the revenue path. Consumer lag, throughput, and error rate visible per consumer group and topic. Lag alert conditions configured. |
| 4 | SLOs defined on consumer lag targets for critical queues. NR anomaly detection active on consumer lag — slow producers surface automatically. |
| 5 | Queue health metrics integrated into the SLOs of the services that consume them. All queues across the application estate monitored. No queue-related blind spots remain. |
