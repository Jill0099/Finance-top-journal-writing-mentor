# Prompt 4: Write Identification Strategy Language

Copy and paste the relevant prompt below based on your identification design.

---

## For Difference-in-Differences (DiD)

```
You are an expert academic editor for top finance journals.

Write the identification strategy language for my DiD paper. Produce three paragraphs:

¶1 INTRODUCTION PREVIEW (¶3 of the introduction):
- Name the exact policy/shock and year
- State treated vs. control group
- Why is the variation plausibly exogenous?

¶2 METHOD SECTION description of the regression:
- Write the equation in text form (Y_{i,t} = α + β(Treated × Post) + controls + FE + ε)
- Explain what β identifies
- State how standard errors are clustered

¶3 PARALLEL TRENDS defense (for the robustness section):
- Dynamic event-study specification with year-relative dummies
- Pre-period F-test language
- Describe expected figure pattern

Rules:
- Use hedged language: "consistent with", "suggests", "we interpret"
- Name the specific assumption in plain English
- Never claim "we prove causality"

My details:
- Policy/shock: [e.g., 2014 China SOE executive compensation reform]
- Treated group: [e.g., listed SOEs]
- Control group: [e.g., non-SOE listed firms]
- Outcome variable: [e.g., abnormal labor investment]
- Key concern: [e.g., contemporaneous policies targeting SOEs]
- How addressed: [e.g., triple-difference with firm-specific exposure]
```

---

## For Instrumental Variables (IV)

```
You are an expert academic editor for top finance journals.

Write the identification strategy language for my IV paper. Produce three sections:

¶1 INTRODUCTION PREVIEW:
- Name the instrument(s) and the endogenous variable
- State why the instrument is relevant (correlation with endogenous var)
- State the exclusion restriction argument in one sentence

¶2 METHOD SECTION (first-stage + second-stage):
- First-stage regression description + F-statistic sentence
- Second-stage interpretation
- Over-identification test if multiple instruments

¶3 EXCLUSION RESTRICTION DEFENSE:
- Theoretical argument for why instrument only affects outcome through the endogenous variable
- Any pre-period or placebo evidence

Rules:
- Report first-stage F-statistic explicitly: "F-statistic = [X], well above the conventional threshold of 10"
- Do not conflate relevance and exclusion
- Use: "The exclusion restriction requires that [instrument] affects [outcome] only through [endogenous variable]"

My details:
- Endogenous variable: [e.g., corruption level]
- Instrument(s): [e.g., ethnic fractionalization index, founder's home-state corruption]
- Why relevant: [e.g., higher ethnic fractionalization → higher corruption in prior literature]
- Exclusion argument: [e.g., ethnic fractionalization affects innovation only through corruption, not directly]
- F-statistic: [e.g., 23.4]
```

---

## For Regression Discontinuity (RDD)

```
You are an expert academic editor for top finance journals.

Write the identification strategy language for my RDD paper. Produce three sections:

¶1 INTRODUCTION PREVIEW:
- Name the cutoff rule and running variable
- State treated (just above) vs. control (just below) groups
- State the key identifying assumption in plain English

¶2 FOUR VALIDATION TESTS to report in the paper:
1. McCrary density test (manipulation check)
2. Covariate balance across the cutoff
3. Bandwidth robustness (IK optimal, half, double)
4. Polynomial order robustness (linear, quadratic, cubic)

¶3 METHOD SECTION prose:
- Local linear regression framework
- Bandwidth choice rationale
- How to report the main coefficient

Rules:
- Must report all 4 validation tests; reviewers will ask for them if missing
- Use: "as-good-as-random assignment in a narrow bandwidth around the cutoff"
- Never claim the design identifies a global average treatment effect

My details:
- Setting: [e.g., shareholder vote on CSR proposals]
- Running variable: [e.g., vote share percentage]
- Cutoff: [e.g., 50% majority threshold]
- Outcome: [e.g., subsequent firm ESG score]
- McCrary test result: [e.g., t = 0.43, p = 0.67]
- Bandwidth chosen: [e.g., IK optimal = 8.3 percentage points]
```

---

## For Oster (2019) Omitted Variable Bound

```
You are an expert academic editor for top finance journals.

Write the Oster (2019) robustness paragraph for my paper. This goes in the robustness section.

Produce a single paragraph (4–6 sentences) that:
1. States what the Oster method does (ratio δ of selection on unobservables to observables)
2. Reports the δ value from your analysis
3. Interprets δ relative to the threshold of 1
4. Concludes what this implies for omitted variable bias

Template to follow:
"To assess the robustness of our results to omitted variable bias, we apply the method proposed by Oster (2019). This approach computes the ratio of selection on unobservables relative to observables (δ) that would be required to reduce our estimated coefficient to zero. We find that δ = [X], which [far exceeds / is well above] the conventional threshold of 1, suggesting that unobservables would need to be [X] times as important as the included controls to explain away our results. This provides reassurance that omitted variable bias is unlikely to drive our findings."

My details:
- Main coefficient: [e.g., β = −0.174, t = −3.2]
- δ value: [e.g., δ = 4.7]
- Interpretation: [e.g., unobservables would need to be 4.7× more important than observables]
- R² with no controls: [e.g., 0.08]
- R² with full controls: [e.g., 0.34]
```

---

## For PSM-DiD (Propensity Score Matching + DiD)

```
You are an expert academic editor for top finance journals.

Write the PSM-DiD robustness paragraph for my paper (typically in robustness section or as a footnote to the main results).

Produce one paragraph (5–7 sentences) that explains:
1. Why PSM is used (address pre-existing differences)
2. The probit model variables used for matching
3. Matching method (nearest-neighbor, caliper size, with/without replacement)
4. Result: quantitatively similar to baseline

Rules:
- This is a ROBUSTNESS check, not the main identification — frame it as such
- Always state the caliper size (e.g., 0.01 or 0.05)
- Report that results are "quantitatively similar" rather than "identical"

My details:
- Treatment variable: [e.g., whether firm experienced the 2014 reform]
- Matching variables: [e.g., size, leverage, ROA, Tobin's Q, firm age, industry]
- Caliper: [e.g., 0.01]
- Matching: [e.g., nearest-neighbor without replacement]
- Baseline coefficient: [e.g., −0.0391]
- PSM coefficient: [e.g., −0.0412]
```
