# QMN Research Automation — How the Loop Works

*Documentation for Elise and any AI assistant working in this repo.*
*Last updated: 2026-06-19*

---

## What Is and Is Not Automated

### Manual (always Elise)

- All Amazon searches — Elise searches Amazon.com by hand, no scraping, no tools
- Competitor observation — Elise reads and records BSR, review counts, prices, cover quality
- Review mining — Elise reads reviews and summarizes in her own words
- Score confirmation — Elise reviews AI suggested scores and sets Elise Final scores
- Decision sign-off — Elise approves or rejects every niche via `/niche-signoff`
- All production decisions — manuscript, character design, illustration, KDP submission

### AI-assisted (Claude, with Elise supervision)

- Structuring Elise's raw intake notes into formatted scorecards
- Suggesting scores with explicit rationale (labeled "Suggested AI" — not binding)
- Writing competitor analysis pattern briefings from Elise's observations
- Updating the master tracker after Elise confirms
- Flagging IP risks and updating `ip_watchlist.md`

---

## The v2 Research Loop

```
Elise does Amazon research
        ↓
Elise fills in INTAKE_TEMPLATE.md (niche_id required, ≥3 search phrases required)
        ↓
/niche-research <intake-file>
        ↓
AI reads intake → reads framework + template + tracker + CLAUDE.md
        ↓
AI checks THIN EVIDENCE (< 3 phrases → cap at Revise, flag in header)
        ↓
AI checks ip_watchlist.md → flags any IP collisions → adds/refreshes rows
        ↓
AI writes/updates <niche_id>_<slug>_score.md (Suggested AI scores, Elise Final blank)
AI writes/updates <niche_id>_<slug>_competitor_analysis.md
AI updates gate_7_niche_shortlist.md tracker row (Suggested score, Elise Score blank)
        ↓
AI prints summary + holds for Elise review
        ↓
Elise reviews scorecard, adjusts suggested scores, makes notes
        ↓
/niche-signoff <niche_id>
        ↓
AI writes Elise Final scores + decision to scorecard
AI updates tracker row (Elise Score, Status → Signed, Decision)
        ↓
Gate 7 selection complete when all priority niches are Signed
```

---

## ID Stability Rule

Each niche has one permanent `niche_id` (e.g. `006`). This ID never changes and is never reused.

- Scorecard is always at `research/scoring/<niche_id>_<slug>_score.md`
- Competitor analysis is always at `research/scoring/<niche_id>_<slug>_competitor_analysis.md`
- If a scorecard with that ID already exists, `/niche-research` updates it in place — it never creates a duplicate number
- If a niche genuinely has no ID yet, `/niche-research` stops and asks Elise before creating anything

---

## Demand vs. Differentiation Evidence (Critical Distinction)

These are two different things. Never conflate them.

**Demand evidence:** Proof that parents are actively searching and buying in this space.
- High review counts on existing titles (1,000+ = meaningful; 5,000+ = strong)
- BSRs in the active range (#1,000–#50,000 in Books)
- Sponsored ads visible on the search phrase
- Multiple titles with similar strong BSRs

**Differentiation evidence:** Proof that a QMN-style entry is not already occupied.
- Zero children's picture books in search results
- No storybook-format entry in results (only workbooks)
- No metaphor matching QMN's proposed approach
- No title using QMN's exact framing

A zero-results search for an invented title (e.g., "The Little Loud Brain") is differentiation evidence ONLY. It proves the space is unoccupied. It does NOT prove demand. Demand must be confirmed through adjacent searches, review counts on related titles, and BSR patterns in the broader niche.

---

## THIN EVIDENCE Guard

If fewer than 3 search phrases were actually searched and recorded in the intake file, the scorecard is considered thin evidence. Rules:
- Header gets a `⚠ THIN EVIDENCE` stamp
- Suggested AI total is capped at 79/100 (Revise tier)
- `/niche-research` notes the cap in the scoring table
- Elise can override the cap if she confirms the research is sufficient

---

## Single Source of Truth

`research/gate_7_niche_shortlist.md` is the master tracker. It is the single source of truth for:
- Which niches exist
- Their canonical IDs
- Suggested AI scores
- Elise confirmed scores
- Research status and decisions

Every scorecard update must have a corresponding tracker row update. AI cannot write Elise Final scores or change decisions in the tracker — only `/niche-signoff` can do that.

---

## Command Reference

| Command | What it does |
|---|---|
| `/niche-research <intake-file>` | Structures Elise's raw intake into scorecard + competitor analysis, suggests scores, updates tracker (Suggested only), flags IP, holds for review |
| `/niche-signoff <niche_id>` | Human-gate sign-off: Elise reviews suggestions, AI writes Elise Final scores + decision, updates tracker to Signed |
| `/gate7-status` | Read-only audit: prints current state of all scorecards, tracker rows, and unsigned gaps |

---

## Invariants (Hard Rules)

1. AI never writes Elise Final scores — only suggests
2. AI never advances a niche from "Scored (suggested)" to "Signed" without `/niche-signoff`
3. AI never creates a new niche_id for an existing niche — update in place
4. AI never accesses Amazon — all data is Elise's manual observations
5. AI never guarantees Amazon ranking, approval, or sales
6. Any IP flag found during research → add/update row in `ip_watchlist.md` in same commit
7. Tracker row must be updated in the same operation as the scorecard
8. THIN EVIDENCE (< 3 phrases) caps the suggested score — cannot suggest Pursue

---

*Ref: `CLAUDE.md` | `docs/niche_research_framework.md` | `research/manual_amazon_research_instructions.md` | `research/gate_7_niche_shortlist.md` | `research/ip_watchlist.md`*
