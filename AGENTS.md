# Economic Reports — YouTube Script Workflow

This repo turns economic research reports into business-focused YouTube video scripts, published as Quarto documents in English and Latin American Spanish.

## Repository Layout

```
refs/                        # Source reports (.txt preferred, .pdf fallback)
refs/YT-scripts/             # Tone reference transcripts
reports/                     # Output scripts as .qmd files
  0001-adapting-to-adversity.qmd       # Completed English example
  0001-adapting-to-adversity-ES.qmd    # Completed Spanish example
```

New scripts follow the naming convention `NNNN-report-slug.qmd` and `NNNN-report-slug-ES.qmd`.

---

## Tone Reference Files

Before writing a new script, read these files in `refs/YT-scripts/` to calibrate tone:

- `stateside-podcast.txt` — Journalistic, street-level, documentary feel
- `f9-the-future-of-motorcyles.txt` — Analytical but loose; uses cultural references to structure an argument
- `the-ash-files.txt` — Personal, literary, essay register
- `gary-vee.txt` — Punchy, motivational, pull-quote-dense

The target tone sits between `stateside-podcast.txt` and `f9-the-future-of-motorcyles.txt`: confident and direct, like an NYT Daily episode for a business audience. Not academic. Not preachy. Treats the listener as smart but not a specialist.

---

## Script Prompt Template

Use the following prompt to start a new script. Fill in the bracketed fields.

---

**PROMPT:**

Read the source report at `refs/[FILENAME].txt`. Write a ~10-minute YouTube video script (approximately 1,400–1,600 words of spoken content) from the perspective of businesses operating in or considering [REGION]. Save the English version to `reports/[NNNN-slug].qmd` and the Spanish version to `reports/[NNNN-slug-ES.qmd]`.

**Audience:** Business leaders, CFOs, COOs, and supply chain executives with operations or sourcing relationships in [REGION]. They are not development economists. They are not a CSR audience. Every finding should be translated into an operational implication.

**Frame:** Read the report as a business risk briefing, not a policy document. The through-line is: this risk is already inside your business. The question is whether you've priced it.

**Structure:**
1. **Open** — Start with a direct question that implicates the viewer's business immediately. Do not explain that you are reading the report from a business perspective — let the question make that self-evident. Follow the question with a brief self-introduction: "Hi, I'm Renato Vargas, an economist and independent consultant who has worked with international organizations for almost two decades." Then preview the four or five topics the video will cover, framed as what the viewer will learn, not as a table of contents. Do not frame the open as a scenario or description; frame it as a question.
2. **Section 1: Exposure** — Where is the risk geographically? Translate the report's exposure data into supplier maps, workforce locations, and logistics corridors.
3. **Section 2: The Nature of the Hit** — Distinguish between catastrophic insured events (getting rarer) and chronic uninsured disruption (staying flat or growing). This is the P&L argument.
4. **Section 3: Country-Level Risk Variation** — Use the report's comparative data to show that the country you source from is a risk decision. Frame recovery speed and resilience infrastructure as operational variables.
5. **Section 4: Root Causes and Leverage Points** — What structural factors keep workers and suppliers exposed? What can businesses actually influence (property rights, infrastructure advocacy, governance engagement)?
6. **Close** — Frame adaptation as supply chain resilience, not philanthropy. End with a first-mover argument: companies that do this work now will have a durable operational advantage.

**Pull Quotes:** Include 5–6 pull quotes, marked with ✦, distributed across sections. Each should:
- Work as a standalone tweet or on-screen text overlay
- Sound like something a CFO or COO might actually say or share
- Be punchy and direct, not academic
- Avoid hedging language

**Charts:** Identify 2 figures from the report worth recreating on camera. For each, write:
- What the chart shows
- When in the script to show it (tied to a specific sentence)
- What to highlight or animate at which moment
- A return-to-camera cue
- How to frame it for a business interpretation (not a policy one)

**Production Notes Block:** At the end of the script, include a callout block with chart instructions and pull quote delivery guidance.

---

## Style Rules (apply to all spoken body text)

These apply to everything the host actually says on camera. They do not apply to section headers, stage directions, or callout blocks.

