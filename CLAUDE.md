# CLAUDE.md — Observability Rubric

## What this repo is

A structured maturity rubric for assessing observability practices across customer environments. It contains 54 rules across 10 domains. Each rule is scored Level 1–5 by a human assessor (or AI agent) against defined criteria and evidence signals.

The content is human-authored markdown. The primary goal is readability in GitHub and low friction for collaborators adding and editing rules.

## Repo structure

```
rubric/
├── README.md           ← domain index and scoring model
├── STRUCTURE.md        ← authoring guide (read this before editing)
└── domains/
    ├── 01-instrumentation-coverage/
    │   ├── _domain.md              ← domain summary + rule list
    │   └── <rule-slug>/
    │       ├── _rule.md            ← rule name, IDs, purpose, scoring summary table
    │       ├── level-1.md … level-5.md   ← criteria, evidence signals, guidance
    │       └── scorecards.md       ← relevant New Relic Scorecard rules
    └── … (10 domains total)
```

Domain folders are numbered (`01-` … `10-`) to control display order in GitHub. Rule folders are kebab-case slugs of the rule name. Files prefixed with `_` sort to the top in file browsers.

## Key IDs

Each `_rule.md` carries two IDs:

- `**Rule ID:**` — a stable semantic ID derived from the domain abbreviation and position within the domain (e.g. `IC-01`, `SLM-03`). Use this in cross-references.
- `**Sheet Rule ID:**` — the original row number from `rubric.xlsx`. Use this to trace back to the source spreadsheet.

## Evidence signal types

Each signal in a `level-N.md` file declares its type with `**Type:**`. Valid values:

| Type | Meaning |
|---|---|
| `scorecard` | Evidence from a New Relic Scorecard check |
| `nrql` | NRDB query — include the NRQL in a fenced `nrql` code block |
| `graphql` | NerdGraph query — include in a fenced `graphql` code block |
| `question` | Question to ask the customer directly during assessment |
| `tool` | Output from an external tool, script, or integration |

## Scoring model

Levels run 1–5. The overall domain score is the **modal** level across its rules — the level most commonly achieved. The overall rubric score is the modal level across all 54 rules.

## Source data

`rubric.xlsx` in the repo root is the original source spreadsheet. The markdown files were generated from it. The spreadsheet is kept for reference; the markdown files are the authoritative content going forward.

## When generating or editing content

- Do not introduce YAML frontmatter or JSON — all metadata uses `**Key:** Value` bold pairs.
- Guidance sections (`## Guidance to reach Level N+1`, `#### Guidance to meet this signal`) are optional — omit the heading entirely rather than leaving a blank section.
- Evidence signals that have not yet been fleshed out are marked `**Type:** \`question\`` with a brief note from the spreadsheet. When expanding them, update the type to the correct value and write the full signal description.
- `_To be completed._` placeholders appear in `## Purpose` sections of `_rule.md` — these are the primary authoring backlog.
- When adding a new rule: create the folder, `_rule.md`, five level files, and `scorecards.md`; add the rule to the domain's `_domain.md`; and update `README.md` if the total rule count changes.
