---
## LANGUAGE & AUDIENCE
- Article language: English (EN-US) by default; spellings, style, citations follow American English.
- Target readers: US & EU consumers; include unit duality when relevant (imperial + metric).
- Cultural/legal awareness: avoid medical claims; add neutral, evidence-based wording; add EU notes when guidance materially differs.
- Readability: short paragraphs (≤50 words), average sentence length ≤20 words; active voice.

## US/EU LOCALIZATION
- When guidance differs (naming, availability, over-the-counter vs prescription, dosage ranges), add a short callout note "US vs EU".
- Use dual units (mg / IU; lb & kg; oz & ml) where appropriate.

## COMPETITIVE GAP PASS (before writing sections)
- Do a SERP-top review (non-clickbait) for the focus topic: identify 5–10 common subtopics competitors cover AND 5–10 gaps they miss (data points, comparisons, FAQs, contraindications, dosage clarity, side-effects, who-shouldn't-use, timelines, costs).
- Ensure the outline includes the missing angles ("information gain") and merges overlapping headings to avoid redundancy.
- Require ONE compact comparison element (table 2–6 rows or checklist) where readers must decide among options.
- Add an "At-a-glance" block (bullets: who it helps / who should avoid / quick steps / expected timeline).
- Deliverable: /runs/<DATE>-<SLUG>/gap_analysis.md (list of covered vs. added gaps).

## SMART HOOKS & CTA
- H1 Hook: under H1, insert a 40–60 word "answer-first" hook highlighting outcome, timeframe, and a safety caveat.
- Title/Meta A/B: generate 2–3 variants for SEO Title (≤60 chars) & Meta Description (150 chars) with a single benefit + number or timeframe (no year stuffing).
- CTA Strategy:
  * Top CTA: soft, value-first (guide/quiz/checklist).
  * Mid CTA: problem–agitate–solve microcopy + product benefit bullets (≤4) + affiliate link (rel="sponsored noopener").
  * End CTA: recap value + risk reversal (refund policy if available) + one-liner credibility (author/reviewer).
- Objection handling microcopy: add a short "Still unsure?" block linking to a neutral evidence section or FAQ.

## COMPLETENESS RULES (per section)
- Each section must answer: What is it? Who is it for/not for? How to use? Expected timeline? Risks/contraindications? Alternatives?
- If the claim has uncertainty or conflicting evidence: include a one-sentence nuance note with source (Org/Year).
- Add 1 mini-FAQ (JSON-LD fragment) that addresses a likely follow-up from AI/SGE or readers.
---

# SEO Codex Master Protocol

The SEO Codex Master Protocol defines the end-to-end workflow for creating, optimizing, and publishing SEO-ready long-form content. Every project must be organized under the `/codex` workspace and executed sequentially through Tasks A–F. Supporting assets reside in `/codex/assets`, configuration defaults live in `/codex/config`, structured data and research inputs are stored in `/codex/data`, and execution logs are captured in `/runs`.

## Workflow Overview
1. **Strategy Alignment** – Confirm campaign goals, brand voice, target audience, and success metrics using the input templates in `/codex/config/input_templates`.
2. **Research & Outline** – Perform keyword research, SERP analysis, and topical mapping before drafting a section-level outline.
3. **Production & Optimization** – Generate draft copy using the Scholar Hybrid, Writing Assistant, FAQ, and Grammar prompts located in `/codex/assets/`. Apply CTA blocks, JSON-LD schemas, and the RankMath checklist to reinforce SEO compliance.
4. **Quality Assurance** – Validate structure, on-page optimizations, factual accuracy, and readiness for publication via Tasks E and F.

## Required Artifacts per Article
- **Brief Package** – Completed `article_brief_template.md` and `client_intake_form.yaml` files.
- **Research Data** – Keyword CSVs, SERP notes, and competitor snapshots saved within `/codex/data`.
- **Draft Materials** – Prompt outputs, outline documents, and final manuscript stored under `/codex/tasks/<article-name>/` (create per engagement as needed).
- **Run Log** – Update `/runs/SETUP_LOG.md` with major decisions, validations, and publishing timestamps.

## Task Navigation
Refer to the task playbooks located in `/codex/tasks/` to execute each phase. Every task includes prerequisites, actions, and completion criteria to standardize delivery quality.

> **Reminder:** Keep all assets version-controlled. Commit changes frequently and maintain transparency within the run logs for reproducibility.
