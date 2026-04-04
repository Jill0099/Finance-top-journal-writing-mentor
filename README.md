# Top Journal Writing Mentor

A [Claude Code](https://claude.ai/code) skill for analyzing and improving academic manuscripts based on writing patterns from top finance journals.

**Journals covered**: JFQA · JCF · Journal of Finance · Review of Finance

---

## What It Does

This skill helps you:

1. **Analyze your manuscript** against top journal writing standards — section by section with scores and rewrite suggestions
2. **Learn writing patterns** extracted from 50 real published papers (abstracts, introductions, hypothesis development, robustness sections)
3. **Sell your paper effectively** — 8 rhetorical strategies from top papers with verbatim examples (how to hook editors, frame gaps, position contributions)
4. **Rewrite sections** in JFQA / JCF / JF style while preserving your scientific content
5. **Use correct identification language** — templates for DiD, IV, RDD, PSM-DiD, Oster bound, and 6 more designs

## Trigger Phrases

Say any of the following to activate this skill:

- `analyze my manuscript against top journal style`
- `rewrite my introduction in JFQA style`
- `check my paper against top journal standards`
- `rewrite my abstract in JCF style`
- `help me write identification strategy language for DiD`

---

## Installation

Copy the skill folder to your Claude Code skills directory:

```bash
cp -r top-journal-writing-mentor ~/.claude/skills/
```

Or clone directly:

```bash
git clone https://github.com/Jill0099/Finance-top-journal-writing-mentor ~/.claude/skills/top-journal-writing-mentor
```

---

## File Structure

```
top-journal-writing-mentor/
├── SKILL.md                          # Core skill (auto-loaded when triggered)
├── references/
│   ├── section-patterns.md           # Abstract/Intro/Hypothesis/Results patterns
│   ├── selling-strategies.md         # 8 rhetorical strategies for selling papers
│   └── empirical-design-patterns.md  # 10 identification strategy templates
└── prompts/
    ├── 01-analyze-manuscript.md      # Full manuscript analysis prompt
    ├── 02-rewrite-introduction.md    # Introduction rewrite prompt (7-paragraph skeleton)
    ├── 03-rewrite-abstract.md        # Abstract rewrite (JFQA 4-move / JCF 5-move)
    └── 04-identification-language.md # Identification strategy language (DiD/IV/RDD/Oster/PSM)
```

---

## Key Patterns Encoded

### Introduction Structure (7-paragraph skeleton)
Every accepted paper in the corpus follows this exact structure:
1. **Hook** — event date / survey stat / striking fact
2. **Literature** — what is known + gap sentence
3. **Design** — the quasi-natural experiment (most critical paragraph)
4. **Findings** — 2–3 key results with specific numbers and baseline anchor
5. **Mechanism** — channel analysis
6. **Robustness** — names key endogeneity concern and the test
7. **Contribution** — 2–4 specific literatures + roadmap sentence

### Journal Differences

| Feature | JFQA | JCF | JF |
|---------|------|-----|-----|
| Abstract | 100–140 words | 130–160 words + keywords | 120–180 words |
| Section numbering | Roman (I, II, III) | Arabic decimals (1, 2.1) | Roman |
| Hypothesis format | Italicized prose | Formal **H1(a)**, **H1(b)** | Integrated prose |
| Footnote density | High (15–25/paper) | Low–medium | Medium |

### Identification Strategy Templates
10 designs covered: DiD · Staggered DiD · Triple Difference · IV · RDD · Event Study · PSM-DiD · Entropy Balancing · Oster (2019) · Heckman

---

## Common Mistakes This Skill Catches

1. Generic opening ("In recent years...") → replace with event/fact/assertion
2. No numbers in introduction → every key result needs % + baseline anchor
3. Vague identification strategy → name the exact shock and why it's exogenous
4. Missing parallel trends figure (now near-obligatory in JFQA/JCF)
5. Roadmap sentence not in last position of introduction
6. No formal H1(a)/H1(b) boxes for JCF submissions
7. Conflating mechanism tests with robustness tests
8. China papers without generalizability discussion

---

## Source Papers

Built from systematic reading of **50 papers** across:
- **JFQA** (Journal of Financial and Quantitative Analysis) — 20 papers
- **JCF** (Journal of Corporate Finance) — 9 papers
- **Journal of Finance** — 12 papers
- **Review of Finance** — 9 papers

Topics: political connections, ESG/sustainable finance, corporate governance, executive compensation, policy uncertainty, innovation.

---

## Prompts (Copy-Paste Ready)

The `prompts/` folder contains 4 standalone prompts for use **without** Claude Code — paste directly into any Claude chat:

| File | Use Case |
|------|----------|
| `01-analyze-manuscript.md` | Full manuscript review — section scores + rewrites |
| `02-rewrite-introduction.md` | Rewrite intro following 7-paragraph skeleton |
| `03-rewrite-abstract.md` | Rewrite abstract in JFQA (4-move) or JCF (5-move) style |
| `04-identification-language.md` | Generate DiD / IV / RDD / Oster / PSM-DiD language |

Each prompt is self-contained with fill-in fields (`[e.g., ...]`) — replace with your paper's details and paste.

---

## Usage Example

```
User: 这是我的manuscript草稿，根据顶刊论文分析我的manuscript

Claude: [Loads top-journal-writing-mentor skill]
        [Analyzes abstract, introduction, hypothesis development...]
        [Outputs section-by-section scores + rewrite suggestions]
```

---

## Contributing

If you add more papers to the reference set or improve the patterns, PRs are welcome. Please include:
- Which journal and year the papers are from
- What new patterns you extracted

---

## License

MIT
