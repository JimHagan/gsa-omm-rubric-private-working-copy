# Rubric Structure Guide

This document explains the folder layout, file naming conventions, and authoring format for the Observability Rubric. Read this before adding or editing content.

---

## Folder Layout

```
rubric/
├── README.md                          ← rubric overview, domain index, scoring model
├── STRUCTURE.md                       ← this file
└── domains/
    ├── 01-instrumentation-coverage/
    │   ├── _domain.md                 ← domain summary and rule list
    │   ├── sli-coverage-rate/
    │   │   ├── _rule.md               ← rule overview and level summary table
    │   │   ├── level-1.md
    │   │   ├── level-2.md
    │   │   ├── level-3.md
    │   │   ├── level-4.md
    │   │   └── level-5.md
    │   └── another-rule/
    │       └── ...
    ├── 02-digital-experience/
    │   └── ...
    └── 03-incident-management/
        └── ...
```

### Naming conventions

| Item | Convention | Example |
|---|---|---|
| Domain folder | `NN-kebab-case` (numbered for ordering) | `01-instrumentation-coverage` |
| Rule folder | `kebab-case` matching the rule name | `sli-coverage-rate` |
| Domain/rule summary files | Prefixed with `_` (sorts to top in browsers) | `_domain.md`, `_rule.md` |
| Level files | `level-N.md` where N is 1–5 | `level-3.md` |
| Rule ID prefix | Two-letter domain abbreviation | `IC-`, `DE-`, `IM-` |

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

## Purpose

<What this rule measures and why it matters to observability maturity.>

## Scoring Summary

| Level | Summary |
|---|---|
| 1 | <one-line description> |
| 2 | <one-line description> |
| 3 | <one-line description> |
| 4 | <one-line description> |
| 5 | <one-line description> |
```

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

## Authoring Notes

- All content is plain GitHub-flavoured markdown — no YAML, no JSON.
- Metadata (`**Domain:**`, `**Rule ID:**`, `**Type:**`) uses bold key-value pairs rather than frontmatter. This is intentional to keep files human-editable without a schema.
- Guidance sections (`#### Guidance to meet this signal`, `## Guidance to reach Level N+1`) are **optional**. Omit the heading entirely if there is nothing to say — don't leave empty sections.
- Evidence signals are **also optional**. A level file with no signals is valid: include the `## Evidence Signals` heading and a brief note explaining why signals are not yet defined or are not applicable.
- When adding a new rule, also add it to the `## Rules in this domain` list in `_domain.md` and to the domain table in the root `README.md`.

---

## Adding a New Rule — Checklist

1. Create a folder under the appropriate domain: `domains/NN-domain-name/rule-name/`
2. Create `_rule.md` from the template above
3. Create `level-1.md` through `level-5.md` from the template above
4. Add the rule to `_domain.md` in the domain folder
5. If it's a new domain, also add it to the domain table in `README.md`

---

## Worked Example

See [domains/02-service-level-management/sli-coverage-rate/](domains/02-service-level-management/sli-coverage-rate/) for a fully populated rule illustrating all conventions.
