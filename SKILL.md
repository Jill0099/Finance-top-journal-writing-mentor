---
name: top-journal-writing-mentor
description: This skill should be used when the user asks to "analyze my manuscript against top journal style", "rewrite my introduction in JFQA style", "check my paper against top journal standards", "rewrite my abstract in JCF style", "improve my writing based on top finance journal papers", "help me write identification strategy language for DiD", or provides PDF papers for writing style analysis. Specialized for top finance journals: JFQA, JCF, Journal of Finance, Review of Finance.
version: 1.1.0
---

# Top Journal Writing Mentor (Finance)

Writing style mentor built from systematic analysis of 50 papers across JFQA, JCF, Journal of Finance, and Review of Finance. Includes full-text reading and structured annotations.

---

## Core Workflow

### Analyze Manuscript Against Top Journal Style

1. Ask the user to provide their manuscript (PDF or text)
2. Identify target journal (JFQA / JCF / JF) — influences section structure and hypothesis format
3. Analyze section by section using `references/section-patterns.md`
4. Output structured feedback report (see format below)

### User Provides Reference PDFs + Manuscript

1. Read reference papers to extract style fingerprint
2. Compare manuscript section by section against that fingerprint
3. Output targeted feedback with rewritten examples

### Rewrite a Section

1. Load target journal conventions from `references/section-patterns.md`
2. Rewrite preserving scientific content; annotate each change with rule applied

---

## Journal Quick Reference

| Feature | JFQA | JCF | JF | Review of Finance |
|---------|------|-----|-----|-------------------|
| Abstract | 100–140 words | 130–160 words + keywords box | 120–180 words | 100–150 words |
| Section numbering | Roman (I, II, III) | Arabic decimals (1, 2.1, 2.2) | Roman | Arabic decimals |
| Hypothesis format | Italicized prose — no boxes | Formal **H1(a)**, **H1(b)** boxes | Integrated prose | Italicized prose |
| Footnote density | High (15–25/paper) | Low–medium | Medium | Medium |
| Article info box | No | Yes (editor, JEL, keywords) | No | Yes (JEL, keywords) |
| Roadmap sentence | Last sentence of intro | Last sentence of intro | Last sentence of intro | Last sentence of intro |

---

## The 7-Paragraph Introduction Skeleton

Every accepted paper in this corpus follows this structure. See `references/section-patterns.md` for full examples.

```
¶1  HOOK         — event date / survey stat / striking fact (never "This paper studies...")
¶2  LITERATURE   — what is known + gap sentence ("However, little is known about...")
¶3  DESIGN       — the quasi-natural experiment / instrument (most critical paragraph)
¶4  FINDINGS     — 2–3 key results WITH specific numbers and baseline anchor
¶5  MECHANISM    — "The effect is concentrated among firms that X, consistent with Y channel"
¶6  ROBUSTNESS   — names the key endogeneity concern and the test that addresses it
¶7  CONTRIBUTION — 2–4 specific literatures by name; ends with roadmap sentence
```

**Opening sentence archetypes** (observed in corpus):
- Event: *"On June 23, 2016, voters in the United Kingdom elected to leave the European Union."* (Campello et al. 2022, JFQA)
- Fact: *"Policy uncertainty can harm the economy."* (Nguyen & Phan 2017, JFQA)
- Broad importance: *"Economists understand the crucial role that innovation plays in a nation's economic growth."* (Ellis et al. 2020, JFQA)
- Bold assertion: *"Asset prices should equal expected discounted cashflows."* (Cochrane 2011, JF)
- Never: *"In recent years...", "With the development of...", "This paper examines..."*

---

## Abstract Formula

**JFQA (4-move, ~120 words)**:
```
Move 1: [Method/sample] + [research question]
Move 2: [Main finding — specific and directional]
Move 3: [Robustness: "These results are robust to..."]
Move 4: [Identification OR overall interpretation]
```

**JCF (5-move, ~140 words)**:
```
Move 1: [Institutional setting / quasi-natural experiment]
Move 2–3: [Main findings with specific % magnitudes]
Move 4: [Mechanism]
Move 5: [Policy implication or contribution claim]
```

---

## Findings Preview — Critical Pattern

**Always include specific numbers in the introduction.** The single most consistent pattern across all 50 papers in the corpus.

**Strong** (JFQA): *"An interquartile increase in our primary measure of corruption is associated with a 17.4% decline in the number of patents."* (Ellis et al. 2020)

**Strong** (JFQA): *"Given that the average quarterly investment rate in 2015 was 1.1% of assets, this decline represents a drop of 15% in baseline investment spending."* (Campello et al. 2022)

