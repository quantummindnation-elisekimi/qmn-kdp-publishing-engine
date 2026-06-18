# KDP Workflow — QMN KDP Publishing Engine

*End-to-end reference for producing and publishing a children's book through this system.*

---

## Overview

Each book passes through 15 phases from niche research to post-launch case study. No phase may be skipped. Human approval gates are marked with **[GATE]**.

---

## Phase 1: Market and Niche Research

**Objective:** Identify high-demand, low-competition children's book themes aligned with QMN values.

**Inputs:**
- Elise's knowledge of parent/child emotional pain points
- `research/keyword_seeds.md`
- `prompts/01_niche_research_prompt.md`
- `templates/niche_research_template.md`

**Outputs:**
- `research/[niche-name]/competitor_observations.md`
- `research/[niche-name]/review_mining_notes.md`
- `research/market_gap_notes.md`

**Method:**
- Elise manually searches Amazon.com for keyword seeds
- Observes top titles, BSRs, cover styles, pricing, review counts
- Records observations manually — no scraping tools, no Amazon ToS violations
- Uses the AI prompt to help structure and analyze observations

**[GATE]** Elise approves shortlist of 3–5 niche candidates before Phase 3.

---

## Phase 2: Competitor Validation

**Objective:** Understand competitor quality and identify genuine market gaps.

**Inputs:**
- `research/[niche-name]/competitor_observations.md`
- `prompts/02_book_concept_prompt.md` (competitor section)

**Outputs:**
- Updated competitor observations
- `research/[niche-name]/review_mining_notes.md` (completed)

**Method:**
- Read 10–20 real reviews for top 3–5 competitors in each niche
- Extract: what parents praise, what they wish was different, recurring language, unmet needs
- Identify if competitor books are low-quality, visually poor, or poorly differentiated

**Risk check:** Ensure no competitor concept is being copied.

---

## Phase 3: Niche Scoring

**Objective:** Apply the 100-point scoring framework to select the best niche.

**Inputs:**
- Completed research and review mining files
- `docs/niche_research_framework.md`

**Outputs:**
- `research/scoring/[niche-name]_score.md`

**Method:**
- Score each candidate across 10 dimensions (see `docs/niche_research_framework.md`)
- Only niches scoring 60+ are considered viable
- Niches below 60 are parked, not discarded

**[GATE]** Elise approves the winning niche before Phase 4.

---

## Phase 4: Book Concept and Positioning

**Objective:** Define the unique angle, audience, emotional hook, and QMN brand fit.

**Inputs:**
- Approved niche score
- `templates/book_brief_template.md`
- `prompts/02_book_concept_prompt.md`

**Outputs:**
- `books/[book-id]/02_book_brief.md`

**Risk check:** Concept must not resemble any known trademarked story world or franchise.

**[GATE]** Elise approves the book brief before Phase 5.

---

## Phase 5: Character Bible

**Objective:** Create original, ownable characters — names, appearances, personalities, story roles.

**Inputs:**
- Approved book brief
- `templates/character_bible_template.md`
- `prompts/03_character_bible_prompt.md`

**Outputs:**
- `books/[book-id]/03_character_bible.md`

**Risk check:**
- Character name must be searched on USPTO trademark database and Amazon before finalizing
- No resemblance to known Disney/Nickelodeon/PBS/streaming characters
- No borrowed visual traits from existing franchises

**[GATE]** Elise approves all character names and visual descriptions before Phase 6.

---

## Phase 6: Manuscript Draft

**Objective:** AI-assisted first draft of the full picture book manuscript.

**Inputs:**
- Approved character bible and book brief
- `templates/manuscript_template.md`
- `prompts/04_manuscript_prompt.md`

**Outputs:**
- `books/[book-id]/04_manuscript.md` (AI Draft v1)

**Risk check:**
- No lifted phrases from known books
- No brand names in text
- No rhyme schemes that copy protected works

---

## Phase 7: Human Edit and Value Review

