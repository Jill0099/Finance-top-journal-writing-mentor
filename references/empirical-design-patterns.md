# Empirical Design Patterns — Prose Templates
## How to Describe Identification Strategies in Top Finance Journals

Extracted from 50 papers across JFQA, JCF, Journal of Finance, and bib annotations.

---

## 1. Difference-in-Differences (DiD)

### Introduction preview (¶3)

> *"We exploit [shock/policy] as a quasi-natural experiment and compare [treated group] to [control group] before and after [year/date]."*

> *"Using a difference-in-differences (DiD) research design, we find that firms in [treated condition] experience a [X]% [increase/decrease] in [outcome] following [event]."* (Guo et al. 2025)

### Regression description (Data/Method section)

> *"We estimate the following difference-in-differences specification:*
> *Y_{i,t} = α + β(Treated_i × Post_t) + γX_{i,t} + δ_i + λ_t + ε_{i,t}*
> *where δ_i denotes firm fixed effects, λ_t denotes year fixed effects, and X_{i,t} is a vector of time-varying control variables. The coefficient of interest, β, captures the differential change in [outcome] for [treated] relative to [control] firms after [event]. Standard errors are clustered at the [firm/industry/state] level."*

### Parallel trends defense (Robustness section)

> *"We verify the parallel trends assumption by estimating a dynamic event study specification, replacing the Treated × Post indicator with a series of year-relative-to-event dummies. Figure X plots the estimated coefficients. The pre-period coefficients are statistically indistinguishable from zero (joint F-test p-value = [X]), while the post-period coefficients are negative and increasing in magnitude, consistent with a treatment effect that grows over time."*

### Placebo test

> *"We conduct a placebo test by reassigning pseudo-treatment dates [X years prior to the actual policy]. Under the null hypothesis of no treatment effect, we expect the coefficient on the placebo interaction to be statistically insignificant. Consistent with this expectation, the placebo coefficient is small and statistically indistinguishable from zero (coefficient = [X], t = [Y])."*

---

## 2. Staggered DiD

When treatment is staggered across units/time:

> *"Our identification exploits the staggered nature of [policy rollout / appointments] across [firms/regions/years]. To address concerns about heterogeneous treatment effects in staggered DiD designs (Goodman-Bacon 2021; Callaway and Sant'Anna 2021), we construct a heterogeneity-robust estimator following [Sun and Abraham (2021) / Callaway and Sant'Anna (2021)]. Our results are robust to this alternative estimator (Table [X], Panel [B])."*

---

## 3. Triple Difference (DDD)

Used to isolate mechanism channels:

> *"To test whether the effect operates through the [mechanism] channel, we augment our DiD specification with an interaction between [Treated × Post] and [Moderator], estimating a triple-difference (DDD) design. The coefficient on Treated × Post × Moderator = [X] (t = [Y]) indicates that the effect is [X]% larger for firms with [high moderator], consistent with the [mechanism] hypothesis."*

---

## 4. Instrumental Variables (IV)

### Introduction preview

> *"To establish causality, we employ [N] instruments for [endogenous variable]: [instrument 1] and [instrument 2]. [Instrument 1] is valid because [intuition for relevance and exclusion]. [Instrument 2] exploits [exogenous variation source]. We find that both instruments are significantly related to [endogenous variable] in the first-stage regression (F-statistic = [X], well above the conventional threshold of 10) and pass the usual over-identification tests."* (Ellis et al. 2020, adapted)

### Method section

> *"In the first stage, we regress [endogenous variable] on [instruments] and the same vector of controls. The F-statistic on the excluded instruments is [X], alleviating concerns about weak instruments. In the second stage, we use the predicted values from the first stage as our measure of [variable]. The coefficient on the instrumented [variable] is [sign and magnitude] (t = [X])."*

### Exclusion restriction defense (required)

> *"The exclusion restriction requires that [instrument] affects [outcome] only through [endogenous variable] and not through any other channel. We argue this holds because [theoretical argument]. As additional support, [evidence: e.g., instrument is uncorrelated with pre-period outcomes, passes over-identification test, etc.]."*

---

## 5. Regression Discontinuity Design (RDD)

### Introduction preview

> *"We exploit a discontinuity in [assignment rule / vote threshold / cutoff] to identify the causal effect of [treatment]. Firms/individuals just above the cutoff [X] are compared to those just below, under the assumption that assignment is as-good-as-random in a narrow bandwidth."* (Flammer 2015)

