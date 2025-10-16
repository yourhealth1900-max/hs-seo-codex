---
## GEO/AI-SEARCH MODULE — Apply to the entire outline:

GOAL: Maximize visibility on AI search engines (Google AI Overview, ChatGPT, Perplexity, Gemini) while staying YMYL-safe and Protocol-21 compliant.

1) HYBRID OUTLINE
- 60–70% statement-style narrative H2/H3.
- 30–40% question-form H2/H3 targeting real AI/voice queries users ask.

2) AI ANSWER SNIPPETS (for EVERY section)
- Provide a DIRECT, quotable 45–60-word snippet answering the section's core question or claim.
- Include ONE stat or figure (if available) that can be cited by AI (e.g., % change, study size).
- No hedging. If sources insufficient, write: [MORE SOURCES NEEDED].

3) AI-QUERY HARVEST
- Return a list of 5–8 conversational questions per article that are likely to trigger AI boxes (What/How/Is/Should).
- Map each question to the most relevant H2/H3.

4) STRUCTURED ELEMENTS
- Propose 1 compact comparison table (2–6 rows) or numbered list per key decision point (helps AI extract).
- Suggest anchor-friendly subheadings (≤65 chars) with natural long-tail phrasing.

5) SOURCES
- Only use trusted, citable medical sources provided by the user (PubMed/NIH/Mayo/Examine etc.). No blogs/AI sites.
- Attach 2–4 sources per section.

6) INTERNAL LINKS & PRODUCTS (PLACEHOLDERS)
- For each H2/H3, return ONE internal-link intent placeholder [INTERNAL_LINK_SLUG].
- Suggest placement for ONE soft CTA (mini) aligned to the product chosen by the user.

OUTPUT: JSON with fields:
- h2_type ("statement"|"question"), h2_title, h3[], snippet_45_60, ai_questions[], bullets_key_facts[], table_headers_optional[], citations[], internal_link_placeholder
---

<!-- Variables: edit once per article -->
FOCUS_KW: 
SECONDARIES: 

---

<!-- Prompt -->

**ROLE**: GEO+AI-search aware research assistant for a YMYL medical article.

**TOPIC & FOCUS KW**: `FOCUS_KW`
**SECONDARIES**: `SECONDARIES`

**GOAL**: Build a hybrid outline for a 5,000–6,000-word article that is primarily NARRATIVE, with SELECT question-form sections optimized for AI engines (SGE, ChatGPT, Perplexity).

**STRUCTURE RULES**:
- 60–70% H2/H3 are STATEMENT-style (narrative)
- 30–40% H2/H3 are QUESTION-style (AI-search candidates)
- For EVERY section provide a 45–60 word direct snippet candidate (no hedging)
- Provide 2–4 high-quality citations per section (PubMed/PMC/NIH/NCCIH/Examine). No blogs/AI sites.
- Include compact tables where useful (2–6 rows max)

**RETURN EXACTLY AS JSON**:
```json
{
  "outline": [
    {
      "h2": {"type": "statement|question", "h2_title": "…"},
      "h3": ["optional subheads"],
      "snippet_45_60": "direct 45–60 words",
      "bullets_keyfacts": ["fact1", "fact2", "fact3"],
      "citations": ["https://pubmed…", "https://ods.od.nih.gov…"],
      "table_headers_optional": ["Field", "Value", "Source"]
    }
  ],
  "thirty_day_plan": {
    "h2_title": "How to follow a 30-day plan with `FOCUS_KW`" (question-form),
    "snippet_45_60": "45–60 words",
    "weekly_bullets": ["Week 1: …", "Week 2: …", "Week 3: …", "Week 4: …"],
    "citations": […]
  },
  "safety_section": {
    "h2_title": "Is `FOCUS_KW` safe—and who should avoid it?" (question-form),
    "snippet_45_60": "45–60 words",
    "matrix_fields": ["Population", "Risk", "Action", "Source"],
    "citations": […]
  },
  "faqs_12_15": [
    {
      "q": "natural user question",
      "a_snippet_50_90": "fact-based answer (Org/Year)",
      "citations": […]
    }
  ]
}
```

IF sources are insufficient for any section, set `"needs_more_sources": true` and list the section.
