<!-- Variables -->
FOCUS_KW: 
SECONDARIES: 
SECTION_TITLE: 
SOURCES: [SRC1, SRC2, SRC3]
PRODUCT_NAME: 
AFFILIATE_URL: 
INTERNAL_1: 
INTERNAL_2: 
INTERNAL_3: 
SECTION_ANCHOR: 
IMAGE_URL_OR_PLACEHOLDER: 

---

<!-- Prompt: publish-ready section -->

**ROLE**: Senior medical SEO writer (GEO-first, narrative). Produce ONE publish-ready SECTION (English) for WordPress.

**CONTEXT**:
- **FOCUS KW**: `FOCUS_KW`
- **SECONDARIES**: `SECONDARIES`
- **SECTION TITLE** (statement or question from Scholar): `SECTION_TITLE`
- **SOURCES**: USE ONLY `SOURCES`
- **INTERNAL LINKS**: choose ONE: `INTERNAL_1`, `INTERNAL_2`, `INTERNAL_3`
- **AFFILIATE**: name=`PRODUCT_NAME`, url=`AFFILIATE_URL` (rel=sponsored noopener…)

**OUTPUT**: return EXACTLY this pack:

**1︎⃣ — SECTION HTML**
```html
<!-- SECTION -->
<section id="SECTION_ANCHOR">
  <h2>SECTION_TITLE</h2>
  <p class="snippet"><strong>Answer</strong>: DIRECT 45–60 word summary with 1 key caution if relevant.</p>
  <p>Intro bridge (1–2 sentences)</p>
  <p>Body (500–700 words) with inline cites like (NIH, 2022) (PubMed, 2019). Short paragraphs (≤50 words).</p>
  <ul>
    <li><strong>Key point</strong>: … (Examine, 2023)</li>
    <li>…</li>
  </ul>
  <table class="stack">
    <thead><tr><th>Item</th><th>Why it matters</th><th>Source</th></tr></thead>
    <tbody>
      <tr><td data-label="Item">Standard dose</td><td data-label="Why it matters">…</td><td data-label="Source">NIH, 2022</td></tr>
    </tbody>
  </table>
  <p>See also <a href="INTERNAL_LINK_SLUG" rel="noopener">related guide</a>.</p>
  <figure>
    <img src="IMAGE_URL_OR_PLACEHOLDER" alt="FOCUS_KW + descriptive" width="1200" height="675" loading="lazy" />
    <figcaption>FOCUS_KW quick visual</figcaption>
  </figure>
  <div class="cta-box"><strong>On-demand support</strong>: Try <a href="AFFILIATE_URL" rel="sponsored noopener">PRODUCT_NAME</a> to reinforce your 30-day plan.</div>
</section>
```

**2︎⃣ — JSON-LD fragment**
```html
<!-- JSON-LD fragment -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@graph": [{
    "@type": "FAQPage",
    "@id": "CANONICAL_URL#faq-SECTION_ANCHOR",
    "mainEntity": [{
      "@type": "Question",
      "name": "SECTION_TITLE as a natural question (or rephrased)",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Rephrase the snippet as a neutral answer (Org/Year)."
      }
    }]
  }]
}
</script>
```

**3︎⃣ — RANKMATH PROTOCOL CHECK**
- Focus KW density 1.0% (never >1.5%); include once in the snippet and early in body.
- Paragraphs ≤50 words; include a list + add a compact table if it adds clarity.
- 1 contextual internal link placeholder used.
- Affiliate links use `rel="sponsored noopener"`.
- If any claim lacks a provided source, append `<!-- CHECK SOURCE -->`.

**RESTRICTIONS**:
English only. Use ONLY the given sources. If sources insufficient, output:
`MORE SOURCES NEEDED FOR: SECTION_TITLE`