### Key validation tests (must report all four)

1. **McCrary density test**: *"We find no evidence of manipulation around the cutoff (McCrary density test, t = [X], p = [Y])."*
2. **Covariate balance**: *"Predetermined firm characteristics are balanced across the cutoff (Table [X])."*
3. **Bandwidth robustness**: *"Results are robust to using the Imbens-Kalyanaraman (2012) optimal bandwidth, half the optimal bandwidth, and twice the optimal bandwidth (Table [Y])."*
4. **Polynomial order robustness**: *"Results hold using linear, quadratic, and cubic polynomial specifications (Table [Z])."*

---

## 6. Event Study / Cumulative Abnormal Returns (CARs)

### Standard prose

> *"We estimate cumulative abnormal returns (CARs) over a [−1, +1] event window around [announcement/policy date], using the [market model / Fama-French 3-factor model] estimated over the pre-event window of [−250, −30] trading days. We require at least [X] non-missing return observations in the estimation window."*

### Reporting CARs

> *"We document a mean 3-day CAR of [X]% (t-statistic = [Y]), with [Z]% of the sample exhibiting positive CARs. The economic magnitude is substantial: for the average firm in our sample with a market capitalization of $[X] billion, this return corresponds to a value change of approximately $[Y] million."*

---

## 7. PSM-DiD (Propensity Score Matching + DiD)

Dominant in JCF China papers:

> *"To ensure our findings are not driven by pre-existing differences between treated and control firms, we use propensity score matching (PSM) to construct a matched control sample. Specifically, we estimate a probit model of [treatment] on [matching variables: size, leverage, ROA, Tobin's Q, age] and match each treated firm to the nearest control firm without replacement using a caliper of [0.01/0.05]. We then re-estimate our baseline DiD specification on the matched sample. The results are quantitatively similar to the full-sample estimates (Table [X])."*

---

## 8. Entropy Balancing

Increasingly standard as a robustness check in JFQA/JCF:

> *"As an alternative to propensity score matching, we use entropy balancing (Hainmueller 2012), which reweights the control sample such that the first and second moments of the pretreatment covariates are exactly equal across treated and control groups. This approach avoids the efficiency loss from discarding unmatched control observations. Table [X] shows that our results are robust to this alternative approach."*

---

## 9. Oster (2019) Bound Estimate for Omitted Variable Bias

Increasingly required by JFQA/JCF reviewers:

> *"To assess the robustness of our results to omitted variable bias, we apply the method proposed by Oster (2019). This approach computes the ratio of selection on unobservables relative to observables (δ) that would be required to reduce our estimated coefficient to zero. We find that δ = [X], which [far exceeds / is well above] the conventional threshold of 1, suggesting that unobservables would need to be [X] times as important as the included controls to explain away our results. This provides reassurance that omitted variable bias is unlikely to drive our findings."*

---

## 10. Heckman Two-Stage Selection Model

> *"To address potential sample selection bias, we employ Heckman's (1979) two-stage procedure. In the first stage, we estimate a probit model of [sample selection / treatment selection] using [exclusion restriction variable] as an identifying instrument. We compute the inverse Mills ratio from the first stage and include it as an additional control in the second-stage regression. [Instrument] satisfies the exclusion restriction because [argument]. The coefficient on the inverse Mills ratio is [significant/insignificant], and our main results remain qualitatively unchanged."*

---

## Key Identification Principles (Universal Across All Designs)

1. **Name the assumption explicitly**: Every identification strategy requires stating the key assumption in plain English, then providing evidence for it.

2. **Pre-trend / pre-registration evidence**: For DiD, always show a figure of pre-trends. For IV, always report the first-stage F-statistic and defend exclusion. For RDD, always report the McCrary test.

3. **Alternative explanation paragraph**: Near the end of the results section, write: *"One concern with our interpretation is that [most plausible alternative explanation]. We address this by [specific test]. The results are inconsistent with the [alternative explanation] story because [evidence]."*

4. **China institutional papers**: Always include a paragraph explaining why findings generalize beyond the specific Chinese policy context. Standard language: *"While our empirical setting uses [Chinese policy X], the mechanisms we identify are theoretically general: [mechanism] should operate whenever [condition], which applies broadly to [other contexts]."*

5. **Never claim causality without qualification**: Even with experimental-style identification, use: *"we estimate the causal effect of X on Y"* or *"this evidence is consistent with a causal interpretation"* — not *"we prove causality."*
