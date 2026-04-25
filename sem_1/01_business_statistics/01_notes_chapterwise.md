# Business Statistics — Chapter-wise Notes

> Use alongside Anderson, Sweeney & Williams (T1). Each chapter ends with a 60-second recap.

---

## Chapter 1 — Introduction to Statistics & Data

### 1.1 What is statistics?
A discipline of collecting, organising, summarising, analysing, and interpreting data so business decisions are supported by evidence rather than gut feel.

Two broad branches:
- **Descriptive statistics** — summarise data (mean, σ, charts).
- **Inferential statistics** — generalise from a sample to a population (estimation, hypothesis testing).

### 1.2 Population vs sample
- **Population (N)**: the complete set of all elements of interest (e.g., all 30,000 employees of TCS).
- **Sample (n)**: a subset selected for study (e.g., 500 employees surveyed).
- **Parameter**: numerical summary of a population (μ, σ, π).
- **Statistic**: numerical summary of a sample (x̄, s, p).

### 1.3 Types of data

| Scale | Property | Example | Permitted operations |
|-------|----------|---------|----------------------|
| Nominal | Labels only | Gender, brand | Counts, mode |
| Ordinal | Order, no equal gaps | Customer satisfaction (1–5) | Median, percentiles |
| Interval | Equal gaps, no true zero | Temperature in °C | Mean, σ, addition |
| Ratio | Equal gaps + true zero | Revenue, weight | All arithmetic |

### 1.4 Sources of data
- **Primary**: collected first-hand (surveys, experiments, observations).
- **Secondary**: already-existing (RBI, NSO, Bloomberg, internal CRM logs).

### 60-second recap
Statistics turns raw numbers into evidence. Know the difference between a parameter (population) and a statistic (sample), and the four data scales — they decide which formula you can use.

---

## Chapter 2 — Descriptive Statistics

### 2.1 Frequency distribution
Group raw data into class intervals; record counts. Display via:
- **Histogram** — vertical bars, no gaps (continuous data).
- **Bar chart** — gaps between bars (categorical data).
- **Ogive** — cumulative frequency curve, used to read percentiles.

### 2.2 Measures of central tendency

| Measure | Formula | When to use | Robust to outliers? |
|---------|---------|-------------|---------------------|
| Mean | x̄ = Σx / n | Symmetric data, ratio scale | No |
| Median | Middle value when sorted | Skewed data, ordinal | Yes |
| Mode | Most frequent value | Nominal data, identifying peaks | Yes |
| Weighted mean | Σ(wᵢxᵢ) / Σwᵢ | Different weights per observation | No |
| Geometric mean | (x₁·x₂·…·xₙ)^(1/n) | Growth rates, ratios | Slightly |
| Harmonic mean | n / Σ(1/xᵢ) | Average of rates (km/h) | Yes |

### 2.3 Measures of dispersion

| Measure | Formula |
|---------|---------|
| Range | max − min |
| Variance (sample) | s² = Σ(x − x̄)² / (n−1) |
| Standard deviation | s = √s² |
| Coefficient of variation | CV = s / x̄ × 100 % |
| Inter-quartile range | IQR = Q3 − Q1 |

Why divide by **n−1** for sample variance? Bessel's correction — gives an unbiased estimate of population variance.

### 2.4 Measures of shape
- **Skewness**: asymmetry. Positive skew → long right tail (income, asset prices). Negative skew → long left tail (exam scores when easy).
  - Pearson's coefficient = 3(Mean − Median) / σ
- **Kurtosis**: tailedness. Excess kurtosis > 0 → leptokurtic (fat tails). < 0 → platykurtic (thin tails).

### 2.5 Five-number summary & box-plot
Min · Q1 · Median · Q3 · Max.
Outliers: any value outside Q1 − 1.5·IQR or Q3 + 1.5·IQR.

### 60-second recap
Mean is sensitive to outliers, median is not. Use σ to express spread, CV to compare spreads of different units. Skewness signals the side with the long tail; kurtosis signals heavy tails.

---

## Chapter 3 — Probability

### 3.1 Definitions
- **Random experiment**: outcome cannot be predicted with certainty (rolling a die).
- **Sample space (S)**: set of all possible outcomes.
- **Event (E)**: subset of S.

