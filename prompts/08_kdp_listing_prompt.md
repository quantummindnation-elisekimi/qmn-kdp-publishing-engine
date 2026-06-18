# Prompt 08: KDP Listing — QMN KDP Publishing Engine

*Use this prompt to draft the Amazon KDP listing metadata.*

---

## When to Use This Prompt

After:
- Manuscript approved by Elise
- Copyright check signed by Elise
- Proceeding to Phase 11 (KDP Metadata and Listing)

---

## Prompt (Copy and use with Claude)

```
I'm writing the Amazon KDP listing for a children's picture book under the QMN / MindQuest brand.

BOOK DETAILS:
- Title: [TITLE]
- Subtitle: [SUBTITLE]
- Target audience: Ages [RANGE]
- Theme and emotional arc: [BRIEF SUMMARY]
- What problem this book solves for parents: [SPECIFIC PAIN POINT — from research]
- Keywords parents use to describe this pain point: [FROM REVIEW MINING NOTES]
- Competitor gap this book fills: [FROM BOOK BRIEF]
- Format: [PAGE COUNT]-page picture book
- Series (if applicable): [SERIES NAME AND POSITION]

Please help me draft:

1. BOOK DESCRIPTION (400 words max)
   Use this structure:
   - Hook (1–2 sentences): Speak to the parent's specific pain point using their language
   - Story summary (2–3 sentences): What happens, what the child learns
   - Value statement (1–2 sentences): What parent and child experience together
   - Series/brand note (1 sentence): QMN/MindQuest positioning
   - Call to action: "Scroll up and grab your copy today."

2. BACKEND KEYWORDS (7 fields, each up to 50 characters)
   - Do not repeat words that appear in the title or subtitle
   - Use phrases parents actually type in Amazon search
   - Focus on longer-tail, specific phrases
   - Do not include competitor names, author names, or restricted terms

3. CATEGORY SUGGESTIONS
   - Suggest 2 categories (full Amazon path)
   - Explain why each is appropriate
   - Note: Elise will verify current category BSR competitiveness before selecting

4. TITLE ORIGINALITY NOTE
   - Flag if the proposed title sounds similar to any well-known existing children's book titles
   - Elise will search the exact title on Amazon before finalizing

IMPORTANT CONSTRAINTS:
- Do not claim this book is "#1," "bestselling," or "award-winning" unless verified.
- Do not guarantee sales, ranking, or reader outcomes.
- Do not make false claims about what the book will do for a child.
- The description must serve the parent's search intent — not just describe the plot.
- All backend keywords must be genuinely relevant — no keyword stuffing.
- This is a draft for Elise's review. She approves the listing before submission.
```

---

## After Getting the Output

1. Complete `books/[book-id]/07_kdp_metadata.md` using `templates/kdp_metadata_template.md`
2. Elise validates keyword demand manually on Amazon before finalizing
3. Elise searches the exact title on Amazon Books — confirm no exact match
4. Elise approves the full listing before upload

---

*Ref: docs/amazon_listing_rules.md | docs/kdp_workflow.md Phase 11*
