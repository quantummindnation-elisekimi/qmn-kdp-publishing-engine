# Prompt 01: Niche Research — QMN KDP Publishing Engine

*Use this prompt to structure and analyze niche research observations after Elise has completed manual Amazon research.*

---

## When to Use This Prompt

After Elise has:
1. Manually searched Amazon.com for keyword seeds
2. Noted top titles, BSRs, cover quality, pricing, and review counts
3. Read 10–20 reviews across top competitors in a candidate niche

Use this prompt to help organize observations into a structured analysis and identify market gaps.

---

## Prompt (Copy and use with Claude)

```
I'm doing niche research for an original children's picture book to be published on Amazon KDP under the QMN / MindQuest brand.

I've manually observed the following on Amazon for the niche: [NICHE THEME].

My keyword seed: [KEYWORD]

Competitor titles I observed:
[List titles, BSRs, prices, review counts — Elise fills this in from manual research]

Review patterns I noticed:
[Paste key review excerpts or summarize what parents said — Elise fills in from manual reading]

Based on this, please help me:

1. Identify the most specific parent pain point this niche addresses.
2. Summarize what competitor books do well and what they are missing.
3. Identify 2–3 potential market gaps — what is underserved in this niche?
4. Flag any copyright or IP risks I should check in this niche (known characters, trademarked concepts, etc.).
5. Suggest 3–5 angle variations QMN could take to differentiate in this niche.

IMPORTANT CONSTRAINTS:
- Do not suggest copying or referencing any existing book title, character, or concept.
- Do not reference any artist style in visual suggestions.
- Do not suggest anything that involves Disney, Pixar, Nickelodeon, PBS, Sesame Street, or similar franchise characters.
- All suggestions must be original and ownable by QMN.
- Do not guarantee sales or Amazon ranking for any suggestion.
```

---

## Output to Save

After using this prompt, save the AI response in:
- `research/[niche-name]/competitor_observations.md`
- `research/[niche-name]/review_mining_notes.md`

Then complete the niche score in `research/scoring/[niche-name]_score.md` using `docs/niche_research_framework.md`.

---

*Ref: docs/kdp_workflow.md Phases 1–2*
