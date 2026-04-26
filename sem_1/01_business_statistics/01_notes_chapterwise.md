# Business Statistics — Session-wise Notes (handout-aligned)

> Built from the official `MBACC ZG501` handout (S2-25, v4.0).
> **Primary text T1** = Levine, Szabat, Stephan & Viswanathan, *Business Statistics*, Pearson 7e (2019).
> **Secondary text T2** = Anderson, Sweeney, Williams, Camm & Martin, *Quantitative Methods for Business*, Cengage 12e (2013).
> **Reference books (per handout, used as alternative reading):**
> - **R1** Ken Black, *Business Statistics*, Wiley 7e (2012) — full alternative to T1 for descriptive/inferential chapters.
> - **R2** Aczel, Sounderpandian, Saravanan & Joshi, *Complete Business Statistics*, McGraw Hill 7e (2017) — alt. for probability, distributions, hypothesis testing.
> - **R3** Hillier & Hillier, *Introduction to Management Science*, McGraw Hill 5e (2019) — LP & operations research (S15).
> - **R4** Render, Stair & Hanna, *Quantitative Analysis for Management*, Pearson 11e (2011) — LP & decision analysis (S15).
>
> 16 contact sessions = exam-ready chunks. Mid-Sem (closed book) covers sessions 1-8; Comprehensive (open book) covers 1-16.
>
> **Note on the handout's S13 / S14 titles**: in the official S2-25 handout, S13 is *titled* "Validating the regression assumption…" but its actual sub-topics are regression fundamentals (types, OLS, R²); S14 is *titled* "Linear Regression" but its sub-topics are diagnostics (heteroscedasticity, Shapiro-Wilk, Anderson-Darling, KS). These notes preserve the handout's titles but follow the handout's sub-topics — i.e. S13 = regression fundamentals, S14 = diagnostics.

## Quick session map

