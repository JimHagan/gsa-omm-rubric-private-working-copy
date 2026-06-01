# Project Context — Observability Maturity Model (OMM) Rubric

> Handoff context for a Claude Code agent picking up work on this repository.
> Written 2026-06-01. This file is a snapshot — verify against the live tree before relying on counts.

---

## What this repo is

A structured maturity rubric for assessing observability practices across customer environments, built for New Relic's Global Solution Architecture team. It encapsulates a model originally developed in a spreadsheet (`rubric.xlsx`) into a first-class, version-controlled data model of human-authored markdown.

**Scale:** 54 rules across 10 domains. Each rule is scored Level 1–5 by a human assessor (or AI agent) against defined criteria and evidence signals.

**End goal:** make the rubric rich enough to power *in-product AI experiences* related to observability maturity — an AI agent should be able to read a single rule folder and have everything it needs: scoring criteria, evidence signals, the authoritative sources behind each criterion, and the business use case the rule serves.

**Primary design value:** readability in GitHub and low friction for collaborators adding/editing rules. All content is plain GitHub-flavoured markdown. **No YAML frontmatter, no JSON** — all metadata uses `**Key:** Value` bold pairs.

---

## Repo structure

```
├── README.md           ← domain index + scoring model
├── STRUCTURE.md        ← authoring guide (READ THIS before editing)
├── use_cases.md        ← use case framework + full rule→use-case mapping
└── domains/
    ├── 01-instrumentation-coverage/
    │   ├── _domain.md
    │   └── <rule-slug>/
    │       ├── _rule.md         ← name, IDs, purpose, primary use case, scoring table
    │       ├── level-1.md … level-5.md   ← criteria, evidence signals, guidance
    │       ├── scorecards.md    ← relevant New Relic Scorecard rules
    │       └── references.md    ← backing industry + NR documentation
    └── … (10 domains, 01- through 10-)
```

Domain folders are numbered `01-`…`10-` to control GitHub display order. Rule folders are kebab-case slugs. `_`-prefixed files sort to the top in file browsers.

### Domain breakdown

| # | Domain | Rules | ID prefix |
|---|--------|-------|-----------|
| 01 | Instrumentation Coverage | 16 | `IC-` |
| 02 | Service Level Management | 5 | `SLM-` |
| 03 | Alerting & Detection | 4 | `AD-` |
| 04 | Digital Experience | 3 | `DE-` |
| 05 | Dashboards & Shared Insights | 3 | `DSI-` |
| 06 | Incident Management | 8 | `IM-` |
| 07 | Business Alignment | 4 | `BA-` |
| 08 | Platform Health & Infra SLM | 2 | `PH-` |
| 09 | OaC & Governance | 6 | `OAC-` |
| 10 | Developer Experience | 3 | `DX-` |

---

## Key IDs

Each `_rule.md` carries two IDs:

- **`**Rule ID:**`** — stable semantic ID from domain abbreviation + position (e.g. `IC-01`, `SLM-03`). Use in cross-references.
- **`**Sheet Rule ID:**`** — original row number from `rubric.xlsx`. Use to trace back to source. Note: the spreadsheet has gaps (items 29 and 39 were deleted), so Sheet Rule IDs are not contiguous.

---

## Evidence signal types

Each signal in a `level-N.md` declares its type with `**Type:**`:

| Type | Meaning |
|---|---|
| `scorecard` | Evidence from a New Relic Scorecard check |
| `nrql` | NRDB query — include NRQL in a fenced `nrql` block |
| `graphql` | NerdGraph query — include in a fenced `graphql` block |
| `question` | Question to ask the customer directly during assessment |
| `tool` | Output from an external tool, script, or integration |

---

## Use case framework

Every rule maps to a **Primary Use Case** in `_rule.md`, drawn from New Relic's Foundational Use Case framework (source: the *Foundational Use Case OMM Domain Mapping* tab in `rubric.xlsx`). Three groups:

| Group | Rules | What it measures |
|---|---|---|
| **Detect and Resolve** | 26 | Speed/accuracy of detecting and resolving failures before customer impact |
| **Improve Quality** | 17 | Reliability, performance, functional correctness from the user's perspective |
| **Improve Efficiency** | 11 | Operational overhead: infra cost, deployment toil, developer cognitive load |

