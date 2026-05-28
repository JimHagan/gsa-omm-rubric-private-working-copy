# Alert Condition Quality

**Domain:** Alerting & Detection  
**Rule ID:** AD-04  
**Sheet Rule ID:** 33  

## Purpose

_To be completed._

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | All alert conditions use static fixed thresholds on individual metrics. No NRQL conditions, no anomaly detection. Alert configuration reflects the tool default, not deliberate design. |
| 2 | Mix of static and NRQL conditions. Severity tiers documented but inconsistently applied. Some runbooks linked. |
| 3 | NRQL-based dynamic conditions and NR Smart Alerts (anomaly detection) active on revenue-path services. The four golden signals covered: latency, traffic, errors, and saturation. |
| 4 | SLO burn-rate alerts configured for services with active SLOs — fast-burn (2% budget consumed in 1h) and slow-burn (5% in 6h). Runbooks linked to all critical alert conditions. |
| 5 | NR NRQL PREDICT-based conditions detect projected violations before they occur. NR Applied Intelligence alert grouping active. Noise is the exception. |
