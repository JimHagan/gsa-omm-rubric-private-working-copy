# Rubric Structure Guide

This document explains the folder layout, file naming conventions, and authoring format for the Observability Rubric. Read this before adding or editing content.

---

## Folder Layout

```
├── README.md                          ← rubric overview, domain index, scoring model
├── STRUCTURE.md                       ← this file (authoring guide)
├── use_cases.md                       ← use case framework index and rule mapping
└── domains/
    ├── 01-instrumentation-coverage/
    │   ├── _domain.md                 ← domain summary and rule list
    │   ├── sli-coverage-rate/
    │   │   ├── _rule.md               ← rule overview, use case, and level summary table
    │   │   ├── level-1.md
    │   │   ├── level-2.md
    │   │   ├── level-3.md
    │   │   ├── level-4.md
    │   │   ├── level-5.md
    │   │   ├── scorecards.md          ← relevant New Relic Scorecard rules
    │   │   └── references.md          ← backing industry and NR documentation
    │   └── another-rule/
    │       └── ...
    ├── 02-service-level-management/
    │   └── ...
    └── 03-alerting-detection/
        └── ...
```

### Naming conventions

| Item | Convention | Example |
|---|---|---|
| Domain folder | `NN-kebab-case` (numbered for ordering) | `01-instrumentation-coverage` |
| Rule folder | `kebab-case` matching the rule name | `sli-coverage-rate` |
| Domain/rule summary files | Prefixed with `_` (sorts to top in browsers) | `_domain.md`, `_rule.md` |
| Level files | `level-N.md` where N is 1–5 | `level-3.md` |
| Rule ID prefix | Domain abbreviation + two-digit number | `IC-01`, `SLM-03`, `IM-08` |

---

## File Templates

### `_domain.md`

```markdown
# <Domain Name>

<One paragraph describing what this domain assesses and why it matters.>

## Rules in this domain

- [Rule Name](rule-folder/_rule.md)
- [Rule Name](rule-folder/_rule.md)
```

---

### `_rule.md`

```markdown
# <Rule Name>

**Domain:** <Domain Name>  
**Rule ID:** <XX-NN>  
**Sheet Rule ID:** <N>  

## Purpose

<What this rule measures and why it matters to observability maturity.>

## Primary Use Case

**Use Case Group:** <Detect and Resolve | Improve Quality | Improve Efficiency>  
**Use Case:** <Use Case Name>

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | <one-line description> |
| 2 | <one-line description> |
| 3 | <one-line description> |
| 4 | <one-line description> |
| 5 | <one-line description> |
```

The `## Primary Use Case` section maps this rule to the New Relic Foundational Use Case framework. See `use_cases.md` at the repo root for the full framework description and the cross-reference table of all 54 rules.

---

### `level-N.md`

```markdown
# Level N

## Criteria

<Full description of what must be true for a customer to be at this level.
Write this for a human assessor — be specific about what "looks like" this level.>

## Evidence Signals

### Signal 1: <Signal Name>

**Type:** `<scorecard | nrql | graphql | question | tool>`

<Describe what to look for, how to interpret results, and any caveats.
For queries, include a fenced code block. For questions, write out the
question(s) to ask the customer verbatim.>

```nrql
SELECT count(*) FROM ...
```

#### Guidance to meet this signal

<Optional. Links, docs, steps, or explanation of what needs to change for
the customer to satisfy this signal. Omit the heading if not applicable.>

### Signal 2: <Signal Name>

...

## Guidance to reach Level <N+1>

<Optional. What the customer needs to do to progress to the next level.
Include links to New Relic docs, videos, or partner resources. Omit for level 5.>
```

---

### `scorecards.md`

Lists the New Relic Scorecard rules that provide automated evidence for this rubric rule. Written in plain prose or as a bullet list — no fixed schema. Describes which scorecard template each rule lives in, what it checks, and how its result maps to a rubric level boundary.

