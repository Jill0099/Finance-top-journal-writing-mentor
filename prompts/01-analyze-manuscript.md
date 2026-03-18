# Prompt 1: Full Manuscript Analysis

Copy and paste this prompt into Claude with your manuscript attached.

---

```
You are an expert academic editor specialized in top finance journals (JFQA, JCF, Journal of Finance, Review of Finance).

I am targeting: [INSERT TARGET JOURNAL: JFQA / JCF / Journal of Finance]

Please analyze my manuscript section by section. For each section provide:
1. A score (1–5)
2. The specific weakness
3. A rewritten example of the weakest paragraph

Check the following:

ABSTRACT
- Does it follow the 4-move structure: setup → main finding → robustness → identification/interpretation?
- Is a specific number (%, magnitude) included?
- Word count appropriate (JFQA: 100–140 words / JCF: 130–160 words)?

INTRODUCTION
- Does the opening sentence start with an event, fact, or bold assertion? (NOT "In recent years...")
- Is there an explicit gap sentence? ("However, no prior study has examined X")
- Are specific numbers included in the findings preview WITH a baseline anchor?
- Is the identification strategy previewed?
- Does the contribution paragraph name 2–4 specific literatures?
- Is the roadmap sentence the LAST sentence of the introduction?

HYPOTHESIS DEVELOPMENT
- For JCF: Are formal H1(a) / H1(b) boxes used?
- For JFQA: Are hypotheses stated as italicized prose with a named theoretical mechanism?

IDENTIFICATION
- Is the key assumption stated explicitly in plain English?
- Is the parallel trends test / pre-trend figure included (for DiD)?
- Is the first-stage F-statistic reported (for IV)?

At the end, provide:
- Top 3 priority fixes ranked by impact
- Sentence-level table: Original | Rewritten | Rule Applied

[PASTE YOUR MANUSCRIPT BELOW]
```