### 3.2 Approaches to probability
1. **Classical**: P(E) = favourable / total (when outcomes are equally likely).
2. **Relative frequency**: P(E) = (number of times E occurred) / total trials.
3. **Subjective**: degree of belief based on judgement.

### 3.3 Axioms (Kolmogorov)
1. 0 ≤ P(E) ≤ 1
2. P(S) = 1
3. For mutually exclusive events: P(A ∪ B) = P(A) + P(B)

### 3.4 Rules

| Rule | Formula |
|------|---------|
| Complement | P(Aᶜ) = 1 − P(A) |
| Addition (general) | P(A ∪ B) = P(A) + P(B) − P(A ∩ B) |
| Multiplication (independent) | P(A ∩ B) = P(A) × P(B) |
| Multiplication (dependent) | P(A ∩ B) = P(A) × P(B \| A) |
| Conditional | P(A \| B) = P(A ∩ B) / P(B) |

### 3.5 Bayes' theorem

P(Aᵢ | B) = [P(B | Aᵢ) · P(Aᵢ)] / Σⱼ [P(B | Aⱼ) · P(Aⱼ)]

Use when we know P(test result | disease) but want P(disease | test result). Foundation of Naive Bayes classifiers in ML.

**Example.** A test for a rare disease has 95% sensitivity and 90% specificity. Disease prevalence = 1%. P(disease | positive) = ?
- P(+ | D) = 0.95, P(+ | ¬D) = 0.10, P(D) = 0.01
- P(D | +) = (0.95 × 0.01) / (0.95 × 0.01 + 0.10 × 0.99) = 0.0095 / 0.1085 ≈ 8.8 %.
Counter-intuitive: even a "positive" result means only 9% chance of disease. This is the base-rate fallacy.

### 60-second recap
Probability lives between 0 and 1. Addition for "or" (subtract overlap), multiplication for "and" (independence simplifies). Bayes flips the conditional and is the heart of medical screening + spam filters + Naive Bayes.

---

## Chapter 4 — Probability Distributions

### 4.1 Discrete distributions

#### Bernoulli
- 1 trial, two outcomes (success/failure).
- P(X = 1) = p, P(X = 0) = 1 − p.
- Mean = p, Variance = p(1 − p).

#### Binomial — n independent Bernoulli trials
- P(X = k) = C(n, k) · pᵏ · (1−p)ⁿ⁻ᵏ
- Mean = np, Variance = np(1 − p).
- Use when: fixed n trials, two outcomes, constant p, independent trials.

#### Poisson — rare events in fixed interval
- P(X = k) = (e⁻λ · λᵏ) / k!
- Mean = Variance = λ.
- Use when: events independent, rate constant, intervals small.
- **Binomial → Poisson approximation** when n large, p small, np ≤ 10.

#### Hypergeometric — sampling without replacement
- P(X = k) = [C(K, k) · C(N−K, n−k)] / C(N, n)
- Used when population is finite and successes are not replaced.

### 4.2 Continuous distributions

#### Uniform
- f(x) = 1 / (b − a) for a ≤ x ≤ b.
- Mean = (a + b)/2, Variance = (b − a)² / 12.

#### Normal — the bell curve
- f(x) = (1 / σ√(2π)) · exp(−(x − μ)² / 2σ²)
- Symmetric around μ; ~68% within μ ± σ, ~95% within μ ± 2σ, ~99.7% within μ ± 3σ.
- **Standardise**: Z = (X − μ) / σ; Z ~ N(0, 1).
- Read Z-tables to find P(Z ≤ z).

#### Exponential — time between Poisson events
- f(x) = λe^(−λx), x ≥ 0.
- Mean = 1/λ, Variance = 1/λ².
- Memoryless property.

### 4.3 Approximations
- Binomial → Normal when np ≥ 5 and n(1−p) ≥ 5. Use μ = np, σ² = np(1−p), with continuity correction (±0.5).
- Binomial → Poisson when n ≥ 30, p ≤ 0.05, np ≤ 10.

### 60-second recap
Discrete = countable outcomes (binomial counts successes; Poisson counts events). Continuous = measurable (normal is the universal default; exponential models waiting times). Always identify the random experiment first, then pick the distribution.

---

## Chapter 5 — Sampling and Sampling Distributions

### 5.1 Sampling techniques

