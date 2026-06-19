# Manual Amazon Research Instructions — QMN KDP Niche Research

**For Elise's use during Gate 7 niche validation.**

*All Amazon research must be conducted manually by Elise. No scraping tools. No automated extraction. No third-party Amazon data services. Personal observation on Amazon.com is the only compliant method.*

---

## Why Manual Research

Amazon's Conditions of Use prohibit scraping or automated data extraction. Beyond compliance, manual research produces better insights: you see what real parents see when they search, how covers look at thumbnail size, what language is used in titles, and what reviewers actually say.

Time estimate per niche: **30–45 minutes of focused manual research.**

---

## What Is Automated vs Manual (Important Distinction)

The "no automation" rule on this project applies to **data collection only**. It does not
forbid downstream processing of data Elise has already gathered by hand.

**Manual only — never automated:**
- Searching Amazon, reading listings, reading reviews, observing BSR
- Any extraction of data from Amazon (no scraping, no third-party Amazon data services or APIs)

**Automation allowed — only after manual collection:**
- Structuring Elise's raw observations into the scorecard format
- Drafting the competitor analysis and market-gap synthesis
- *Suggesting* (never finalizing) the 100-point scores, with rationale tied to the framework
- The `/niche-research` slash command performs only this downstream work — it never touches Amazon

Elise's manual observation remains the only source of Amazon data. Claude never accesses Amazon
directly. Final scores and sign-off remain human.

---

## Step 1: Set Up Your Research Session

1. Open Amazon.com on a browser (desktop recommended for easier observation)
2. Navigate to: Books → Children's Books
3. Have the relevant scorecard file open alongside Amazon: `research/scoring/00X_[niche]_score.md`
4. Use a note-taking format you're comfortable with (screenshot + notes, or direct typing into the scorecard)

---

## Step 2: Search Each Keyword Phrase

For each niche, the scorecard lists 5–7 suggested Amazon search phrases. For each phrase:

1. Type the phrase into Amazon's search bar (Books category)
2. Observe the first page of results (top 10–16 titles)
3. Note:
   - How many results appear? (Amazon shows "1–16 of X results")
   - Are there any sponsored ads at the top? (Signal of commercial intent)
   - What do the top titles look like? Are they from big publishers or independent/self-published authors?
   - Are the covers professional or low-quality?

**Record in the scorecard's Competitor Observation Table.**

---

## Step 3: Check BSR (Best Sellers Rank)

For the top 3–5 most relevant titles you find:

1. Click into the book's product page
2. Scroll down to "Product Details"
3. Find the "Best Sellers Rank" — it will look like: `#12,453 in Books` and `#42 in Children's Books > Growing Up & Facts of Life > Emotions & Feelings`
4. Record both numbers

**How to interpret BSR:**
- **#1 – #10,000 in Books:** Very actively selling — strong demand signal
- **#10,000 – #50,000 in Books:** Selling regularly — good demand signal
- **#50,000 – #100,000 in Books:** Selling occasionally — moderate signal
- **Above #100,000:** Selling infrequently — weak demand or stale listing
- **Above #500,000:** Likely not selling meaningfully

*BSR fluctuates daily. One reading is a snapshot, not a guarantee. Record what you see and note the date.*

---

## Step 4: Mine Reviews

For the top 2–3 most relevant competitor titles, read **10–20 real customer reviews**:

1. Click the star rating to go to the reviews section
2. Sort by "Most Recent" and also check "Top reviews"
3. Read the text of the reviews (not just the stars)
4. Record patterns:
   - What specific words do parents use to describe the problem they were solving?
   - What did the child respond to in the book?
   - What do parents wish was different?
   - Are there any unmet needs mentioned ("I wish this book also...")

**Do not copy and paste review text.** Summarize the patterns in your own words. You are looking for insight, not content.

---

## Step 5: Record Cover and Quality Observations

For each top-ranking title you observe:

- Is the cover professional or does it look low-budget?
- Is the title readable at the thumbnail size shown in search results?
- Does the art look original, or does it feel generic?
- Would a parent choose this cover or scroll past it?

This informs your **Competition Weakness** score — if most existing covers are low-quality, there's an opening for a well-produced book.

---

## Step 6: Note the Publisher Type

Look at the author name and publisher for each title:

- **Big publisher** (Penguin, Random House, Scholastic, etc.): Hard to displace from top rankings; indicates validated demand but strong competition
- **Independent / small press / self-published:** More vulnerable to being outcompeted by a higher-quality book

A niche dominated by big publishers is harder to enter. A niche where the top titles are indie-published is a better opportunity.

---

## Step 7: Fill In the Scorecard

After researching each niche:

1. Open `research/scoring/00X_[niche]_score.md`
2. Fill in:
   - Competitor Observation Table (title, BSR, price, reviews, rating, cover quality, publisher type)
   - Review Mining Notes (patterns you observed — in your own words)
   - BSR Observation Notes (healthiest BSR seen, most competitive title)
   - Market Gap Hypothesis (validate or reject the pre-filled hypothesis, or write your own)
3. Score each of the 10 categories (0–10 points each) based on what you found
4. Write your final recommendation: Pursue / Revise / Reject

---

## Step 8: Repeat for All Five Niches

Complete Steps 2–7 for all five niches in `research/gate_7_niche_shortlist.md` before making a final selection.

---

## Forbidden Actions (Policy Reminder)

- Do not scrape Amazon data using any automated tool or service
- Do not copy competitor book titles, subtitles, descriptions, or character names into QMN materials
- Do not reproduce review text verbatim — summarize in your own words
- Do not use any data that violates Amazon's Conditions of Use
- Do not make production decisions (character bible, manuscript, illustration prompts) until a niche is selected and approved

---

## After Research Is Complete

1. Update `research/gate_7_niche_shortlist.md` with scores and decisions for all five niches
2. Select the niche with the strongest score AND best QMN brand fit
3. Sign the Gate 7 approval line in `research/gate_7_niche_shortlist.md`
4. Notify the next session to proceed to Book Brief (Gate 7 complete → Phase 4 begins)

---

*Ref: `docs/niche_research_framework.md` | `docs/kdp_workflow.md` Phases 1–3 | `research/gate_7_niche_shortlist.md`*
