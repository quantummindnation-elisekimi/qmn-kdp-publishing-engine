# CLAUDE.md — QMN KDP Publishing Engine

## Project Identity

This repo belongs to QMN / MindQuest. It is a human-directed, AI-assisted system for researching, creating, and publishing original children's books on Amazon KDP under the MindQuest brand.

**This is not a mass AI book spam system.** AI is an assistant. Every phase requires human direction, editing, and approval before proceeding.

---

## What This Repo Is For

- Niche research and market validation for children's books
- Book concept development, character bible creation, manuscript drafting
- Illustration prompt planning (copyright-safe, original only)
- Canva layout planning (layout tool only, not source of original IP)
- Amazon KDP metadata optimization
- Post-launch case study documentation for QMN/MindQuest

---

## What Claude Can Do in This Repo

- Help draft, edit, and improve any file in the `docs/`, `templates/`, `prompts/`, `research/`, `books/`, or `case_studies/` folders
- Suggest niche research directions based on Elise's manual Amazon observations
- Draft manuscripts, character bibles, illustration prompts, and KDP metadata when asked
- Apply the copyright and policy guardrails documented in this repo
- Flag potential risks (copyright, IP, policy) before they become problems
- Generate scored niche evaluations using the framework in `docs/niche_research_framework.md`

---

## What Claude Must NOT Do Without Elise Approval

- Create, edit, commit, push, or delete any file without explicit instruction
- Proceed from one workflow phase to the next without Elise sign-off
- Submit to Amazon KDP, Canva, or any external platform
- Generate final publish-ready files (all files are drafts until Elise approves)
- Migrate or delete files from any other repository (SweepX_Backtest_v1 must not be touched)
- Skip any approval gate listed below

---

## Absolute Forbidden Actions

Claude must refuse or flag the following without exception:

- Using any Disney, Pixar, DreamWorks, Nickelodeon, PBS, Sesame Street, or similar character names, visual traits, or story concepts
- Using any living artist's name in illustration prompts ("in the style of Eric Carle," "like Dr. Seuss," "in the style of [any living or recently deceased illustrator]")
- Using any famous brand, mascot, celebrity, trademarked IP, or famous character in any book content
- Copying competitor book titles, subtitles, descriptions, or character concepts
- Using Canva "personal use only" elements in a commercially sold book
- Submitting AI-generated content to KDP without completing the AI disclosure step
- Guaranteeing Amazon approval, ranking, or sales anywhere in the codebase or documentation
- Publishing any book without a completed and Elise-signed `09_copyright_check.md`
- Skipping the human edit phase (Phase 7) for any manuscript

---

## Required Approval Gates

| Gate | Requires Approval Before |
|---|---|
| Gate 1 | Architecture finalized |
| Gate 2 | Repo structure created |
| Gate 3 | File list committed |
| Gate 4 | Migration/rebuild method selected |
| Gate 5 | Initial commit pushed to new repo |
| Gate 6 | Any cleanup of SweepX accidental files |
| Gate 7 | Book 001 niche, concept, and character direction |
| Gate 8 | Any KDP submission |

---

## Quality Principles

- Books must solve a real parent/child emotional or educational need — not just fill a generic AI content slot
- Every manuscript must be human-read, human-edited, and human-approved before illustration work begins
- Every character must be original — searched for trademark risk before finalizing
- Every illustration prompt must describe original visual concepts — no artist style references
- Every Canva asset used must be documented with its license type
- Every book must include the KDP AI disclosure if AI was used in production

---

## Repo Policy Reminders

- This repo is private. Do not share book drafts, character bibles, or manuscripts publicly without Elise approval.
- All files in `books/001_the_little_brave_brain/` are marked DRAFT SAMPLE — NOT FINAL / NOT PUBLISH-READY.
- Files in `books/_template_book_project/` are blank instructional templates only — not real book content.
- The `exports/` folder contains PDFs only when Elise has approved the relevant book for export prep.
- The `case_studies/` folder contains documentation only after a book has been published and results observed.

---

## Key Reference Files

| File | Purpose |
|---|---|
| `docs/copyright_policy.md` | What is and is not allowed — copyright and trademark |
| `docs/ai_disclosure_policy.md` | How to handle AI disclosure on KDP |
| `docs/human_review_sop.md` | Standard operating procedure for human review gates |
| `docs/kdp_workflow.md` | End-to-end publishing workflow reference |
| `docs/niche_research_framework.md` | Niche scoring system (100-point framework) |
| `docs/canva_design_rules.md` | Canva usage policy for this project |
| `docs/book_quality_checklist.md` | Pre-publication quality standards |
| `docs/amazon_listing_rules.md` | KDP metadata and listing optimization guide |
| `docs/qmn_case_study_framework.md` | How to document QMN case studies |

---

*Last updated: 2026-06-18 | Owner: Elise Kimi / QMN*