**Objective:** Elise reads, edits, and approves the manuscript.

**Inputs:**
- AI Draft v1 manuscript

**Outputs:**
- `books/[book-id]/04_manuscript.md` (Human-Edited v1)

**Required:**
- Elise reads the full manuscript aloud — this is the real test for children's books
- Story arc, pacing, language level, and emotional resonance all require human judgment
- Activity pages (if included) reviewed for age-appropriateness

**[GATE]** Elise signs off on Human-Edited v1 before Phase 8. This gate is hard. No exceptions.

---

## Phase 8: Illustration Prompt Planning

**Objective:** Write safe, specific, original illustration prompts for every page spread.

**Inputs:**
- Approved final manuscript
- `templates/illustration_prompt_template.md`
- `prompts/05_illustration_prompt.md`

**Outputs:**
- `books/[book-id]/05_illustration_prompts.md`

**Risk check:**
- Zero artist or studio style references in any prompt
- Every prompt describes a completely original visual scene

**[GATE]** Elise reviews all prompts before any images are generated.

---

## Phase 9: Canva Layout Planning

**Objective:** Plan page-by-page layout — typography, composition, trim size, bleed.

**Inputs:**
- Approved manuscript and illustration plan
- `templates/canva_notes_template.md`
- `docs/canva_design_rules.md`

**Outputs:**
- `books/[book-id]/06_canva_notes.md`

**Risk check:**
- Canva templates and assets must be identified and license-checked
- Document every Canva element to be used

**[GATE]** Elise approves Canva layout plan before production begins.

---

## Phase 10: Copyright/IP Review

**Objective:** Full pre-publication copyright and IP risk check.

**Inputs:**
- All production files
- `docs/copyright_policy.md`
- `templates/copyright_check_template.md`

**Outputs:**
- `books/[book-id]/09_copyright_check.md` (signed by Elise)

**[GATE — HARD GATE]** Elise personally reviews and signs. No KDP submission without this.

---

## Phase 11: KDP Metadata and Listing

**Objective:** Write the complete Amazon KDP listing.

**Inputs:**
- Approved manuscript and brief
- `templates/kdp_metadata_template.md`
- `prompts/08_kdp_listing_prompt.md`
- `docs/amazon_listing_rules.md`

**Outputs:**
- `books/[book-id]/07_kdp_metadata.md`

**[GATE]** Elise approves full listing before upload.

---

## Phase 12: PDF/Export Readiness

**Objective:** Prepare and validate KDP-spec PDFs.

**Inputs:**
- Finalized Canva files
- KDP print specifications

**Outputs:**
- `exports/[book-id]/interior_draft.pdf`
- `exports/[book-id]/cover_draft.pdf`

**Checks:**
- KDP file validator passes on both files
- Cover thumbnail readable at ~160px width
- Correct trim size, bleed, margins, page count

**[GATE]** Elise reviews exported PDFs before KDP upload.

---

## Phase 13: Launch Plan

**Objective:** Plan the initial launch strategy.

**Inputs:**
- `templates/launch_plan_template.md`

**Outputs:**
- `books/[book-id]/08_launch_plan.md`

**[GATE]** Elise approves before any KDP submission.

---

## Phase 14: Post-Launch Optimization

**Objective:** Observe performance and optimize listing based on real data.

**Inputs:**
- Live KDP dashboard observations (manual)
- Existing metadata file

**Outputs:**
- Updated `books/[book-id]/07_kdp_metadata.md` with optimization notes

**[GATE]** Elise approves any metadata changes before updating the live listing.

---

## Phase 15: QMN/MindQuest Case Study

**Objective:** Document the full journey as a transparent QMN case study.

**Inputs:**
- All book project files
- Post-launch data observations

**Outputs:**
- `case_studies/[book-id]/case_study_draft.md`

**[GATE]** Elise reviews and approves before any public sharing.

---

*This workflow is the operational guide for every book in this repo.*