| # | Session | Source | Mid-Sem? |
|--:|---------|--------|:--------:|
| 1 | [Defining and collecting data](#session-1--defining-and-collecting-data) | T1 Ch. 1 | ✅ |
| 2 | [Organising and analysing data](#session-2--organising-and-analysing-data) | T1 Ch. 2 | ✅ |
| 3 | [Numerical Descriptive Measures](#session-3--numerical-descriptive-measures) | T1 Ch. 3 | ✅ |
| 4 | [Basic Probability](#session-4--basic-probability) | T1 Ch. 4 | ✅ |
| 5 | [Discrete Probability Distributions](#session-5--discrete-probability-distributions) | T1 Ch. 5 | ✅ |
| 6 | [Normal Distribution](#session-6--normal-distribution) | T1 Ch. 6 | ✅ |
| 7 | [Sampling Distributions](#session-7--sampling-distributions) | T1 Ch. 7 | ✅ |
| 8 | [Confidence Interval Estimation](#session-8--confidence-interval-estimation) | T1 Ch. 8 | ✅ |
| 9 | [Fundamentals of Hypothesis Testing](#session-9--fundamentals-of-hypothesis-testing) | T1 Ch. 9 | — |
| 10 | [Two-sample tests and ANOVA](#session-10--two-sample-tests-and-anova) | T1 Ch. 10 | — |
| 11 | [Chi-square test](#session-11--chi-square-test) | T1 Ch. 11 | — |
| 12 | [Other Non-parametric tests](#session-12--other-non-parametric-tests) | Class Notes | — |
| 13 | [Validating regression assumption & normality testing](#session-13--validating-regression-assumption--normality-testing) | T1 Ch. 13 | — |
| 14 | [Linear Regression — diagnostics](#session-14--linear-regression--diagnostics) | Class Notes | — |
| 15 | [Introduction to Linear Programming](#session-15--introduction-to-linear-programming) | Class Notes / T2 | — |
| 16 | [Revision](#session-16--revision) | — | — |

---

## Session 1 — Defining and collecting data
**Source:** Levine T1 Ch. 1.

**Why it matters.** Every analytic conclusion is only as good as the data definition and the way it was collected. Mis-defined variables and biased samples cause expensive downstream rework.

**Key concepts**
- **Statistics**: Descriptive (summarise data) vs Inferential (generalise from sample to population).
- **Variable**: a characteristic that varies — Categorical (Nominal, Ordinal) or Numerical (Discrete, Continuous; Interval, Ratio).
- **Data scales**: Nominal < Ordinal < Interval < Ratio (each higher level supports more arithmetic).
- **Population (N)** vs **Sample (n)**; **Parameter** (population) vs **Statistic** (sample).
- **Operational definition**: precise rule for measuring the variable (essential for reproducibility).

**Sampling methods** (probability)
- **Simple Random** — every unit equal chance (use random numbers/RAND()).
- **Systematic** — every k-th unit; k = N/n.
- **Stratified** — divide into strata (by gender/region/etc.), sample within each.
- **Cluster** — divide into clusters (geographic), sample whole clusters.

**Non-probability** (use with caution): Convenience, Judgmental, Quota, Snowball.

**Survey methods**: Personal interview (high cost, high quality), Telephone, Mail, Online (lowest cost, highest non-response).

**Errors**
- **Coverage error** (population frame missing units)
- **Non-response error** (selected units don't reply)
- **Sampling error** (chance variation across samples)
- **Measurement error** (badly worded questions, interviewer bias)

**Excel/Python pointers**
- Excel: `=RANDBETWEEN(1,N)` for SRS; `Data → Data Analysis → Sampling`.
- Python: `pandas.DataFrame.sample(n)`, `sklearn.model_selection.train_test_split` for stratified split.

---

## Session 2 — Organising and analysing data
**Source:** Levine T1 Ch. 2.

**For categorical variables**
- **Summary table**: counts/percentages.
- **Bar chart, Pie chart, Pareto chart** (Pareto = bar in descending order + cumulative line; powerful for "vital few" analysis).
- **Cross-tabulation (contingency table)** for two categorical variables; **side-by-side bar chart** to visualise.

**For numerical variables**
- **Frequency distribution** with classes (use *Sturges' rule*: classes ≈ 1 + 3.322 log₁₀ n).
- **Histogram, Polygon, Cumulative (ogive)**, **Stem-and-leaf** plot.
- **Time-series plot** (numerical vs time).
- **Scatter plot** for two numerical variables.

**Visualising sets of variables**
- Multidimensional contingency tables, side-by-side / stacked bar charts.
- **Drill-down** PivotTables in Excel.

**Best practices**
- Avoid 3-D effects, "chartjunk", non-zero baselines on bars, dual axes.
- Use color sparingly to highlight; label axes.

**Excel/Python pointers**
- Excel: PivotTable + PivotChart; `=FREQUENCY()`.
- Python: `pandas.crosstab`, `seaborn.histplot`, `seaborn.scatterplot`.

---

## Session 3 — Numerical Descriptive Measures
**Source:** Levine T1 Ch. 3 (alt: Black R1 Ch. 3, Aczel R2 Ch. 3).

**Central tendency**
- **Mean** $\bar{X} = \frac{\sum X_i}{n}$ — affected by outliers.
- **Median** = middle value; robust to outliers.
- **Mode** = most frequent value; can be multimodal.
- **Geometric mean** = $\left(\prod X_i\right)^{1/n}$ — for growth rates.

**Variation**
- **Range** = max − min.
- **Interquartile range (IQR)** = Q₃ − Q₁ (boxplot whiskers).
- **Variance** $S^2 = \frac{\sum (X_i-\bar{X})^2}{n-1}$ (sample) — note $n-1$ for unbiasedness.
- **Std deviation** $S = \sqrt{S^2}$.
- **Coefficient of variation** $CV = (S / \bar{X}) \times 100\%$ — for comparing variability across different units.

**Shape**
- **Skewness** = E[(X−μ)³]/σ³. >0 right-skewed (mean > median), <0 left-skewed.
- **Kurtosis** = E[(X−μ)⁴]/σ⁴. >3 leptokurtic (peaked, fat tails), <3 platykurtic.
- **Empirical rule (normal)**: ≈ 68 % within 1σ, 95 % within 2σ, 99.7 % within 3σ.
- **Chebyshev's rule** (any distribution): ≥ (1 − 1/k²) within k σ.

**Exploring data**
- **Five-number summary** (min, Q₁, median, Q₃, max).
- **Boxplot** highlights outliers.
- **z-score** $z = (X - \bar{X})/S$; |z| > 3 typically flagged.

**Population measures** (μ, σ²) — divide by N (not n−1).

**Covariance & correlation**
- $\text{Cov}(X,Y) = \frac{\sum (X_i-\bar{X})(Y_i-\bar{Y})}{n-1}$.
- **Pearson r** = Cov(X,Y)/(SₓSᵧ); range [−1, +1]; measures **linear** association only.

**Excel/Python pointers**
- Excel: `=AVERAGE`, `=MEDIAN`, `=STDEV.S`, `=VAR.S`, `=PERCENTILE.INC`, `=SKEW`, `=KURT`, `=CORREL`, `=COVARIANCE.S`.
- Python: `df.describe()`, `df.skew()`, `df.kurt()`, `df.corr()`.

---

## Session 4 — Basic Probability
**Source:** Levine T1 Ch. 4 (alt: Black R1 Ch. 4, Aczel R2 Ch. 2-3).

**Approaches to probability**
- **Classical (a priori)**: equally likely outcomes, P(A) = favourable/total.
- **Empirical (relative frequency)**: P(A) = #occurrences / #trials (Law of Large Numbers).
- **Subjective (Bayesian prior)**: degree of belief.

**Axioms**: 0 ≤ P(A) ≤ 1; P(S) = 1; for mutually exclusive A,B: P(A ∪ B) = P(A) + P(B).

**Rules**
- **Complement**: P(A') = 1 − P(A).
- **Addition (general)**: P(A ∪ B) = P(A) + P(B) − P(A ∩ B).
- **Multiplication (independent)**: P(A ∩ B) = P(A) × P(B).
- **Conditional**: P(A|B) = P(A ∩ B) / P(B) (B has happened).
- **Independence test**: A,B independent iff P(A|B) = P(A).

**Bayes' theorem**
$$P(A_i|B) = \frac{P(B|A_i) P(A_i)}{\sum_j P(B|A_j) P(A_j)}$$
- Use cases: medical testing (sensitivity, specificity → PPV), spam filtering, fraud detection.
- **Prior** × **Likelihood** ∝ **Posterior**.

**Counting rules**
- Permutation: $P(n,r) = n!/(n-r)!$ (order matters).
- Combination: $C(n,r) = n!/(r!(n-r)!)$ (order doesn't).

**Worked Bayes example**
- Disease prevalence 1 %, test sensitivity 99 %, specificity 95 %.
- P(Disease|+) = (0.99 × 0.01) / (0.99 × 0.01 + 0.05 × 0.99) ≈ **16.7 %** — counter-intuitive low PPV.

**Excel/Python**
- Excel: `=PERMUT()`, `=COMBIN()`.
- Python: `math.perm`, `math.comb`, `scipy.stats.bayes_mvs`.

---

## Session 5 — Discrete Probability Distributions
**Source:** Levine T1 Ch. 5 (alt: Black R1 Ch. 5, Aczel R2 Ch. 3).

**General**
- PMF $P(X = x)$, satisfies $\sum P(x) = 1$.
- **Expected value** $E(X) = \mu = \sum x \cdot P(x)$.
- **Variance** $\sigma^2 = \sum (x-\mu)^2 P(x)$; **σ** = √Var.

**Binomial distribution** B(n, p)
- $P(X=x) = \binom{n}{x} p^x (1-p)^{n-x}$.
- Mean = np; Variance = np(1−p).
- Use cases: defective items, conversions, yes/no.
- Conditions: fixed n, two outcomes, constant p, independent trials.
- Excel: `=BINOM.DIST(x, n, p, FALSE/TRUE)`.

**Poisson distribution** P(λ)
- $P(X=x) = \frac{e^{-\lambda} \lambda^x}{x!}$.
- Mean = Variance = λ.
- Models rare events per unit time/space (calls/hour, defects/m²).
- **Binomial → Poisson** when n large, p small, np = λ.
- Excel: `=POISSON.DIST(x, λ, FALSE/TRUE)`.

**Discrete uniform** P(X=x) = 1/k for k equally likely outcomes; mean = (k+1)/2.

**Worked example (binomial)**
- Click-through rate p = 2 %, send n = 500 emails. P(X ≥ 15) = 1 − BINOM.DIST(14, 500, 0.02, TRUE).

---

## Session 6 — Normal Distribution
**Source:** Levine T1 Ch. 6 (alt: Black R1 Ch. 6, Aczel R2 Ch. 4).

**Continuous probability**: PDF $f(x)$, P(X = a single point) = 0; probability = area under curve.

**Normal distribution** N(μ, σ²)
- Bell-shaped, symmetric about μ; defined by μ and σ.
- $f(x) = \frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}$.
- **Standardisation**: $Z = (X-\mu)/\sigma$ → N(0,1).
- 68-95-99.7 rule.

**Standard normal table usage**
- Find P(Z < z), P(Z > z), P(a < Z < b).
- Inverse: find z given probability (e.g., for 95th percentile, z ≈ 1.645).

**Other continuous**
- **Uniform**: f(x) = 1/(b−a) on [a,b]; mean = (a+b)/2; var = (b−a)²/12.
- **Exponential**: f(x) = λe^(−λx); mean = 1/λ; memoryless. Time between Poisson events.

**Worked example**
- Daily order volume X ~ N(1200, 150²). P(X > 1500) = P(Z > 2) ≈ **2.28 %**.

**Excel/Python**
- Excel: `=NORM.DIST(x, μ, σ, TRUE)`, `=NORM.S.INV(p)`.
- Python: `scipy.stats.norm.cdf`, `norm.ppf`.

---

## Session 7 — Sampling Distributions
**Source:** Levine T1 Ch. 7.

**Sampling distribution of the mean** $\bar{X}$
- $E(\bar{X}) = \mu$; $\sigma_{\bar{X}} = \sigma/\sqrt{n}$ (standard error).
- **Central Limit Theorem (CLT)**: for n ≥ 30 (or population already normal), $\bar{X}$ is approximately normal regardless of population shape.
- Implication: as n increases, sampling distribution narrows; precision improves with √n.

**Sampling distribution of the proportion** $p$
- $E(p) = π$; $\sigma_p = \sqrt{π(1-π)/n}$.
- Approximately normal when nπ ≥ 5 and n(1−π) ≥ 5.

**Why it matters**
- Foundation of all inferential statistics. Every test/CI uses a sampling distribution.

**Finite Population Correction (FPC)** = √((N−n)/(N−1)); apply when n/N > 5 %.

---

## Session 8 — Confidence Interval Estimation
**Source:** Levine T1 Ch. 8.

**CI for mean (σ unknown)** — small/large samples
$$\bar{X} \pm t_{\alpha/2,\,n-1} \cdot \frac{S}{\sqrt{n}}$$
- Use **t-distribution** with n−1 degrees of freedom; t > z (wider CI to reflect extra uncertainty from estimating σ).
- 95 % CI ⇒ α = 0.05, t-critical from table.

**CI for proportion**
$$p \pm z_{\alpha/2} \cdot \sqrt{\frac{p(1-p)}{n}}$$

**Determining sample size**
- For mean: $n = \left(\frac{z_{\alpha/2}\,\sigma}{e}\right)^2$ (e = margin of error).
- For proportion: $n = \frac{z_{\alpha/2}^2 \cdot π(1-π)}{e^2}$ (use π = 0.5 for max n if unknown).

**Interpretation pitfalls**
- "95 % CI" means 95 % of such intervals constructed from repeated samples will contain μ — NOT "95 % probability μ is in this interval".

**Worked example**
- Sample n = 50, $\bar{X}$ = 4.2, S = 1.1, want 95 % CI: 4.2 ± 2.01 × 1.1/√50 = **4.2 ± 0.31**.

**Excel/Python**
- Excel: `=CONFIDENCE.T(α, S, n)`.
- Python: `scipy.stats.t.interval(0.95, n-1, loc=xbar, scale=S/sqrt(n))`.

---

> **Mid-Semester scope ends here (Sessions 1–8).** Closed Book, 2 hrs, 30 % weight, 20-Jun-2026 (FN).

---

## Session 9 — Fundamentals of Hypothesis Testing
**Source:** Levine T1 Ch. 9 (alt: Black R1 Ch. 9, Aczel R2 Ch. 7).

**Methodology (7 steps)**
1. State H₀ and H₁ (research question).
2. Choose α (typically 0.05 or 0.01).
3. Choose test statistic (z, t, χ², F).
4. State decision rule (critical region).
5. Collect data, compute test statistic.
6. Compare to critical value or compute p-value.
7. Decide: reject/fail to reject H₀; interpret in business terms.

**Errors**
- **Type I (α)** — reject H₀ when true (false positive).
- **Type II (β)** — fail to reject H₀ when false (false negative).
- **Power** = 1 − β. Increases with n, effect size, α.

**t-test for mean (σ unknown), two-tail**
$$t = \frac{\bar{X} - \mu_0}{S/\sqrt{n}}, \; df = n-1$$
- One-tail tests: directional H₁ (μ > μ₀ or μ < μ₀).

**Z-test for proportion**
$$Z = \frac{p - \pi_0}{\sqrt{\pi_0 (1-\pi_0)/n}}$$

**p-value**: probability of observing data as extreme as (or more than) the sample, *assuming H₀ true*. p < α ⇒ reject H₀.

---

## Session 10 — Two-sample tests and ANOVA
**Source:** Levine T1 Ch. 10 (alt: Black R1 Ch. 10-11, Aczel R2 Ch. 8-9).

**Two means (independent populations)**
- **Pooled-variance t** (assumes equal σ²):
  $$t = \frac{(\bar{X}_1 - \bar{X}_2)}{\sqrt{S_p^2 (1/n_1 + 1/n_2)}}, \; df = n_1+n_2-2$$
- **Separate-variance (Welch) t** when σ² unequal.

**Two means (related/paired)**
- Compute differences D, treat as one-sample t-test on $\bar{D}$.
- Use cases: before-after, matched pairs.

**Two proportions** — Z-test using pooled p̂.

**F-test for two variances**
$$F = S_1^2 / S_2^2,\; df_1 = n_1-1, df_2 = n_2-1$$

**One-way ANOVA**
- Tests equality of k means: H₀: μ₁ = μ₂ = … = μ_k.
- F = MS_between / MS_within; Reject if F > F_critical(k−1, n−k).
- Assumptions: independence, normality, equal variances.
- **Post-hoc**: Tukey's HSD to identify which pairs differ.

| Source | df | SS | MS | F |
|--------|---:|----|----|---|
| Between groups | k − 1 | SSB | MSB | MSB/MSW |
| Within groups | n − k | SSW | MSW |  |
| Total | n − 1 | SST |  |  |

**Excel**: `Data → Data Analysis → ANOVA: Single Factor`.
**Python**: `scipy.stats.f_oneway`, `statsmodels.stats.multicomp.pairwise_tukeyhsd`.

---

## Session 11 — Chi-square test
**Source:** Levine T1 Ch. 11.

**Chi-square family** uses categorical data; statistic $\chi^2 = \sum \frac{(O - E)^2}{E}$.

**Test for difference in two proportions** — equivalent to z-test, df = 1.

**Test for difference in > 2 proportions** — df = c − 1 (c = # of groups).

**Test of independence (contingency table)**
- H₀: variables independent.
- df = (r−1)(c−1).
- E_ij = (row total × column total) / grand total.
- Caveat: each E_ij ≥ 5 (else use Fisher's exact test or merge categories).

**Goodness of fit**
- Compares observed counts to expected from a hypothesised distribution (e.g., uniform, Poisson).
- df = k − 1 − (# parameters estimated).

**Excel**: `=CHISQ.TEST(observed, expected)` for p-value.

---

## Session 12 — Other Non-parametric tests
**Source:** Class Notes (also covered in Levine Ch. 12 / online supplements).

**When to use non-parametric**
- Data are ordinal, or
- Distributional assumptions of parametric tests violated, or
- Small samples without clear normality.

**Sign Test** (one-sample / paired median)
- Count positive vs negative differences from hypothesised median.
- Apply binomial with p = 0.5.

**Wilcoxon Rank-Sum Test (a.k.a. Mann-Whitney U)** — two independent samples
- Combine, rank all observations, sum ranks for sample 1.
- Tests whether two populations have the same distribution (specifically median).
- Non-parametric alternative to two-sample t.

**Wilcoxon Signed-Rank Test** — paired samples (uses signed differences and ranks).

**Kruskal-Wallis Test** — three or more independent samples
- Non-parametric ANOVA alternative.
- Statistic H ≈ χ² with k − 1 df.

**Spearman Rank Correlation**
- $r_s = 1 - \frac{6 \sum d_i^2}{n(n^2-1)}$ where d_i = rank(X_i) − rank(Y_i).
- Measures monotonic (not necessarily linear) association.
- Robust to outliers; works on ordinal data.

**Quick selector**
| Question | Parametric | Non-parametric |
|---------|-----------|----------------|
| 1 sample mean/median | 1-sample t | Sign / Wilcoxon Signed-Rank |
| 2 indep. groups | 2-sample t | Mann-Whitney U |
| Paired groups | Paired t | Wilcoxon Signed-Rank |
| 3+ groups | One-way ANOVA | Kruskal-Wallis |
| Linear association | Pearson r | Spearman r_s |

**Python**: `scipy.stats.mannwhitneyu`, `wilcoxon`, `kruskal`, `spearmanr`.

---

## Session 13 — Validating regression assumption & normality testing
**Source:** Levine T1 Ch. 13 (alt: Black R1 Ch. 14, Aczel R2 Ch. 10-11).
*(Handout titles S13 as "Validating…" but its sub-topics are regression fundamentals — see header note.)*

**Types of regression models**
- Simple linear: $Y = \beta_0 + \beta_1 X + \epsilon$.
- Multiple linear: $Y = \beta_0 + \beta_1 X_1 + \dots + \beta_k X_k + \epsilon$.
- Polynomial / interaction terms.

**OLS estimation**
- $\hat{\beta}_1 = \frac{\text{SSXY}}{\text{SSX}}$; $\hat{\beta}_0 = \bar{Y} - \hat{\beta}_1 \bar{X}$.

**Measures of variation**
- **SST** = Σ(Y − Ȳ)² (total).
- **SSR** = Σ(Ŷ − Ȳ)² (regression).
- **SSE** = Σ(Y − Ŷ)² (error).
- **Coefficient of Determination** $R^2 = SSR/SST$ — proportion of variation explained by regression.
- Adjusted R² penalises for adding predictors: $R_{adj}^2 = 1 - \frac{(1-R^2)(n-1)}{n-k-1}$.

**Standard error of estimate** $S_{YX} = \sqrt{SSE/(n-2)}$.

**Inference on slope**
- t-test: $t = \hat{\beta}_1 / S_{\hat{\beta}_1}$, df = n−2.
- F-test: F = MSR/MSE.

**Assumptions (LINE)**
- **L**inearity — relationship is linear.
- **I**ndependence of errors.
- **N**ormality of errors (residuals ε).
- **E**qual variance of errors (homoscedasticity).

---

## Session 14 — Linear Regression — diagnostics
**Source:** Class Notes (Levine Ch. 13 and supplements).

**Residuals = observed − predicted**: $e_i = Y_i - \hat{Y}_i$.

**Visual diagnostics**
- **Residuals vs Fitted** plot: random scatter ⇒ linearity & equal variance OK; funnel shape ⇒ heteroscedasticity; curve ⇒ non-linearity.
- **Q-Q plot** of residuals vs normal: straight line ⇒ normality OK.
- **Residuals vs time (or sequence)**: detects autocorrelation.

**Heteroscedasticity** (non-constant variance)
- Detection: residual plots; **Breusch-Pagan test**, **White test**.
- Fix: log/Box-Cox transform Y; weighted least squares (WLS); robust standard errors.

**Autocorrelation** (residuals correlated)
- Detection: **Durbin-Watson** test (DW ≈ 2 ⇒ no autocorr; <2 positive; >2 negative).
- Fix: add lag terms; Cochrane-Orcutt procedure.

**Normality testing** (errors)
- **Shapiro-Wilk test** — best for small samples (n < 50). H₀: data normal. p < α ⇒ reject normality.
- **Anderson-Darling test** — emphasises tail-fit; widely used.
- **Kolmogorov-Smirnov (KS) test** — compares empirical CDF to normal CDF; less powerful than SW.

**Python**: `from scipy.stats import shapiro, anderson, kstest`; `statsmodels.stats.diagnostic.het_breuschpagan, het_white`; `statsmodels.stats.stattools.durbin_watson`.

**Multicollinearity** (multiple regression)
- Variance Inflation Factor (VIF). VIF > 5–10 ⇒ problematic.

---

## Session 15 — Introduction to Linear Programming
**Source:** Class Notes (Anderson T2, Hillier R3, or Render R4).

**LP setup**
- **Decision variables** (x₁, x₂, …).
- **Objective function** Z to maximise/minimise (linear in variables).
- **Constraints** (≤, ≥, =) — also linear.
- **Non-negativity** x_i ≥ 0.

**Simple maximisation example**
> Maximise Z = 40x₁ + 30x₂ subject to:
> 4x₁ + 5x₂ ≤ 200 (machine hours)
> 2x₁ + 3x₂ ≤ 100 (labour hours)
> x₁, x₂ ≥ 0

**Graphical solution**
1. Plot constraints; identify **feasible region** (convex polygon).
2. Identify **corner/extreme points**.
3. Evaluate Z at each corner.
4. Optimal solution at one of the corner points (Fundamental Theorem of LP).

**Computer solution**
- **Excel Solver** (Simplex LP method) — `Data → Solver`.
- Online: **PHPSimplex**, **Lindo**, **GAMS**, Python `scipy.optimize.linprog` or `pulp`.

**Sensitivity analysis** (Solver output)
- **Shadow price** of a binding constraint = improvement in Z per unit increase of RHS.
- **Reduced cost** of a non-basic variable = penalty per unit forced into solution.
- **Allowable increase/decrease**: range over which current optimal basis stays valid.

**Special LP cases**
- Multiple optimal solutions (objective parallel to a constraint).
- Infeasibility (no point satisfies all constraints).
- Unbounded (feasible region open in direction of improvement).
- Degeneracy.

**Common applications**
- Product mix, blending, transportation, assignment, scheduling, portfolio optimisation.

---

## Session 16 — Revision

**Pre-mid-sem (closed book) checklist** — Sessions 1-8
- Standard normal Z-table application; computing P(Z<z), P(Z>z), P(a<Z<b).
- Computing μ, σ², CV, percentiles, IQR.
- Bayes' theorem 2x2 problems (medical/quality).
- Binomial vs Poisson selection; Poisson approximation conditions.
- CLT statement and applications.
- CI for mean (σ unknown, t-table) and proportion; sample-size formula.

**Pre-comprehensive (open book) checklist** — Sessions 9-16 + earlier
- Hypothesis testing 7-step framework; one- vs two-tail.
- Choosing the right two-sample test (independent vs paired, equal vs unequal variance).
- One-way ANOVA: F-statistic, source-table, post-hoc Tukey.
- Chi-square: goodness-of-fit vs independence (df differs!).
- Non-parametric selector table (this file → Session 12).
- Regression diagnostics: residual plots → which assumption violated → which fix.
- Normality tests: when to use SW vs AD vs KS.
- LP graphical method on 2-variable problem; Solver output interpretation.

**Reference cheat values**
- z-critical: 1.645 (90 %), 1.96 (95 %), 2.576 (99 %).
- Chebyshev: ≥ 75 % within 2σ; ≥ 89 % within 3σ.
- Empirical: 68/95/99.7 within 1σ/2σ/3σ.
- Power formula direction: ↑ n, ↑ effect, ↑ α → ↑ power.

**Open-book strategy (EC-3)**
- Tab the textbook by chapter; flag formulas you slow down on.
- Pre-print: Z-table, t-table, F-table, χ²-table.
- Bring a **non-programmable** scientific calculator (Casio FX-991EX is the WILP standard — non-programmable).

---

## Mandatory Experiential Learning resources (per handout)

### IIMA Case Centre cases
- **QM0284EX** — [Sankhosh Constructions Inc](https://cases.iima.ac.in/index.php/sankhosh-constructions-inc.html) (Sankaranarayanan)
- **PROD0331EX** — [Anugnyaa Agricultural Association](https://cases.iima.ac.in/download.php?file=media/downloads/4972/PROD0331_Inspection_Copy.pdf) (Sankaranarayanan)
- **CMHS0028** — [Understanding Lung Cancer – Tobacco Smoking Linkage](https://cases.iima.ac.in/index.php/understanding-lung-cancer-tobacco-smoking-linkage.html) (Roy & Laha)
- **QM0226** — Iron Ore Distribution for Steel Authority of India Limited (Kalro, Shukla, Tripathy, Raghuram)

### HSTalks videos (login via BITS WILP)
- [Fundamentals of Data Analysis](https://hstalks.com/t/3522/fundamentals-of-data-analysis/?business)
- [Predictive Analytics](https://hstalks.com/t/4282/predictive-analytics/?business)
- [The analytical framework and the four stages of data analysis](https://hstalks.com/t/5177/the-analytical-framework-and-the-four-stages-of-da/?business)
- [Failure and feedback in data analytics: lessons learnt, improvements made](https://hstalks.com/t/5077/failure-and-feedback-in-data-analytics-lessons-lea/?business)
