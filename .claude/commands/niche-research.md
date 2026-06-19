---
description: Turn Elise's raw manual Amazon observations into a populated niche scorecard + competitor analysis, matching repo format and guardrails.
argument-hint: <path-to-intake-file>  e.g. research/_intake/004_anger_intake.md
---

# /niche-research — QMN Niche Research Builder ($0 semi-auto)

You are operating inside the `qmn-kdp-publishing-engine` repo. Elise has already done the
**manual** Amazon research (compliant with `research/manual_amazon_research_instructions.md` —
no scraping was used). Your job is to turn her raw notes into finished, repo-formatted research
documents. You do NOT collect any data yourself.

## Input

Read the intake file the user passed: **$ARGUMENTS**

If no path was given, ask for one and stop.

## Before you write anything, read these for format + rules

1. `docs/niche_research_framework.md`  — the 100-point scoring rubric (10 categories × 10).
2. `research/scoring/niche_scorecard_template.md`  — the exact scorecard structure to follow.
3. `CLAUDE.md`  — project guardrails. These are hard rules.

## What to produce

Create TWO files (numbered by checking the highest existing `00X` in `research/scoring/`):

### File 1 — `research/scoring/00X_[niche-slug]_score.md`
Populate the scorecard template **exactly**, filling from the intake:
- Niche Overview (pain point, age, search phrases, brand-fit summary)
- Competitor Observation Table — one row per competitor from the intake
  (Title | Author Type | BSR | Price | Reviews | Avg Rating | Cover Quality | Notes)
- Review Mining Notes — reorganize Elise's raw notes into the four buckets, in your own words
- BSR Observation Notes
- Market Gap Hypothesis — synthesize from the competitor pattern; mark what still needs validation
- Series Potential, Monetization Angle, Copyright/IP Risk Notes
- 100-Point Scoring Table — **fill the score column with SUGGESTED scores**, but label the
  block clearly: `SUGGESTED SCORES — Elise must confirm or override`. Put a one-line rationale
  for each score in the Notes column, tied to the rubric in the framework file.
- Leave the Final Recommendation sign-off and Elise decision/date lines BLANK.

### File 2 — `research/scoring/00X_[niche-slug]_competitor_analysis.md`
A deeper pattern write-up (like a competitor briefing): the formats present in the niche,
the strongest competitors and why, the observed pattern, the best differentiated doorway for QMN,
and 2–3 provisional positioning directions. Prose, not a workbook.

## Hard guardrails (from CLAUDE.md — refuse/flag, never violate)

- Do NOT copy any competitor title, subtitle, description, or character concept into QMN
  suggestions. Reference competitors only to contrast against them.
- Any QMN title/character idea you propose must be original. No Disney/Pixar/Sesame/etc.
  characters, no living-artist style references, no trademarked mascots or brands.
- If the niche sits near a known IP (e.g. Inside Out for emotion characters), FLAG it explicitly
  in the IP Risk section and suggest how to steer clear.
- Scores and final sign-off are Elise's. You only *suggest*. Make that unmistakable.
- Do NOT make claims guaranteeing Amazon ranking, approval, or sales.

## Finish — do NOT commit

Per CLAUDE.md, never commit/push without explicit instruction. After writing the two files:
1. Print a short summary: niche, # competitors processed, suggested total score, top IP flag.
2. State the planned branch (`claude/gate-7-00X-[niche-slug]`) and the two file paths.
3. Say: *"Files written, holding for your review. Say 'approved, commit and push' to proceed."*
4. Stop.
