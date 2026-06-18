# QMN KDP Publishing Engine

A human-directed, AI-assisted system for researching, creating, and publishing original children's books under the **QMN / MindQuest** brand on Amazon KDP.

---

## What This Is

This repo is the operational engine behind QMN's children's book publishing initiative. It is not a mass content generator. Every book produced through this system requires human research, human direction, human editing, and human approval before it gets anywhere near Amazon.

AI assists with drafting, research structuring, and prompt generation. Humans decide everything that matters.

---

## How This Repo Is Organized

```
qmn-kdp-publishing-engine/
├── CLAUDE.md                    # AI instructions and policy guardrails
├── README.md                    # This file
├── .gitignore
├── docs/                        # Reference policies and frameworks
├── templates/                   # Reusable blank document forms
├── prompts/                     # Curated AI prompt scripts per phase
├── research/                    # Niche research notes and scorecards
│   └── scoring/                 # Niche score files
├── books/                       # One subfolder per book project
│   ├── _template_book_project/  # Blank template for new book projects
│   └── 001_the_little_brave_brain/  # Sample Book 001 (DRAFT ONLY)
├── assets/                      # Covers, illustrations, brand kit notes
├── exports/                     # KDP-ready PDFs (only after Elise approval)
└── case_studies/                # Post-launch documentation per book
```

---

## Publishing Workflow (15 Phases)

| Phase | Name |
|---|---|
| 1 | Market and niche research |
| 2 | Competitor validation |
| 3 | Niche scoring |
| 4 | Book concept and positioning |
| 5 | Character bible |
| 6 | Manuscript draft |
| 7 | Human edit and child/parent value review |
| 8 | Illustration prompt planning |
| 9 | Canva layout planning |
| 10 | Copyright/IP review |
| 11 | KDP metadata and listing optimization |
| 12 | PDF/export readiness |
| 13 | Launch plan |
| 14 | Post-launch optimization |
| 15 | QMN/MindQuest case study documentation |

Full workflow detail: `docs/kdp_workflow.md`

---

## Policy Summary

- No copyrighted characters, brands, mascots, or celebrity names
- No artist style references in illustration prompts
- No guaranteed sales or Amazon approval claims
- AI disclosure required for all KDP submissions using AI-assisted content
- Every manuscript must be human-read and human-edited before illustration work
- Every book requires `09_copyright_check.md` signed by Elise before KDP submission
- Canva is a layout tool only — not the source of original IP
- All Canva assets used must be documented with license type

Full policy: `docs/copyright_policy.md` | `docs/ai_disclosure_policy.md` | `docs/canva_design_rules.md`

---

## Approval Gates

No phase proceeds without Elise sign-off. See `docs/human_review_sop.md` for the full gate process.

---

## Brand

**QMN / MindQuest** — children's emotional intelligence, mindset, courage, and growth.

Every book in this system must align with those values. This is not a vanity publishing project. It is a real product line with real children and real parents as the audience.

---

*Owner: Elise Kimi / QMN | Repo initialized: 2026-06-18*
