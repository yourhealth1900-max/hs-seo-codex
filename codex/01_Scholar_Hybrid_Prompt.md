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
