# Task A – Strategy & Keyword Research

## Objective
Establish the strategic foundation for the article, align with stakeholder goals, and surface priority keywords.

## Prerequisites
- Completed `client_intake_form.yaml` and `article_brief_template.md` in `/codex/config/input_templates/`.
- Access to up-to-date analytics and keyword tools.

## Inputs Needed
- LANGUAGE: English (EN-US). Target: US & EU readers.
- MARKETING: Include smart hook under H1 and Top/Mid/End CTAs.
- COMPETITION: Run Competitive Gap Pass and include added_gaps in `outline.json`.
- COMPLETENESS: Cover who/when/how/risks/alternatives in relevant sections.

## Actions
1. Review campaign objectives, target personas, and success KPIs.
2. Conduct primary keyword research (seed, supporting, and long-tail variants).
3. Capture SERP intent, competing URLs, and content gaps.
4. Store research findings in `/codex/data/keyword_research/` using the provided CSV template.

## Competitive Gap Pass
- Append to `outline.json`: fields `{covered_competitors[], added_gaps[], at_a_glance_bullets[]}`.
- Save `gap_analysis.md` alongside `outline.json`.

## Outputs
- `keyword_research_summary.md`
- `primary_keyword_list.csv`

## Quality Checks
- Keywords meet intent and volume thresholds agreed upon with stakeholders.
- SERP review identifies at least three competitive differentiators.
- Research artifacts saved with ISO timestamps.
