# Cloud Service Integration Coverage

**Domain:** Instrumentation Coverage  
**Rule ID:** IC-04  
**Sheet Rule ID:** 4  

## Purpose

_To be completed._

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | Cloud provider services (AWS, Azure, GCP) visible only as external calls in APM traces. No native NR cloud integrations active. |
| 2 | Core cloud services directly supporting the revenue path integrated (e.g., RDS, ECS, Lambda functions used by critical application flows). |
| 3 | Cloud integrations cover supporting managed services — primary databases, queue services, CDN, and key platform-as-a-service components reporting independently into NR. |
| 4 | All cloud services including infrastructure components integrated. NR Cloud Cost Intelligence (CCI) active — cloud cost attributed by service team. |
| 5 | Cloud integration provisioning automated. New cloud resources detected and integrated without manual configuration. Coverage self-maintaining as infrastructure scales. |
