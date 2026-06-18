# Human Review Standard Operating Procedure — QMN KDP Publishing Engine

*This SOP defines when and how Elise reviews and approves each phase of book production.*

---

## Why Human Review Is Non-Negotiable

AI makes this process faster. Human judgment makes this process good.

- AI cannot assess whether a book will genuinely help a child
- AI cannot verify whether a character is emotionally resonant for a 5-year-old
- AI cannot confirm that an illustration concept is truly original
- AI cannot take legal responsibility for copyright or trademark issues
- AI cannot make brand decisions for QMN/MindQuest

Elise owns the judgment. AI does the drafting.

---

## Approval Gate Summary

| Gate | What Is Being Approved | Required Action |
|---|---|---|
| Gate 1 | Overall architecture | Review `CLAUDE.md` + `README.md`, confirm structure |
| Gate 2 | Repo structure before first commit | Review full file tree |
| Gate 3 | File list in first commit | Review each file before committing |
| Gate 4 | Migration vs rebuild method | Confirm approach |
| Gate 5 | Initial commit pushed to new repo | Confirm GitHub shows correct files |
| Gate 6 | Cleanup of any accidental files in other repos | Explicitly authorize specific delete commands |
| Gate 7 | Book 001 niche, concept, and character direction | Review `01_research.md`, `02_book_brief.md`, `03_character_bible.md` |
| Gate 8 | Any KDP submission | Review all 10 book files + PDFs + copyright check |

---

## Per-Phase Review Checklist

### Phase 1–3: Research and Niche Scoring

**Elise reviews:**
- [ ] Keyword seed list makes sense for QMN brand
- [ ] Competitor observations were gathered manually from Amazon (not scraped)
- [ ] Niche score was applied using the framework in `docs/niche_research_framework.md`
- [ ] Niche score is 60+ before moving to book concept work
- [ ] No copyright-risk themes flagged in the niche

**Approval action:** Elise writes "Niche approved: [niche name], Score: [X/100]" in `01_research.md` and dates it.

---

### Phase 4: Book Concept and Brief

**Elise reviews:**
- [ ] The emotional hook is specific and real (not generic)
- [ ] The concept does not resemble a known trademarked story world
- [ ] The QMN/MindQuest brand fit is genuine
- [ ] Series potential is identified if relevant
- [ ] Differentiator from existing books is clearly stated

**Approval action:** Elise writes "Book brief approved" in `02_book_brief.md` and dates it.

---

### Phase 5: Character Bible

**Elise reviews:**
- [ ] Character name has been searched for trademark risk
- [ ] Character appearance is original (no resemblance to known characters)
- [ ] Character personality feels authentic and useful for the theme
- [ ] Supporting characters are appropriate and original
- [ ] No references to known brands, shows, or trademarked franchises

**Approval action:** Elise writes "Character bible approved" in `03_character_bible.md` and dates it.

---

### Phase 6–7: Manuscript Draft and Human Edit

**Elise reviews and edits:**
- [ ] Elise reads the full manuscript aloud (read-aloud test is essential for children's books)
- [ ] The story arc works for the target age group
- [ ] Language is age-appropriate (short sentences, concrete imagery, emotional clarity)
- [ ] No brand names, trademarks, or IP risks in the text
- [ ] No lifted phrases from known books
- [ ] The story solves a real child/parent need — not just a generic AI filler theme
- [ ] Activity pages (if included) are age-appropriate and genuinely useful

**Approval action:** Elise marks the manuscript file with "Human-Edited v1 — Approved by Elise [date]" at the top.

---

### Phase 8: Illustration Prompts

**Elise reviews:**
- [ ] Every prompt describes an original visual scene
- [ ] No artist names or studio names in any prompt
- [ ] Character descriptions match the approved character bible
- [ ] No trademarked visual concepts
- [ ] Color palette and mood direction are appropriate for the story

**Approval action:** Elise writes "Illustration prompts approved" in `05_illustration_prompts.md` and dates it.

---

### Phase 9: Canva Layout Notes

**Elise reviews:**
- [ ] Trim size is correct for KDP
- [ ] Bleed is planned correctly
- [ ] Font choices match QMN Brand Kit or are approved fonts
- [ ] Text placement is readable for the target age group
- [ ] Any Canva template or element to be used is identified and license confirmed

**Approval action:** Elise writes "Canva notes approved" in `06_canva_notes.md` and dates it.

---

### Phase 10: Copyright/IP Review

**Elise personally completes:**
- [ ] Character name search (USPTO + Amazon + Google)
- [ ] Title search (Amazon + Google Books)
- [ ] Illustration concept review
- [ ] AI disclosure status confirmed
- [ ] Canva asset license confirmed

**Approval action:** Elise writes "Copyright check signed off — Elise [date]" in `09_copyright_check.md`.

*This gate cannot be delegated to AI. Elise must personally verify and sign.*

---

### Phase 11: KDP Metadata

**Elise reviews:**
- [ ] Title and subtitle are original and do not exactly match existing Amazon titles
- [ ] Description follows approved structure and makes no false claims
- [ ] Backend keywords are relevant and do not violate KDP keyword policies
- [ ] Categories are appropriate
- [ ] AI disclosure selection is documented
- [ ] No guaranteed sales or ranking claims in any text

**Approval action:** Elise writes "KDP metadata approved" in `07_kdp_metadata.md` and dates it.

---

### Phase 12: PDF Export Review

**Elise reviews:**
- [ ] Interior PDF passes KDP file validator without errors
- [ ] Cover PDF passes KDP file validator without errors
- [ ] Cover thumbnail is readable at small size (test at approximately 160px width)
- [ ] Interior margins are correct
- [ ] Page count is correct and even (for print)

**Approval action:** Elise writes "PDFs approved for upload" in `10_final_checklist.md` and dates it.

---

### Gate 8 Final Sign-Off

**Before clicking Publish on KDP, Elise confirms:**
- [ ] All 10 book files are complete and individually approved
- [ ] Copyright check is signed
- [ ] PDFs are validated
- [ ] AI disclosure is prepared
- [ ] QMN Brand Kit is applied consistently
- [ ] Book meets QMN quality standard (not generic AI content)

**This is the final gate. Nothing is submitted to KDP without this sign-off.**

---

*This SOP must be followed for every book in this repo. Skipping a gate is not an option.*