| Method | Description | When to use |
|--------|-------------|-------------|
| Simple random | Every unit equal chance | Homogeneous population |
| Stratified | Divide into strata, sample within | Heterogeneous, want representation |
| Systematic | Every kᵗʰ element | Ordered list |
| Cluster | Sample whole groups | Geographically dispersed |
| Convenience | Easiest to reach | Pilot study only — biased |

### 5.2 Sampling distribution of the mean
If we draw all possible samples of size n and compute x̄ for each, the distribution of x̄ has:
- Mean: μ_x̄ = μ
- Standard error: σ_x̄ = σ / √n (or s/√n if σ unknown)

### 5.3 Central Limit Theorem
For sufficiently large n (≥30), the sampling distribution of x̄ is approximately normal regardless of the population's distribution. This is the engine that makes nearly all inference work.

### 5.4 Sampling distribution of the proportion
- Mean: μ_p = π
- Standard error: σ_p = √(π(1−π)/n)
- Approximately normal when nπ ≥ 5 and n(1−π) ≥ 5.

### 60-second recap
Pick a sample, compute a statistic. Repeat. The variation of that statistic across samples is the sampling distribution. CLT says: the sample mean is approximately normal for n ≥ 30. Standard error shrinks as 1/√n.

---

## Chapter 6 — Estimation

### 6.1 Point estimation
A single best-guess value. Properties of a good estimator:
- **Unbiasedness**: E(θ̂) = θ
- **Consistency**: θ̂ → θ as n → ∞
- **Efficiency**: minimum variance among unbiased estimators
- **Sufficiency**: uses all sample information

### 6.2 Interval estimation — Confidence Intervals (CI)

**For population mean (σ known)**: x̄ ± Z_(α/2) · (σ/√n)
**For population mean (σ unknown, n small)**: x̄ ± t_(α/2, n−1) · (s/√n)
**For population proportion**: p̂ ± Z_(α/2) · √(p̂(1−p̂)/n)

Common Z values:
| Confidence | Z |
|-----------:|---|
| 90% | 1.645 |
| 95% | 1.96 |
| 99% | 2.576 |

**Interpretation of 95% CI**: if we drew many samples and built an interval each time, ~95% of those intervals would contain the true population parameter. NOT "95% chance the true value lies in this interval."

### 6.3 Sample size determination
For estimating mean with margin of error E:
- n = (Z · σ / E)²
For estimating proportion:
- n = (Z² · p̂(1−p̂)) / E²

If p̂ unknown, use 0.5 for the most conservative (largest) sample size.

### 60-second recap
A point estimate is a single number; a CI is a range. Width grows with desired confidence (Z), variability (σ), and shrinks with √n. To halve the margin of error, quadruple the sample.

---

## Chapter 7 — Hypothesis Testing

### 7.1 Setup
- **H₀ (null)**: status quo, "no effect" (e.g., μ = 50).
- **H₁ (alternative)**: claim we want evidence for (e.g., μ ≠ 50, > 50, or < 50).
- **α (significance level)**: P(reject H₀ | H₀ true) = Type I error rate. Commonly 0.05.
- **β**: P(fail to reject H₀ | H₀ false) = Type II error.
- **Power = 1 − β**.

### 7.2 Test procedure
1. State H₀ and H₁ (one-tailed or two-tailed).
2. Choose α.
3. Compute test statistic.
4. Find critical value or p-value.
5. Decide: reject H₀ if test statistic falls in rejection region OR if p ≤ α.
6. Conclude in business language.

### 7.3 Common tests

| Test | When | Statistic |
|------|------|-----------|
| One-sample Z (mean, σ known) | Large n | (x̄ − μ₀) / (σ/√n) |
| One-sample t (mean, σ unknown) | Any n; use df = n−1 | (x̄ − μ₀) / (s/√n) |
| One-sample proportion | nπ₀ ≥ 5 | (p̂ − π₀) / √(π₀(1−π₀)/n) |
| Two-sample t (independent) | Compare two means | (x̄₁ − x̄₂) / SE |
| Paired t | Same subjects, before/after | d̄ / (s_d/√n) |
| Chi-square goodness-of-fit | Observed vs expected categories | Σ (O−E)²/E |
| Chi-square independence | 2 categorical variables | Same; df = (r−1)(c−1) |

### 7.4 p-value approach
p-value = probability of observing a test statistic at least as extreme as the one computed, assuming H₀ is true. Smaller p → stronger evidence against H₀.