```markdown
# Relevant Scorecard Rules

- **Intelligent Observability Scorecard — Team Tag Coverage**: Pass criterion is APM entity has
  a team tag value. Aggregate % maps to IC-05 level boundaries.

- **Business Uptime Scorecard — Alert Noise Baseline**: < 15 incidents per 7-day window per
  entity. Maps to AD-01 L3/L4 boundary.
```

---

### `references.md`

Lists the industry standards, New Relic platform documentation, research reports, and enablement resources that back the scoring criteria for this rule. Each entry includes a full title, URL, and a summary explaining its relevance.

```markdown
# References

## Site Reliability Engineering: How Google Runs Production Systems
**URL:** https://sre.google/sre-book/table-of-contents/
**Summary:** Canonical authority for SLI/SLO/SLA theory and the four golden signals...

## Service Level Management: Optimize SLM Guide
**URL:** https://docs.newrelic.com/docs/...
**Summary:** New Relic's primary SLM guide. Defines the three SLI types...
```

References are organised roughly from foundational industry standards through to NR platform docs, research data, and enablement resources. A rule may have one reference or many — include all that directly back the scoring criteria for this specific rule.

---

## Evidence Signal Types

Each signal must declare its **Type** using one of the tags below. This enables future tooling to filter and process signals by category.

| Type | Meaning |
|---|---|
| `scorecard` | Evidence surfaced by a New Relic Scorecard check |
| `nrql` | A query against NRDB — include the NRQL in a fenced `nrql` code block |
| `graphql` | A NerdGraph query — include in a fenced `graphql` code block |
| `question` | A direct question to ask the customer during the assessment conversation |
| `tool` | Output or result from an external tool, script, or integration |

---

## Use Case Framework

Every rule is mapped to a **Primary Use Case** drawn from the New Relic Foundational Use Case framework. The three use case groups are:

| Group | What it measures |
|---|---|
| **Detect and Resolve** | Speed and accuracy of detecting and resolving failures before customer impact |
| **Improve Quality** | Reliability, performance, and functional correctness from the user's perspective |
| **Improve Efficiency** | Operational overhead: infrastructure cost, deployment toil, developer cognitive load |

See `use_cases.md` for the full framework, use case definitions, and the complete mapping of all 54 rules.

---

## Authoring Notes

- All content is plain GitHub-flavoured markdown — no YAML, no JSON.
- Metadata (`**Domain:**`, `**Rule ID:**`, `**Type:**`) uses bold key-value pairs rather than frontmatter. This is intentional to keep files human-editable without a schema.
- Guidance sections (`#### Guidance to meet this signal`, `## Guidance to reach Level N+1`) are **optional**. Omit the heading entirely if there is nothing to say — don't leave empty sections.
- Evidence signals are **also optional**. A level file with no signals is valid: include the `## Evidence Signals` heading and a brief note explaining why signals are not yet defined or are not applicable.
- When adding a new rule, also add it to the `## Rules in this domain` list in `_domain.md` and to the domain table in the root `README.md`.

---

## Adding a New Rule — Checklist

1. Create a folder under the appropriate domain: `domains/NN-domain-name/rule-name/`
2. Create `_rule.md` from the template above — include `**Sheet Rule ID:**`, `## Purpose`, `## Primary Use Case`, and `## Scoring Summary`
3. Create `level-1.md` through `level-5.md` from the template above
4. Create `scorecards.md` listing any relevant New Relic Scorecard rules
5. Create `references.md` listing the industry and NR documentation that backs this rule
6. Add the rule to `_domain.md` in the domain folder
7. Add the rule to the appropriate use case table in `use_cases.md`
8. If it's a new domain, also add it to the domain table in `README.md`

---

## Worked Example

See [domains/02-service-level-management/sli-coverage-rate/](domains/02-service-level-management/sli-coverage-rate/) for a fully populated rule illustrating all conventions.
