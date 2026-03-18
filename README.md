# Top Journal Writing Mentor

A [Claude Code](https://claude.ai/code) skill for analyzing and improving academic manuscripts based on writing patterns from top finance journals.

**Journals covered**: JFQA · JCF · Journal of Finance · Review of Finance

---

## What It Does

This skill helps you:

1. **Analyze your manuscript** against top journal writing standards — section by section with scores and rewrite suggestions
2. **Learn writing patterns** extracted from 50 real published papers (abstracts, introductions, hypothesis development, robustness sections)
3. **Rewrite sections** in JFQA / JCF / JF style while preserving your scientific content
4. **Use correct identification language** — templates for DiD, IV, RDD, PSM-DiD, Oster bound, and 6 more designs

## Trigger Phrases

Say any of the following to activate this skill:

- `根据顶刊论文分析我的manuscript`
- `analyze my manuscript against top journal style`
- `用顶刊风格改写我的Introduction`
- `按顶刊标准检查我的稿件`
- `rewrite my abstract in JFQA style`

---

## Installation

Copy the skill folder to your Claude Code skills directory:

```bash
cp -r top-journal-writing-mentor ~/.claude/skills/
```

Or clone directly:

```bash
git clone https://github.com/Jill0099/top-journal-writing-mentor ~/.claude/skills/top-journal-writing-mentor
```

---

## File Structure

```
top-journal-writing-mentor/
├── SKILL.md                          # Core skill (auto-loaded when triggered)
└── references/
    ├── section-patterns.md           # Abstract/Intro/Hypothesis/Results patterns
    └── empirical-design-patterns.md  # 10 identification strategy templates
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
