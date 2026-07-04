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

**Write for a clever, engaged high schooler.** If a word would need a footnote in a magazine, find a simpler one. Avoid financial and academic jargon — words like "variance," "hedge," "nexus," "discourse," or "paradigm" have plain-English equivalents. Use jargon only when it is the most precise way to convey a concept from the report, and when you do, let context make the meaning clear without a formal definition.
- Wrong: "It'll show up as variance you can't explain and can't hedge."
- Right: "It'll bleed quietly into your numbers, and there's no insurance policy that covers it."

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

**Register:** Use informal **tú** throughout. The host is speaking directly to the viewer. "Usted" would feel too formal for video.

**Vocabulary:** Use standard pan-Latin American business Spanish. Avoid regionalism that would feel odd outside one country.

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
