# Business Statistics — Short Questions (handout-aligned)

> Aligned to `MBACC ZG501` 16-session plan. Mid-Sem (closed book) draws from S1-S8; Comprehensive (open book) from S1-S16.
> Each Q has a one- to three-line ideal answer to drill quickly.

## Session 1 — Defining and collecting data
1. **Distinguish parameter vs statistic.** Parameter is a numerical descriptor of population (μ, σ, π); statistic is its sample analogue (X̄, S, p) used to estimate the parameter.
2. **List four probability sampling methods.** Simple Random, Systematic, Stratified, Cluster.
3. **What is operational definition of a variable?** Precise rule for measuring it so different observers get the same value.
4. **State four sources of survey error.** Coverage, Non-response, Sampling, Measurement.
5. **When is stratified sampling preferable to SRS?** When the population has distinct sub-groups whose proportions you want preserved in the sample (improves precision per ₹).

## Session 2 — Organising and analysing data
6. **What is a Pareto chart used for?** Bars in descending order with cumulative line; identifies the "vital few" categories driving most of the impact.
7. **Sturges' rule for histogram classes.** k ≈ 1 + 3.322 log₁₀(n).
8. **Difference between histogram and bar chart.** Histogram for numerical data (touching bars, intervals); bar chart for categorical (gaps).
9. **Why avoid 3-D pie charts?** Distorts area perception → audience mis-reads the relative magnitudes.

## Session 3 — Numerical Descriptive Measures
10. **Why use n-1 in sample variance?** Bessel's correction — gives an unbiased estimator of population variance (degrees-of-freedom argument).
11. **Define coefficient of variation. When use it?** CV = σ/μ × 100 %. Compares variability across data sets with different units or means.
12. **What does kurtosis = 3 mean?** Mesokurtic — same peakedness as a normal distribution.
13. **State Chebyshev's rule.** For any distribution, ≥ (1 − 1/k²) of observations lie within k standard deviations of the mean.
14. **Pearson r limits and meaning.** Range [-1, +1]. ±1 perfect linear, 0 no linear relationship. Doesn't capture non-linear association.

## Session 4 — Basic Probability
15. **Define conditional probability.** P(A|B) = P(A ∩ B)/P(B), assuming P(B) > 0.
16. **State Bayes' theorem.** P(A|B) = [P(B|A)·P(A)] / Σ P(B|Aᵢ)·P(Aᵢ).
17. **A and B are independent. P(A∩B) = ?** P(A) × P(B).
18. **Difference between mutually exclusive and independent events.** Mutually exclusive: cannot occur together (P(A∩B)=0); Independent: occurrence of one doesn't affect the other (P(A|B)=P(A)).

## Session 5 — Discrete Probability Distributions
19. **Mean & variance of binomial B(n,p).** μ = np; σ² = np(1−p).
20. **Mean & variance of Poisson(λ).** μ = σ² = λ.
21. **When approximate Binomial by Poisson?** n large, p small, np = λ moderate (rule of thumb: n ≥ 20, p ≤ 0.05).
22. **Conditions for binomial.** Fixed n trials, two outcomes (S/F), constant p, independent trials.

## Session 6 — Normal Distribution
23. **Empirical rule.** ≈ 68 % within ±1σ, 95 % within ±2σ, 99.7 % within ±3σ for a normal distribution.
24. **Z-score formula and use.** Z = (X − μ)/σ. Standardises any normal variable to N(0,1) for table lookup.
25. **What property makes the exponential distribution special?** Memoryless: P(X > s+t | X > s) = P(X > t).

## Session 7 — Sampling Distributions
26. **State CLT.** For sample size n large enough (≥30 typically), the distribution of X̄ is approximately normal regardless of population shape.
27. **Standard error of mean.** σ/√n (or S/√n if σ unknown).
28. **When apply Finite Population Correction?** When n/N > 5 %; multiply SE by √((N−n)/(N−1)).

## Session 8 — Confidence Interval Estimation
29. **Why use t-distribution instead of z?** When σ unknown and we estimate it with S; t accounts for extra uncertainty (heavier tails).
30. **95 % CI formula for mean (σ unknown).** X̄ ± t_(α/2, n-1) · S/√n.
31. **Sample size formula for mean estimation.** n = (z_(α/2)·σ / e)².
32. **Common interpretation pitfall of CI.** Saying "there's a 95 % chance μ is in this CI" — wrong; the parameter is fixed; 95 % refers to long-run capture rate.