### 60-second recap
Hypothesis testing converts data into a binary decision. Pick α, compute statistic, compare to critical value or p to α. Rejecting H₀ does not "prove" H₁ — it just says the data are unlikely under H₀.

---

## Chapter 8 — Analysis of Variance (ANOVA)

### 8.1 One-way ANOVA
Compares means of 3+ independent groups. H₀: μ₁ = μ₂ = … = μₖ.

Decompose total variation:
- **SST (total)** = SSB (between groups) + SSW (within groups)
- F = MSB / MSW = (SSB/(k−1)) / (SSW/(N−k))
- Compare to F_(α, k−1, N−k).

### 8.2 Why not multiple t-tests?
Multiple t-tests inflate the family-wise error rate. ANOVA controls overall α at one level.

### 8.3 Post-hoc
If F is significant, use Tukey's HSD or Bonferroni to find which pairs differ.

### 60-second recap
ANOVA tests whether at least one group mean differs. F-statistic = between-group spread / within-group spread. Big F → reject equality.

---

## Chapter 9 — Correlation and Regression

### 9.1 Correlation
- **Covariance** Cov(X, Y) = Σ(xᵢ − x̄)(yᵢ − ȳ) / (n−1). Sign tells direction; magnitude depends on units.
- **Pearson's r** = Cov(X, Y) / (s_x · s_y). Range: −1 to +1.
  - |r| ≥ 0.7 → strong; 0.3 ≤ |r| < 0.7 → moderate; < 0.3 → weak.
- **Spearman's ρ**: rank correlation; robust to outliers, non-linear monotone.

Correlation ≠ causation. Always check for confounders.

### 9.2 Simple linear regression
Model: Y = β₀ + β₁X + ε

**Least-squares estimates**:
- b₁ = Σ(xᵢ − x̄)(yᵢ − ȳ) / Σ(xᵢ − x̄)²
- b₀ = ȳ − b₁x̄

**Goodness of fit**:
- R² = SSR/SST = 1 − SSE/SST.
- Standard error of estimate s_e = √(SSE / (n−2)).

**Inference on β₁**: t = b₁ / SE(b₁), df = n − 2.

### 9.3 Multiple regression
Y = β₀ + β₁X₁ + β₂X₂ + … + βₖXₖ + ε

- Adjusted R² penalises adding useless predictors.
- **Multicollinearity**: predictors correlated with each other. Detect via VIF (Variance Inflation Factor); VIF > 10 → problem.
- Assumptions: linearity, independence, normality of residuals, homoscedasticity (LINH).

### 60-second recap
Correlation measures linear association (−1 to +1). Regression fits a line by minimising squared errors. R² is share of variance explained. Beware multicollinearity in multiple regression.

---

## Chapter 10 — Time Series & Forecasting

### 10.1 Components
- **Trend (T)**: long-term direction.
- **Seasonality (S)**: regular short-term cycles (quarterly, monthly).
- **Cyclical (C)**: longer waves (business cycles).
- **Irregular (I)**: random noise.

Models: additive Y = T + S + C + I; multiplicative Y = T × S × C × I.

### 10.2 Forecasting techniques

| Technique | When to use |
|-----------|-------------|
| Naive (Y_t = Y_(t−1)) | Stable series, baseline |
| Moving average | Smooth random fluctuations |
| Weighted moving average | Recent values matter more |
| Exponential smoothing | Recent values weighted exponentially |
| Holt's (trend) / Holt-Winters (trend + seasonality) | Patterns present |
| Linear trend regression | Clear linear trend |

**Simple exponential smoothing**: F_(t+1) = αY_t + (1 − α) F_t, α ∈ [0, 1].

### 10.3 Forecast accuracy
- **MAD** = Σ|e| / n
- **MSE** = Σe² / n
- **MAPE** = (Σ|e/Y| / n) × 100%
- **Bias** = Σe / n; should be near 0.

### 60-second recap
Decompose to understand. Forecast using technique matched to pattern. Compare models with MAD/MSE/MAPE — lowest wins.

---

## Chapter 11 — Index Numbers

### 11.1 Simple price index
P_(0t) = (P_t / P_0) × 100

### 11.2 Weighted indices (price)
- **Laspeyres** = Σ(P_t · Q_0) / Σ(P_0 · Q_0) × 100 — base-year quantities.
- **Paasche** = Σ(P_t · Q_t) / Σ(P_0 · Q_t) × 100 — current-year quantities.
- **Fisher's ideal** = √(Laspeyres × Paasche) — passes both time-reversal and factor-reversal tests.