`use_cases.md` at the repo root has the full framework: group definitions, 10 use case definitions, and a cross-reference table mapping every rule to its use case.

---

## Scoring model

Levels run 1–5. The overall **domain score** is the **modal** level across its rules (most common, NOT average). The overall **rubric score** is the modal level across all 54 rules. A single L1 domain is flagged as a P0 gap regardless of overall posture.

---

## Source data: `rubric.xlsx`

The original spreadsheet is **NOT committed to the repo** (intentional — kept out of version control). The markdown is authoritative going forward. The spreadsheet has 10 tabs; the most important for this work:

- **Discovery Worksheet (Template)** — the 54 rules with scoring criteria. Source of truth for rule content.
- **Technical References** — 60-entry bibliography (Parts A–D: industry standards, NR docs, NR research, NR University enablement). Source for `references.md` files.
- **Foundational Use Case OMM Domain Mapping** — domain×level×use-case mapping. Source for the Primary Use Case fields.
- Other tabs: Index, Attainment Level Reference, Maturity Matrix (Rubric), Summary Readout, Observability Domains, Platform Eng vs Service Eng Tracks, Acceleration Plan.

If you need the spreadsheet, ask the user — they share it via Google Drive or direct upload. There is a Google Drive MCP integration in some sessions, but access can be flaky; direct file upload to the session has been the reliable path.

**Important caveat on the Technical References tab:** the "Used In / Supports" column references rule item numbers from an *older* version of the worksheet — the numbers have drifted and are mostly wrong. Always match references to rules by **topic/description**, never by the cited item number.

---

## What's been done (as of this handoff)

Recent work (on branch `claude/blissful-allen-xNJw1`, PR #2 open against `main`):

1. **`references.md` added to all 54 rules** — industry + NR documentation backing each rule, drawn from the 60-entry bibliography plus two NR blog posts (alert lifecycle architecture; multi-tiered SLM, both by Jim Hagan). Format: `## Title` / `**URL:**` / `**Summary:**` blocks. One orphaned reference (originally backing deleted rule item 29) was re-mapped to the Alerting & Detection rules rather than dropped.

2. **`## Primary Use Case` section added to all 54 `_rule.md` files** — sits between `## Purpose` and `## Scoring Summary`.

3. **`use_cases.md` created** at repo root.

4. **`STRUCTURE.md` updated** to document the full per-rule file set, the use case framework, and an expanded new-rule checklist.

---

## Authoring backlog (what still needs doing)

These are the known gaps, roughly in priority order:

1. **54 `Purpose` sections are placeholders.** Every `_rule.md` still has `## Purpose\n\n_To be completed._`. This is the single largest content backlog. Writing these would benefit from the NR research data in the references (Part C of the bibliography) to frame the *why*.

2. **Evidence signals are mostly undeveloped.** ~71 of 270 level files still have `**Type:** \`question\`` placeholder signals carrying brief notes from the spreadsheet. These need expanding to proper `nrql` / `graphql` / `scorecard` typed signals with real queries. The Discovery Worksheet's "Source / Method" and "Platform Scorecard Coverage" columns are the raw material.

3. **`scorecards.md` files are informally written.** Good content but not in a consistent typed format. Could be standardised.

---

## Conventions & gotchas

- **No YAML/JSON.** Metadata is `**Key:** Value` bold pairs only. This is a hard rule from `CLAUDE.md`.
- **Optional sections are omitted, not left blank.** Guidance headings (`## Guidance to reach Level N+1`, `#### Guidance to meet this signal`) should be dropped entirely if empty — never leave an empty section.
- **When adding a rule:** create the folder + `_rule.md` + 5 level files + `scorecards.md` + `references.md`; add it to `_domain.md`; add it to `use_cases.md`; update `README.md` if the total count changes. (Full checklist in `STRUCTURE.md`.)
- **Trailing two-space line breaks** are used in the `**Key:** Value` metadata blocks — preserve them.
- **Branch discipline:** development has been on `claude/blissful-allen-xNJw1`. Confirm the active branch with the user before pushing.

---

## Pointers

- Read `STRUCTURE.md` first — it's the authoritative authoring guide.
- Read `use_cases.md` for the business-outcome lens.
- The worked example rule is `domains/02-service-level-management/sli-coverage-rate/`.
