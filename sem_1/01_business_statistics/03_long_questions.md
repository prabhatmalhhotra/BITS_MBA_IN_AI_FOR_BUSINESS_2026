# Business Statistics — Long Questions (handout-aligned)

> 12-15 mark essay/problem prompts spanning the 16 sessions of `MBACC ZG501`. Use the answer skeletons to structure exam responses.

## Mid-Sem scope (Sessions 1-8)

### LQ-1 (Sessions 1-2) — Data collection and visualisation framework
**Prompt.** A retail chain wants to study purchase patterns across 50 cities. Discuss (a) appropriate sampling methods with rationale, (b) likely sources of error, (c) recommended data visualisations for both customer demographics and purchase amounts.

**Skeleton**: SRS vs Stratified vs Cluster comparison → recommendation (stratified by city tier + customer demographics; cluster within city for cost) → coverage/non-response/sampling/measurement error analysis → demographics: bar charts, pie, cross-tabs; purchase amounts: histogram, boxplot by city, time-series of monthly trend, scatter (basket size vs frequency).

### LQ-2 (Session 3) — Descriptive statistics interpretation
**Prompt.** For two stocks, compute and interpret mean, median, std deviation, CV, skewness, kurtosis. Explain why CV > σ for comparison and what skewness/kurtosis tell investors.

**Skeleton**: Compute formulas → CV makes returns comparable across stocks of different price levels → positive skewness (right tail = chance of big gains; downside loss bounded) → leptokurtic (fat tails = more extreme moves than normal) → recommend stock with higher Sharpe-like ratio adjusted for tail risk.

### LQ-3 (Session 4) — Bayes' theorem in business
**Prompt.** A bank's fraud detection model flags 2 % of transactions. True fraud rate is 0.5 %. Sensitivity 95 %, Specificity 98 %. Compute Positive Predictive Value (PPV) and discuss the operational implications.

**Skeleton**: 2x2 contingency setup → P(Fraud|+) = (0.95×0.005) / (0.95×0.005 + 0.02×0.995) ≈ 19.3 % → 81 % of flagged transactions are false positives → human-investigator workload, customer friction → mitigations: higher specificity threshold, multi-factor scoring, reduce friction via step-up authentication.

### LQ-4 (Session 5) — Discrete distribution problem
**Prompt.** A call centre receives on average 12 calls/hour. (a) P(exactly 10 calls in next hour). (b) P(at least 20 calls in next hour). (c) Justify Poisson assumption. (d) If conversion rate to sale is 15 %, expected sales per hour and its standard deviation (use binomial within Poisson hour).

**Skeleton**: Poisson(λ=12) → POISSON.DIST formulas → Poisson assumed because rare-event count over fixed time, independent arrivals, constant rate → conversions ~Binomial(n=12, p=0.15) compounded with Poisson → E[sales]=λp=1.8/hr, more rigorous: E=12·0.15=1.8, Var=12·0.15·0.85+0.15²·12 (compound Poisson) ≈ approximately 2.07.

### LQ-5 (Session 6) — Normal distribution applications
**Prompt.** Daily turnover of a delivery service is N(μ=320, σ=42) parcels. (a) Probability tomorrow's volume exceeds 400. (b) The 90th percentile of demand. (c) For staffing, the volume that has only 5 % probability of being exceeded.

**Skeleton**: (a) Z = (400-320)/42 = 1.905 → P(Z>1.905) ≈ 0.0284 ≈ 2.8 %; (b) z₉₀ = 1.282 → 320 + 1.282×42 ≈ 374 parcels; (c) z = 1.645 → 320 + 1.645×42 ≈ 389 parcels. Discuss buffer stock implications.

### LQ-6 (Session 7) — CLT & sampling distribution
**Prompt.** Population of customer wait times is right-skewed with μ = 8 min, σ = 4 min. (a) Distribution of sample mean for n=64. (b) P(X̄ > 9 min). (c) How would n=16 change conclusions? (d) Explain why CLT lets us use normal even for skewed populations.

