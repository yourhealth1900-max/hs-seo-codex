# Task F – Final QA & Publication Prep

## Objective
Complete final validation, assemble deliverables, and prepare assets for publishing or client handoff.

## Prerequisites
- Approved `draft_v2.md` from Task E.
- Optimization and editorial checklists completed.

## Actions
1. Run a final QA pass referencing `/codex/assets/07_RankMath_Checklist.txt` and CTA placements.
2. Compile final documents: `draft_final.md`, `article_schema.json`, `optimization_report.md`, `editorial_feedback.md`.
3. Generate publication brief including metadata, slug, social copy, and featured image requirements.
4. Update `/runs/SETUP_LOG.md` with final status, date, and outstanding actions.

## Outputs
- `draft_final.md`
- `publication_brief.md`

## Quality Checks
- All deliverables stored in article folder with consistent naming.
- Hand-off package reviewed by project lead.
- Final approval recorded with stakeholder signature or confirmation email reference.

## RANKMATH GATE (Expanded)
- Global: Focus KW density 0.8–1.3% (NEVER >1.5%); appears in the first 10% of the article; one subheading (if natural).
- Per-section: Focus KW or close variant appears early; section density target ≈1.0%.
- Title/Meta: return 3 variants; pick the best; Meta = EXACT 150 chars; both include Focus KW (once).
- Internal Links: 8–15 genuine internal links in final article (placeholders replaced).
- External Evidence: 10–15 trusted citations distributed across body.
- Schema: @graph valid; per-section FAQ fragments merged; Review JSON-LD present for review sections.
- Images: alt + width/height + lazy; feature & infographic metadata logged in `/assets/media_meta.json`.
- Gap Pass: check that every "added gap" from `gap_analysis.md` is reflected in sections.
- Output `report.md` with PASS/FAIL per item and a "What we added beyond competitors" summary.
