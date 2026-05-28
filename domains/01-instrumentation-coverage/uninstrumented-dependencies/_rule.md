# Uninstrumented Dependencies

**Domain:** Instrumentation Coverage  
**Rule ID:** IC-08  
**Sheet Rule ID:** 8  

## Purpose

_To be completed._

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | Many uninstrumented external dependencies visible in NR — third-party APIs and external services appear as unknown endpoints in trace waterfalls. Dependency failures cannot be attributed. |
| 2 | Primary external dependencies on the revenue path identifiable (main payment API, core auth service). Most databases and secondary external services still appear as uninstrumented spans. |
| 3 | All external dependencies on the revenue path and its direct supporting services are either independently monitored, integrated via NR OHI or cloud integration, or formally acknowledged as unmonitorable with documented rationale. No unknown dependencies in the critical path trace. |
| 4 | All external dependencies across the application estate accounted for — instrumented, integrated, or documented as explicit exceptions. Dependency topology is accurate and complete. |
| 5 | Intelligent Observability Scorecard uninstrumented entity count is zero. New external dependencies auto-detected and triaged for instrumentation on service deployment. |