**Skeleton**: X̄ ~ N(8, 4/√64 = 0.5²); P(X̄ > 9) = P(Z > 2) ≈ 2.28 %; n=16 gives SE=1, X̄ less reliably normal (CLT marginal); CLT theorem: as n→∞, distribution of X̄ approaches normal regardless of population shape; foundation of inferential statistics.

### LQ-7 (Session 8) — CI and sample-size determination
**Prompt.** Quality team measures 50 items: X̄ = 25.4 cm, S = 1.2 cm. (a) Construct 95 % CI for μ. (b) Construct 99 % CI. (c) Sample size needed for ±0.2 cm margin at 95 % confidence. (d) Interpret each CI in plain English.

**Skeleton**: t_(0.025, 49) ≈ 2.01 → 25.4 ± 2.01×0.17 ≈ (25.06, 25.74); 99 % CI wider; n = (1.96×1.2/0.2)² ≈ 139; "we are 95 % confident the true population mean lies in this interval" — meaning constructed via repeated sampling argument.

---

## Comprehensive scope (Sessions 9-16)

### LQ-8 (Session 9) — Hypothesis testing methodology
**Prompt.** A new manufacturing process claims to reduce defect rate from historical 4 % to lower. Sample of 500 items shows 14 defects. Test at α = 0.05 (one-tail) whether the new process is better.

**Skeleton**: H₀: π ≥ 0.04 vs H₁: π < 0.04; Z = (0.028 − 0.04)/√(0.04×0.96/500) = −1.376; critical z = −1.645; |Z| < critical → fail to reject H₀; p-value ≈ 0.084 > 0.05; conclusion: insufficient evidence to claim improvement at α=0.05; recommend larger sample.

### LQ-9 (Session 10) — Two-sample tests selection & ANOVA
**Prompt.** Three regional sales teams (A, B, C) with respective sample mean sales of 45, 52, 48 (₹ lakh) and SS values given. (a) Conduct one-way ANOVA. (b) If significant, what post-hoc test? (c) Why ANOVA instead of multiple t-tests?

**Skeleton**: Compute SSB, SSW, MSB, MSW, F = MSB/MSW; compare to F_critical; interpret; Tukey's HSD as post-hoc; ANOVA controls family-wise α (multiple t-tests inflate Type I error); state assumptions: independence, normality, equal variance (Levene's test).

### LQ-10 (Session 11) — Chi-square applications
**Prompt.** A survey of 400 customers cross-classified by age group (Young, Middle, Senior) and brand preference (A, B, C). (a) State H₀, H₁. (b) Compute expected frequencies. (c) Run chi-square test of independence (df). (d) Discuss managerial action if H₀ rejected.

**Skeleton**: H₀: age & brand preference independent vs H₁: associated; df = (3-1)(3-1) = 4; compute E_ij = row total × column total / N; χ² = Σ(O-E)²/E; compare to χ²_(0.05, 4) = 9.488; if reject → segment campaigns by age cohort.

### LQ-11 (Session 12) — Non-parametric test selection
**Prompt.** A pharmaceutical firm compares pain-relief scores (ordinal 1-10) across three drug groups, n=15 each. Discuss (a) why non-parametric is appropriate, (b) which test to use, (c) interpretation of p-value, (d) one limitation vs parametric ANOVA.

**Skeleton**: Ordinal data + small sample → can't assume normality → Kruskal-Wallis H test (non-parametric counterpart to one-way ANOVA); rank all observations across groups → compute H stat, compare to χ²_(k-1) df = 2 → reject H₀ if p < α; limitation: lower power than ANOVA when data truly normal; can't detect specific pair differences without post-hoc Dunn's test.