### 11.3 Tests of an index
- **Time-reversal**: P_(0t) × P_(t0) = 1.
- **Factor-reversal**: P × Q = value index.

### 11.4 CPI applications
- Real income = nominal income × (100 / CPI).
- Inflation rate = (CPI_t − CPI_(t−1)) / CPI_(t−1) × 100.

### 60-second recap
Indices compare values over time. Laspeyres uses old quantities (overstates inflation), Paasche uses new (understates), Fisher splits the difference.

---

## Chapter 12 — Decision-making & SQC (overview)

### 12.1 Decision under uncertainty
- **Maximax** (optimist): pick alternative with the best best-case payoff.
- **Maximin** (pessimist): pick alternative with the best worst-case payoff.
- **Minimax regret**: minimise the maximum regret.
- **Laplace**: assume equally likely; pick highest average.

### 12.2 Decision under risk (probabilities known)
- **Expected Monetary Value (EMV)** = Σ Pᵢ × Payoffᵢ. Pick max EMV.
- **EVPI** (Expected Value of Perfect Information) = (EV with perfect info) − (best EMV).

### 12.3 Statistical Quality Control
- **Variable charts**: X-bar (mean), R (range).
- **Attribute charts**: p (proportion defective), c (count of defects).
- Process is in control if points lie within ±3σ control limits and show no patterns.

### 60-second recap
Decision tools formalise judgement when payoffs and probabilities are known. SQC charts spot when a process drifts out of control before defects pile up.

---

## References & Sources

### Primary textbook (T1)
Anderson, Sweeney & Williams — *Statistics for Business and Economics*, Cengage Learning.
- Publisher page: https://www.cengage.com/c/statistics-for-business-economics-15e-anderson/

### Chapter-to-source mapping

| Chapter | Primary source | Online supplement |
|---------|----------------|-------------------|
| 1 — Introduction | Anderson Ch. 1; OpenStax Ch. 1 | https://openstax.org/details/books/introductory-business-statistics-2e |
| 2 — Descriptive stats | Anderson Ch. 2–3; Levine Ch. 3–4 | https://www.khanacademy.org/math/statistics-probability/summarizing-quantitative-data |
| 3 — Probability | Anderson Ch. 4 | https://stattrek.com/probability/probability-rules |
| 4 — Distributions | Anderson Ch. 5–6 | https://stattrek.com/probability-distributions/probability-distribution |
| 5 — Sampling & CLT | Anderson Ch. 7 | https://www.khanacademy.org/math/statistics-probability/sampling-distributions-library |
| 6 — Estimation | Anderson Ch. 8 | https://stattrek.com/estimation/confidence-interval |
| 7 — Hypothesis testing | Anderson Ch. 9 | https://www.khanacademy.org/math/ap-statistics/tests-significance-ap |
| 8 — ANOVA | Anderson Ch. 13 | https://stattrek.com/anova/anova |
| 9 — Regression | Anderson Ch. 14–15 | https://www.statlearning.com (ISLR Ch. 3) |
| 10 — Time series | Anderson Ch. 17 | https://otexts.com/fpp3/ (Hyndman) |
| 11 — Index numbers | S.P. Gupta Ch. 11 | RBI WPI manual: https://www.rbi.org.in/scripts/PublicationsView.aspx?id=15394 |
| 12 — Decision-making & SQC | Anderson Ch. 21–22 | NIST Engineering Statistics Handbook: https://www.itl.nist.gov/div898/handbook/ |

### Free reference
- NIST/SEMATECH e-Handbook of Statistical Methods: https://www.itl.nist.gov/div898/handbook/
- Statistics by Jim (intuitive explanations): https://statisticsbyjim.com/
- Cross-Validated (StackExchange): https://stats.stackexchange.com/

### Bayes' theorem extra reading
- 3Blue1Brown video (visual proof): https://www.youtube.com/watch?v=HZGCoVF3YvM
- Better Explained — Bayes: https://betterexplained.com/articles/an-intuitive-and-short-explanation-of-bayes-theorem/

### Indian-context data
- RBI Database on Indian Economy (DBIE): https://dbie.rbi.org.in/
- Ministry of Statistics (MoSPI): https://www.mospi.gov.in/
- NSE/BSE for live market data