**Strong** (JCF): *"The baseline reform results in a 10.08% reduction in the average annual compensation of SOE executives."* (Cao et al. 2026)

**Weak** (never acceptable): *"We find a significant negative effect of corruption on innovation."*

Rule: Report the coefficient magnitude → scale to a meaningful baseline unit → state what % of the mean this represents.

---

## Hedging Language Tiers

**Tier 1 — For main causal claims** (even with DiD or IV):
- "is consistent with", "suggests that", "provides evidence that", "is associated with"
- Never "proves" or "demonstrates causality"

**Tier 2 — For mechanism claims**:
- "appears to operate through", "is primarily driven by", "the pattern is consistent with X rather than Y"

**Tier 3 — For scope limits**:
- "while we cannot rule out", "results should be interpreted with caution in [context]"

---

## Contribution Paragraph Pattern

Every paper names 2–4 specific literatures. Template:

```
"We contribute to the literatures on [X] and [Y].

[Prior work on X does Z. We differ by showing...]

Second, our study contributes to [Y] by [specific angle]."
```

Never: "We contribute to the literature on [broad field]."

---

## Identification Strategy Language

Always preview the identification strategy in the introduction:

**DiD**: *"We exploit [shock] as a quasi-natural experiment and compare [treated group] to [control group] before and after [date]."*

**IV**: *"To establish causality, we employ [N] instruments for [variable]: [instrument]. We find that [instrument] passes the relevance condition (F-statistic = X) and defend the exclusion restriction because [argument]."*

**RDD**: *"We exploit a discontinuity in [assignment rule] to compare [units] just above and below the cutoff, under the assumption that assignment is as-good-as-random in a narrow bandwidth."*

---

## Feedback Report Format

```markdown
# Writing Style Analysis Report
**Target Journal**: [JFQA / JCF / JF]

## Overall Assessment
[2–3 sentences: strengths and main gaps vs top journal standard]

## Section Analysis

### Abstract [X/5]
**Issue**: [specific problem]
**Rewrite**:
> [rewritten version]

### Introduction [X/5]
**Opening sentence**: [assess — event/fact/assertion vs generic]
**Gap statement**: [assess — explicit or implicit?]
**Findings preview**: [assess — specific numbers included?]
**Identification strategy**: [assess — previewed in intro?]
**Contribution paragraph**: [assess — specific literatures named?]
**Roadmap sentence**: [assess — last sentence of intro?]
**Suggested rewrite of weakest paragraph**:
> [rewritten version]

### Hypothesis Development [X/5]
[For JCF: are H1(a)/H1(b) format used? For JFQA: italicized prose?]

## Top 3 Priority Fixes
1. [Highest impact change with example]
2. ...
3. ...

## Sentence-Level Examples
| Original | Rewritten | Rule |
|----------|-----------|------|
| "In recent years..." | "On [date], X occurred..." | Avoid generic opening |
| "significant effect" | "17.4% decline (t = -3.2)" | Include numbers |
```

---

## Common Mistakes (From Corpus Analysis)

1. **Generic opening** — "In recent years / with the development of" → replace with event/fact/assertion
2. **No numbers in introduction** — translate every key coefficient to % of sample mean
3. **Vague identification** — name the exact shock and why it is exogenous
4. **Missing pre-trend figure** — now nearly obligatory in JFQA/JCF
5. **Roadmap in wrong position** — always the final sentence of introduction
6. **No formal hypotheses (JCF)** — JCF expects H1(a)/H1(b) format
7. **Conflating mechanism and robustness tests** — keep them in separate sections
8. **Missing exclusion restriction defense** for IV papers
9. **China papers without generalizability discussion** — always explain why findings travel beyond the specific institutional context

---

## Additional Resources

### Reference Files

- **`references/section-patterns.md`** — Section-by-section structural patterns with real paper quotes
- **`references/empirical-design-patterns.md`** — How to describe 10 identification strategies in prose (DiD, IV, RDD, PSM-DiD, Oster bound, etc.)

### Standalone Prompts (Copy-Paste Ready)

For use without Claude Code — paste directly into any Claude chat:

- **`prompts/01-analyze-manuscript.md`** — Full manuscript analysis with section scores
- **`prompts/02-rewrite-introduction.md`** — 7-paragraph introduction rewrite
- **`prompts/03-rewrite-abstract.md`** — Abstract rewrite (JFQA 4-move / JCF 5-move)
- **`prompts/04-identification-language.md`** — DiD / IV / RDD / Oster / PSM-DiD language templates