### LQ-12 (Sessions 13-14) — Regression & diagnostics
**Prompt.** You build a regression of monthly sales on advertising spend across 30 months. R² = 0.65, β₁ = 4.2 (SE=0.8). (a) Test β₁ ≠ 0 at α=0.05. (b) Interpret R² and β₁. (c) Discuss residual plot, Durbin-Watson = 1.1, Shapiro-Wilk p=0.04 — what each indicates and remediation.

**Skeleton**: t = 4.2/0.8 = 5.25, df=28, |t| > 2.05 → reject H₀; β₁: ₹4.2L sales per ₹1L ad spend; DW=1.1 → positive autocorrelation (likely seasonality, lag terms; Cochrane-Orcutt); SW p=0.04 → normality of residuals violated, log-transform Y or use bootstrap; possible heteroscedasticity → Breusch-Pagan, WLS; consider multiple regression with seasonal dummy.

### LQ-13 (Session 15) — Linear Programming formulation & solution
**Prompt.** A factory makes Product A and B. Each A needs 4 hrs machine + 2 hrs labour, profit ₹40. Each B needs 3 hrs machine + 5 hrs labour, profit ₹30. Available: 200 machine hours, 150 labour hours. (a) Formulate LP. (b) Solve graphically. (c) Identify binding constraints and shadow prices. (d) Comment on what to do if labour increases by 10 hrs.

**Skeleton**: Max Z = 40A + 30B s.t. 4A + 3B ≤ 200, 2A + 5B ≤ 150, A,B ≥ 0; identify corner points (0,0), (50,0), (0,30), and intersection of two constraints; intersection: solve 4A+3B=200, 2A+5B=150 → A=35.7, B=15.7; Z values at corners; optimal at intersection ≈ ₹1900; both constraints binding so both have positive shadow prices; for labour +10 hrs, ΔZ = shadow price × 10 (use sensitivity output).

### LQ-14 (Session 12, 13, 14 cross-cutting) — Choosing the right test
**Prompt.** For each scenario, identify the right statistical test:
1. Compare mean exam scores of two batches (n₁=40, n₂=35).
2. Compare median customer ratings (1-5 scale) across 4 cities (n=20 each).
3. Test if the proportion of female employees is the same across 3 departments.
4. Examine if salary is linearly associated with years of experience (continuous data).
5. Test if monthly returns of a stock are normally distributed.
6. Compare BP readings before & after a treatment in same patients.

**Skeleton**: 1) Two-sample t (independent) — possibly Welch if variances unequal; 2) Kruskal-Wallis (ordinal data); 3) Chi-square test for >2 proportions (df=2); 4) Pearson correlation + simple linear regression; 5) Shapiro-Wilk (n≤50) or Anderson-Darling; 6) Paired t-test (parametric) or Wilcoxon Signed-Rank (non-parametric).

### LQ-15 (Open-book strategic) — Comprehensive case (Sessions 1-16)
**Prompt.** A telecom firm wants to (a) understand churn drivers, (b) optimise customer-care staff scheduling, (c) compare retention rates across plans. Lay out an end-to-end statistical analysis plan touching: data definition/sampling, descriptive analysis, hypothesis testing, regression for churn drivers, ANOVA across plans, LP for staff scheduling, model diagnostics.

**Skeleton (use bullet points / framework)**:
1. **Data definition**: churn = no usage in 30 days; sampling = stratified by plan & tenure cohort (n=10,000).
2. **Descriptive**: histograms of usage, retention curves, summary stats.
3. **Hypothesis tests**: chi-square churn-vs-plan (categorical), 2-sample t for ARPU difference between churners/non-churners.
4. **Regression**: logistic regression on churn (0/1) with predictors — usage, tenure, complaints, plan type. Validate diagnostics (no perfect collinearity, residual normality not required for logistic).
5. **ANOVA**: one-way comparing retention rates across 5 plans; Tukey's post-hoc.
6. **LP for staffing**: Min staff cost subject to coverage constraints (peak vs off-peak); Excel Solver.
7. **Communication**: tabbed dashboard, clear recommendations on retention investment.
