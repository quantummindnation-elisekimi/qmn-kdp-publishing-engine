# Prompt 04: Manuscript Draft — QMN KDP Publishing Engine

*Use this prompt to generate the AI first draft of the manuscript after the character bible has been approved.*

---

## When to Use This Prompt

After:
- Character bible approved by Elise
- Book brief approved by Elise
- Proceeding to Phase 6 (Manuscript Draft)

---

## Prompt (Copy and use with Claude)

```
I'm writing a children's picture book manuscript for Amazon KDP under the QMN / MindQuest brand.

This is an AI first draft only. The manuscript will be reviewed, edited, and approved by a human editor before any illustration work begins.

BOOK DETAILS:
- Title (working): [TITLE]
- Subtitle: [SUBTITLE]
- Target audience: [AGE RANGE]
- Word count target: [TARGET — typical picture book: 500–1000 words for ages 4–7]
- Page count: [PAGE COUNT — typically 32 pages]
- Theme: [THEME]

APPROVED EMOTIONAL ARC:
- Opening emotion: [from book brief]
- Complicating emotion (middle): [from book brief]
- Turning point: [from book brief]
- Closing emotion: [from book brief]
- Takeaway for the child: [from book brief]

APPROVED CHARACTERS:
- Main character: [NAME — from approved character bible]
- Supporting character(s): [NAMES AND ROLES]
- Setting: [from approved character bible]

Please draft the manuscript page by page (32 pages total = 16 spreads).

For each spread:
- Label it: "Pages X–Y"
- Write the text that will appear on the page
- Add a brief illustration direction note in [brackets] for the illustrator — describe the scene without artist style references

The text should:
- Be age-appropriate for [AGE RANGE] — short sentences, concrete imagery, clear emotional language
- Flow naturally when read aloud by an adult
- Build the emotional arc across the page spreads
- Avoid brand names, trademarks, or any known IP references
- Not lift phrases, structures, or rhyme schemes from any protected work

Activity pages (if applicable):
- If [BOOK TITLE] will include [NUMBER] activity pages, please suggest what those pages could contain — age-appropriate journaling prompts, drawing activities, or parent-child discussion questions related to the theme.

IMPORTANT CONSTRAINTS:
- This is a working draft only. Do not present this as a finished, publish-ready manuscript.
- No artist style references in illustration direction notes.
- No franchise characters, brand names, or trademarked IP in any text.
- Language must be tested for read-aloud flow at human editing stage.
- Mark this output clearly as "AI Draft v1 — Human Edit Required."
```

---

## After Getting the Output

1. Copy the draft into `books/[book-id]/04_manuscript.md` using `templates/manuscript_template.md`
2. Mark the file status as "AI Draft v1"
3. Submit to Elise for the human edit phase (Phase 7)
4. Elise reads the full manuscript aloud before editing begins

**No illustration prompts are written until Elise approves the Human-Edited v1 manuscript.**

---

*Ref: docs/kdp_workflow.md Phases 6–7*
