# Prompt 05: Illustration Prompts — QMN KDP Publishing Engine

*Use this prompt to create safe, original illustration prompts after the manuscript has been approved.*

---

## When to Use This Prompt

After:
- Manuscript approved by Elise (Human-Edited v1)
- Proceeding to Phase 8 (Illustration Prompt Planning)

---

## Critical Policy Reminder

**Under no circumstances may any illustration prompt contain:**
- Artist names (living or recently deceased)
- Studio names (Disney, Pixar, DreamWorks, etc.)
- Any phrase resembling "in the style of," "similar to," or "inspired by [named illustrator]"
- Visual descriptions that replicate the distinctive look of known franchise characters

All illustration prompts must describe entirely original visual concepts.

---

## Prompt (Copy and use with Claude)

```
I'm creating illustration prompts for a children's picture book for Amazon KDP under the QMN / MindQuest brand.

These prompts will be used as creative briefs for an illustrator (human or AI tool — TBD). They must describe original visual concepts only.

BOOK DETAILS:
- Title: [TITLE]
- Approved character descriptions: [PASTE FROM APPROVED CHARACTER BIBLE]
- Visual style direction: [from approved character bible — no artist references]
- Color palette direction: [from character bible]

For each of the following 16 spreads (Pages 1–2 through Pages 31–32), please create a specific illustration prompt.

The text for each spread is:
[PASTE APPROVED MANUSCRIPT TEXT — spread by spread]

For each spread, write an illustration prompt with:
1. SCENE: What is happening in this moment of the story
2. CHARACTERS: Who is visible, what they are doing, their expression and body language
3. ENVIRONMENT: Where this takes place, key visual elements in the frame
4. MOOD/LIGHTING: Emotional tone, time of day if relevant, warm or cool palette
5. FOCUS: What the reader's eye should land on first
6. COMPOSITION NOTES: How the image relates to the text placement (text left/right/bottom)

IMPORTANT CONSTRAINTS:
- Zero artist names. Zero studio names. No "in the style of" language.
- All scenes must be derived from the approved manuscript — no invented scenes.
- Character descriptions must match the approved character bible exactly.
- No visual elements that could be confused with existing franchise characters, logos, or brand imagery.
- These are creative briefs, not the finished art. Mark each as a working prompt.
- Color palette and style must be consistent across all 16 spreads.
```

---

## After Getting the Output

1. Copy the prompts into `books/[book-id]/05_illustration_prompts.md` using `templates/illustration_prompt_template.md`
2. Manually review every prompt for any artist references — remove all found
3. Submit to Elise for review before any images are generated

**No images are generated until Elise approves the full prompt set.**

---

*Ref: docs/kdp_workflow.md Phase 8 | docs/copyright_policy.md*