---

## Session 9 — Fundamentals of Hypothesis Testing
33. **State the 7 steps of hypothesis testing.** State H₀/H₁ → choose α → pick test stat → decision rule → collect data → compute → decide.
34. **Type I vs Type II error.** Type I = rejecting true H₀ (α); Type II = accepting false H₀ (β).
35. **What does p-value of 0.03 mean?** Probability of observing data as extreme as the sample if H₀ is true is 3 %.
36. **Power of test definition.** 1 − β; probability of correctly rejecting a false H₀.

## Session 10 — Two-sample tests and ANOVA
37. **When use paired t-test?** When observations are naturally pairwise related (before/after, matched pairs).
38. **F-test purpose.** Compare two variances; ratio S₁²/S₂² with df = n₁−1, n₂−1.
39. **One-way ANOVA H₀.** All k population means are equal: μ₁ = μ₂ = … = μ_k.
40. **What is Tukey's HSD?** Post-hoc multiple-comparison test to identify which pairs of means differ after a significant ANOVA.

## Session 11 — Chi-square test
41. **Expected count formula in contingency table.** E_ij = (row total × column total) / grand total.
42. **df for chi-square test of independence (r×c table).** (r − 1)(c − 1).
43. **Goodness-of-fit df.** k − 1 − (number of parameters estimated from data).
44. **When chi-square test is invalid.** When any expected frequency < 5 (use Fisher's exact instead, or merge categories).

## Session 12 — Other Non-parametric tests
45. **Non-parametric counterpart to two-sample t.** Mann-Whitney U / Wilcoxon Rank-Sum.
46. **Non-parametric counterpart to one-way ANOVA.** Kruskal-Wallis H test.
47. **Non-parametric counterpart to paired t.** Wilcoxon Signed-Rank.
48. **Spearman rank correlation formula.** r_s = 1 − [6 Σd_i² / (n(n²−1))] where d_i = rank difference.
49. **Why use non-parametric tests?** When normality assumption violated, data ordinal, or small samples.

## Session 13 — Regression assumption & normality testing
50. **List regression assumptions (LINE).** Linearity, Independence of errors, Normality of errors, Equal variance.
51. **What does R² = 0.78 mean?** 78 % of variation in Y is explained by the regression model.
52. **Adjusted R² vs R².** Adjusted R² penalises addition of predictors; better for comparing models with different numbers of variables.
53. **F-test in regression purpose.** Tests overall significance — at least one β_i ≠ 0.

## Session 14 — Linear Regression — diagnostics
54. **Detect heteroscedasticity from residual plot.** Funnel/cone shape (variance changing with fitted values).
55. **Durbin-Watson interpretation.** DW ≈ 2 → no autocorrelation; <2 positive; >2 negative.
56. **Best test of normality for small samples.** Shapiro-Wilk (also Anderson-Darling).
57. **What's VIF and threshold?** Variance Inflation Factor for multicollinearity; VIF > 5–10 problematic.
58. **Fix for heteroscedasticity.** Transform Y (log/Box-Cox), use weighted least squares, or use heteroscedasticity-robust SEs.

## Session 15 — Introduction to Linear Programming
59. **Three components of an LP.** Decision variables, linear objective function, linear constraints (+ non-negativity).
60. **Where does optimal LP solution lie?** At an extreme/corner point of the feasible region (Fundamental Theorem of LP).
61. **What is shadow price?** Improvement in objective function per unit increase in RHS of a binding constraint.
62. **What is reduced cost?** Penalty per unit forced into the optimal solution if a non-basic variable is brought in.
63. **Special LP cases.** Multiple optimal, infeasibility, unbounded, degeneracy.
64. **Excel tool for LP.** Solver add-in (use Simplex LP method for linear models).

## Session 16 — Revision (cross-cutting)
65. **Quick selector — categorical association test?** Chi-square test of independence.
66. **Open-book exam tactic.** Tab textbook by chapter; pre-print Z/t/F/χ² tables; flag formulas you slow down on.