**Write for the broadest possible audience — think honors-program high schooler, not MBA.** If a word would need a footnote in a magazine, find a simpler one. Avoid financial and economic jargon — words like "variance," "hedge," "nexus," "discourse," "paradigm," or even standard econ terms like "inflation," "current account," or "monetary tightening" have plain-language equivalents. Reach for the plain version first every time, even when the jargon term is common in business media. Use jargon only when there is no accurate plain-language substitute, and when you do, let context make the meaning clear without a formal definition.
- Wrong: "It'll show up as variance you can't explain and can't hedge."
- Right: "It'll bleed quietly into your numbers, and there's no insurance policy that covers it."
- Wrong: "Inflation rose to 4.4 percent."
- Right: "Prices, on average, rose faster, climbing 4.4 percent over the year." (Once the idea of "prices rising" is established, later references can shorten to "prices" or "the pace of price increases" rather than reintroducing "inflation.")
- Wrong: "The current account deficit widened."
- Right: "The country bought more from the rest of the world than it sold."

**Do not address the audience directly as "you."** Speak about the audience in the third person — "businesses," "business leaders," "executives," "investors," "companies" — rather than turning the viewer into "you" and "your business." This keeps the tone of a briefing about the world, not a lecture aimed at the viewer. This applies throughout the script, including the open: the direct question should implicate business decision-makers in general, not the viewer specifically.
- Wrong: "Have you priced that into your plan? Your cost base runs through diesel."
- Right: "Have business leaders priced that into their plans? Any company whose cost base runs through diesel is exposed."

**No colons introducing lists or explanations.** Replace with a period and a full sentence.
- Wrong: "Here's the problem: workers don't own their homes."
- Right: "Here's the problem. Workers don't own their homes."

**No em dashes.** Replace with commas, or break into two sentences.
- Wrong: "The disaster — the one that triggers insurance claims — is getting rarer."
- Right: "The disaster, the one that triggers insurance claims, is getting rarer."
- Or: "The disaster is getting rarer. It's the kind that triggers insurance claims."

**No sentence fragments after a period** (unless used deliberately for single-word punchy effect, e.g. "An operational risk."). When a colon or em dash previously introduced a list of fragments, convert each fragment to a full sentence with its own verb.
- Wrong: "Your exposure is the chronic disruption: the harvest below forecast. The worker who misses two weeks."
- Right: "Your exposure is the chronic disruption. It's the harvest that comes in below forecast. It's the worker who misses two weeks."

---

## Fact-Checking Rules

Every specific statistic, percentage, named program, and country example must be traceable to the source report. Before finalizing:

1. For every numerical claim, grep the source `.txt` file to confirm it appears there.
2. For every named study or program, confirm it is cited in the report (not added from general knowledge).
3. If a claim cannot be found in the source, either remove it or replace the specific figure with a general description of what the report shows.
4. Illustrative examples used for rhetorical effect (e.g., "a harvest that comes in well below forecast") are acceptable but must not include specific numbers that are not in the report.

Common failure modes from past work:
- Adding industry names to a geographic corridor based on general knowledge rather than what the report states
- Inventing a percentage for an illustrative example (e.g., "30% below forecast")
- Embellishing a cited study's finding (e.g., "flood defense projects" when the report says "community projects")
- Describing recovery timeframes in specific units (e.g., "months") when the report only shows a trend

---

## Spanish Translation Rules

After the English script is fact-checked and final, produce the Spanish version.

**Register:** Avoid addressing the viewer directly as "tú" or "usted." Following the English-language rule above, speak in the third person about "las empresas," "los líderes empresariales," "los ejecutivos," "los inversionistas" rather than turning the viewer into the addressee. Keep the narration conversational and direct in tone, just not aimed at "tú" as a grammatical subject.

**Vocabulary:** Use standard pan-Latin American business Spanish. Avoid regionalism that would feel odd outside one country. Apply the same plain-language rule as in English: prefer everyday words over technical terms whenever the meaning survives the swap (for example, "aumento generalizado de precios" instead of "inflación" on first mention, then "los precios" on later mentions). Use jargon only when there is no accurate plain-language substitute.

**Key terms:**
- supply chain → cadena de suministro
- operational risk → riesgo operacional
- workforce → fuerza laboral
- poverty gap → brecha de pobreza
- land titling → titulación de tierras
- early warning systems → sistemas de alerta temprana
- parametric insurance → seguro paramétrico
- clientelism → clientelismo
- informal settlements → asentamientos informales
- cash transfer → transferencia monetaria

**Pull quotes:** Rewrite for punch in Spanish. Do not translate word-for-word. The rhythm should feel natural when spoken aloud.

**File format:** Mirror the English .qmd structure exactly, including callout blocks, stage directions, and production notes — all translated.

---

## Completed Example

See `reports/0001-adapting-to-adversity.qmd` (English) and `reports/0001-adapting-to-adversity-ES.qmd` (Spanish) for a fully worked example based on the World Bank report *Adapting to Adversity: Poverty and Climate Risks in Latin America and the Caribbean* (2026). These files reflect all style rules, fact-checking passes, and production note conventions described above.
