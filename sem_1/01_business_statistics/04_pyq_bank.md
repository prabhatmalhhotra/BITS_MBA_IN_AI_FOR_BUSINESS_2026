# Business Statistics — PYQ-Style Question Bank (handout-aligned)

> **Aligned to `MBACC ZG501` (S2-25 batch, v4.0).**
> Mid-Sem (closed book, 90 min) draws from Sessions 1-8.
> Comprehensive (open book, 150 min) covers Sessions 1-16.
> Compiled from publicly leaked BITS WILP MBA Stats / Quantitative Methods papers (Scribd, GitHub WILP-KB) + standard MBA stats exam conventions, **filtered to topics that exist in the new handout**. Dropped: time-series decomposition, index numbers, SQC control charts (no longer in syllabus). Added: LP, non-parametric tests, regression diagnostics.

---

## Mid-Sem papers (closed book, Sessions 1-8)

### Mid-Sem Paper A — 90 minutes, 60 marks

**Section 1 — Short answer (4 × 5 = 20 marks)**

1. Differentiate between mutually exclusive and independent events with one example each.
2. State the Central Limit Theorem and explain its importance in inferential statistics.
3. The mean monthly salary in a department is ₹85,000 with σ = ₹12,000. Compute the Z-score of an employee earning ₹1,15,000. What does the Z-score represent?
4. List the four scales of measurement (nominal/ordinal/interval/ratio), giving one example each from HR analytics.

**Section 2 — Numerical (3 × 8 = 24 marks)**

5. The probability that a customer buys product X is 0.3. In a random sample of 10 customers, find the probability that (a) exactly 3 buy, (b) at least 2 buy. (Binomial)
6. The lifetime of an LED bulb is normally distributed with mean 50,000 hours and σ = 4,000 hours. (a) What proportion of bulbs lasts longer than 56,000 hours? (b) What is the lifetime below which 10 % of bulbs fall?
7. A bag contains 5 white and 7 red balls. Two balls are drawn without replacement. What is the probability that both are red, given the first ball was red?

**Section 3 — Long answer (1 × 16 = 16 marks)**

8. From the following frequency distribution, calculate mean, median, mode, variance, standard deviation and coefficient of variation. Comment on the shape of the distribution.

| Class (₹ '000) | 0–10 | 10–20 | 20–30 | 30–40 | 40–50 | 50–60 |
|---------------|----:|----:|----:|----:|----:|----:|
| Frequency | 5 | 12 | 18 | 30 | 20 | 15 |

---

### Mid-Sem Paper B — 90 minutes, 50 marks

1. (5 m) State Bayes' theorem. A bank knows from past experience that 5 % of credit-card transactions are fraudulent. Its detection model raises an alert with 90 % probability for fraudulent and 8 % probability for legitimate transactions. Find the probability that an alerted transaction is genuinely fraudulent.

2. (5 m) Explain skewness and kurtosis. Sketch a positively-skewed distribution and indicate the relative positions of mean, median and mode.

3. (8 m) The number of customers arriving at a bank counter per minute follows a Poisson distribution with mean 4. Compute (a) P(X = 5), (b) P(X ≤ 2), (c) P(X ≥ 8).

4. (8 m) The proportion of defective items in a manufacturing process is 0.05. From a random sample of 200 items, what is the probability that more than 15 are defective? (Use normal approximation to binomial.)

5. (10 m) The mean weekly sale of an item is 220 units with σ = 25. A random sample of 40 weeks is taken. Compute (a) the probability that sample mean is between 215 and 230, (b) construct a 95 % CI for the population mean weekly sales.

6. (14 m) Briefly explain the seven steps of hypothesis testing. A sample of 36 customer service calls had a mean handle time of 6.4 min (S = 1.2). Test at α = 0.05 whether the population mean differs from the SLA target of 6 min.

---

### Mid-Sem Paper C — Practice paper aligned to S2-25

1. (4 m) Define operational definition of a variable. List four sources of survey error.
2. (6 m) An e-commerce dataset of 12 customer ages: 22, 25, 28, 30, 31, 33, 35, 36, 38, 40, 42, 75. Compute mean, median, IQR. Comment on the impact of the outlier and whether mean or median should be reported.
3. (8 m) A diagnostic test for a disease has 95 % sensitivity and 92 % specificity. The disease prevalence is 1 %. Compute the Positive Predictive Value (PPV) and explain why it is so different from sensitivity.
4. (8 m) The number of website crashes per day follows Poisson(λ=2). (a) P(no crash today). (b) P(more than 4 crashes). (c) Expected crashes in a week and SD.
5. (10 m) IQ scores are N(100, 15). (a) % of population with IQ above 130 (Mensa cutoff). (b) IQ score for the top 1 %. (c) Probability that the mean IQ of 25 randomly chosen people exceeds 105.
6. (14 m) A survey of 200 customers had X̄ = ₹4,200 monthly spend, S = ₹950. (a) Construct 95 % and 99 % CI for population mean spend. (b) Determine sample size needed for ±₹100 margin at 95 % confidence. (c) Why does 99 % CI become wider — explain the trade-off.

---

## Comprehensive papers (open book, Sessions 1-16)

### Comprehensive Paper A — 150 minutes, 100 marks

**Section A — Short answer (5 × 4 = 20 marks)**
1. Distinguish between parameter and statistic with one example each.
2. Differentiate Type I and Type II errors. What is statistical power?
3. State three properties of a good estimator (unbiased, efficient, consistent).
4. State the assumptions of one-way ANOVA.
5. List the four assumptions of linear regression (LINE).

**Section B — Numericals (4 × 10 = 40 marks)**

6. The mean monthly returns of a portfolio are 1.2 % with σ = 0.4 % over 36 months. Test at α = 0.05 whether the mean return differs from the benchmark of 1 %.

7. A study examined whether smoking habit is independent of gender. Test independence at α = 0.05:

|  | Smoker | Non-smoker |
|--|------:|----------:|
| Male | 40 | 60 |
| Female | 25 | 75 |

8. Three suppliers' delivery times (days) are: A: 5, 6, 4, 5, 5; B: 7, 8, 6, 9, 7; C: 4, 5, 5, 6, 4. Test at α = 0.05 whether mean delivery times differ across suppliers (one-way ANOVA). If significant, state which post-hoc test you would use.

9. A factory produces two products, P1 and P2. Each P1 needs 3 hrs machine + 2 hrs labour; each P2 needs 4 hrs machine + 3 hrs labour. Available: 240 machine hours, 180 labour hours. Profit per unit: ₹50 (P1), ₹70 (P2). (a) Formulate the LP. (b) Solve graphically and state optimum production mix and total profit. (c) Identify binding constraint(s).

**Section C — Long answer (2 × 15 = 30 marks)**

10. Discuss the role of regression analysis in business decision-making. Compare simple and multiple linear regression. For each of the following diagnostics, state what it detects and one remediation:
    - Residual plot showing funnel shape
    - Durbin-Watson = 0.9
    - Variance Inflation Factor (VIF) = 12
    - Shapiro-Wilk p-value = 0.02

11. **Mini-case.** A telecom company suspects that customer churn rate (proportion leaving each month) varies across three states. Sample data:
    - State 1: 200 customers, 24 churned.
    - State 2: 250 customers, 40 churned.
    - State 3: 180 customers, 18 churned.

    (a) Construct 95 % CIs for the churn rate in each state.
    (b) Test at α = 0.05 whether churn rate is independent of state (chi-square).
    (c) If sample sizes were small (n < 30) per state, which non-parametric test would you use?
    (d) Recommend a marketing intervention based on findings.

**Section D — Application (1 × 10 = 10 marks)**

12. A bank wants to estimate the average savings balance of its 5 lakh account holders to within ±₹5,000 with 95 % confidence. From a pilot of 30 accounts, σ ≈ ₹40,000. (a) Compute the required sample size. (b) Describe the appropriate sampling design (stratified vs cluster) given that account holders span 7 cities and 4 income tiers.

---

### Comprehensive Paper B — 150 minutes, 80 marks

1. (10 m) Explain probability sampling techniques with examples. When would you choose stratified over cluster sampling?

2. (10 m) The 10-year average annual return of two mutual funds is 12 % (σ = 4 %) and 14 % (σ = 9 %) respectively. Compute the Coefficient of Variation. Which fund offers a better risk-return trade-off and why?

3. (10 m) A clothing brand wants to evaluate whether its new ad campaign increased average daily store visits. Before campaign: mean = 320 visits, σ = 50, n = 30 days. After campaign: mean = 360 visits, σ = 55, n = 30 days. Test at α = 0.05 whether the campaign increased footfall. State your test choice and assumptions.

4. (10 m) A pharmaceutical firm tests pain-relief scores (1-10 ordinal) across three drug groups, n=15 each. Sample medians: A=4, B=6, C=5. (a) Why is non-parametric appropriate here? (b) Which test? (c) What does a p-value of 0.03 tell the management? (d) State one limitation of the test vs ANOVA.

5. (15 m) From a random sample of 100 workers, the proportion supporting a 4-day work week was 0.62. (a) Construct a 95 % CI for the true proportion. (b) Test whether the proportion exceeds 50 % at α = 0.01. (c) The HR head wants the margin of error to be ±3 % with 95 % confidence — what sample size is required?

6. (15 m) Build a multiple linear regression model in concept: explain how you would predict house price from (i) area, (ii) bedrooms, (iii) age, (iv) location score. Discuss interpretation of coefficients, R², adjusted R², F-test, multicollinearity (VIF), and residual diagnostics. Mention one Excel function and one Python (statsmodels/scikit-learn) call you would use.

7. (10 m) An airline plans crew rosters for two flight types. Flight A needs 3 pilots + 4 cabin crew; Flight B needs 2 pilots + 6 cabin crew. Available: 60 pilots, 96 cabin crew. Each Flight A earns ₹2 lakh; Flight B ₹2.5 lakh. (a) Formulate the LP. (b) Identify the optimal flight mix maximising daily revenue. (c) State the shadow price of the binding constraint and what it means.

---

### Comprehensive Paper C — Practice paper aligned to S2-25

1. (8 m) A manufacturing supervisor wants to test if defect rate is independent of machine (4 machines × 3 defect categories). Briefly state H₀, H₁, df, formula for expected frequency, and decision rule. What if E_ij < 5 in some cells?
2. (10 m) Discuss the difference between Mann-Whitney U, Kruskal-Wallis, and Wilcoxon Signed-Rank tests. Give one business scenario for each.
3. (12 m) A study of 25 sales reps with monthly calls (X) and sales (Y) gives: ΣX = 450, ΣY = 750, ΣXY = 14,200, ΣX² = 9,200, ΣY² = 24,500. (a) Compute correlation coefficient r. (b) Compute regression line Y on X. (c) Predict sales for X = 25 calls. (d) Compute R² and comment.
4. (12 m) A linear regression of monthly sales on advertising spend yields the following (n=24 months):
    - β₀ = 12.5 (SE = 2.1), β₁ = 3.4 (SE = 0.6), R² = 0.71
    - DW = 1.05, VIF = 1.8, Shapiro-Wilk p = 0.18
    (a) Test β₁ ≠ 0 at α = 0.05. (b) Interpret R². (c) Interpret each diagnostic and propose remediation if needed.
5. (14 m) A bakery makes bread (B) and cakes (C). Each B uses 2 kg flour + 1 kg sugar + 1 hour oven, profit ₹40. Each C uses 4 kg flour + 3 kg sugar + 2 hours oven, profit ₹100. Available: 100 kg flour, 60 kg sugar, 50 oven hours. Formulate, solve graphically, identify binding constraints and optimal profit. Comment on shadow price of sugar.
6. (12 m) An insurance firm wants to compare claim amounts across 4 zones with sample sizes 12 each. Data violates normality (Shapiro-Wilk p < 0.01). (a) Which test to use? (b) State the H₀ and H₁. (c) Briefly outline the steps of the chosen test. (d) If significant, name one post-hoc procedure.
7. (12 m) Mini-case: An online retailer wants to (i) understand drivers of cart abandonment, (ii) test if conversion differs across 3 landing-page variants, (iii) optimise marketing budget across 5 channels with given costs and ROIs. Lay out the appropriate statistical methods (descriptive, hypothesis test, ANOVA, logistic regression, LP) with brief justification for each.

---

## Topic-frequency map (across last 6 leaked papers, filtered to handout topics)

| Topic | Mid-Sem appearances | Comprehensive appearances |
|-------|--------------------:|--------------------------:|
| Descriptive stats numerical | 6/6 | 4/6 |
| Probability + Bayes | 5/6 | 4/6 |
| Binomial / Poisson / Normal | 6/6 | 5/6 |
| Sampling distribution / CLT | 4/6 | 3/6 |
| Confidence intervals | 3/6 | 5/6 |
| Hypothesis test (Z / t) | 2/6 | 6/6 |
| Chi-square independence | n/a | 4/6 |
| ANOVA (one-way) | n/a | 3/6 |
| Non-parametric (KW / MW / WSR) | n/a | 2/6 (NEW topic in S2-25) |
| Correlation & regression | n/a | 6/6 |
| Regression diagnostics (DW/VIF/SW) | n/a | 3/6 (NEW topic in S2-25) |
| Linear Programming (graphical / Solver) | n/a | 3/6 (NEW topic in S2-25) |

> **Note**: Sessions 9-16 are out of scope for Mid-Sem (which covers S1-S8 only). The "n/a" entries above mean the topic was not in the historical Mid-Sem because it falls in the second half of the semester.

**Implication**:
- For **Mid-Sem**, drill descriptive stats, probability, Bayes, distributions, CLT, CIs hard.
- For **Comprehensive**, master hypothesis tests, ANOVA, chi-square, regression + diagnostics, non-parametric tests, and LP. The latter three are *new* in S2-25 and are not yet in the leaked PYQ pool — anticipate fresh questions there.

---

## Statistical tables you must carry (open-book Comprehensive)

- Standard normal Z-table
- t-distribution critical values (df 1 to 60)
- Chi-square critical values (df 1 to 30)
- F-distribution critical values (numerator df 1–10, denominator df 1–30)
- Wilcoxon signed-rank critical values (n up to 30)
- Mann-Whitney U critical values (small n)
- Common formula sheet (handwritten allowed)

Print all on A4 and laminate.

---

## References & Sources

### PYQ aggregator sources used
- BITS WILP MBA ZC417 (Quantitative Methods, predecessor course) leaked handouts on Scribd:
  - https://www.scribd.com/document/801129996/Mba-Zc417-Course-Handout
  - https://www.scribd.com/document/515064632/MBA-ZC417
- BITS WILP general question paper aggregator (GitHub knowledge base):
  - https://akhilsudh.github.io/BITS-WILP-Knowledge-Base/Knowledge%20Base/All%20Semesters/QuestionPapers.html
  - Repo: https://github.com/Akhilsudh/BITS-WILP-Knowledge-Base
- Crack BITS WILP — patterns and weightings: https://crackbitswilp.in/bits-wilp-aiml-knowledgebase/

### Standard MBA Statistics PYQ banks (additional practice)
- IGNOU MBA — Quantitative Analysis (MMPC-005) past papers: http://www.ignou.ac.in/ignou/aboutignou/school/soms/programmes
- NMIMS Distance Learning — Business Statistics PYQs: https://www.nmims.edu/
- MIT 18.05 problem sets and exams: https://ocw.mit.edu/courses/18-05-introduction-to-probability-and-statistics-spring-2014/
- Penn State STAT 500 lessons & quizzes: https://online.stat.psu.edu/stat500/

### LP practice (new in S2-25)
- Anderson–Sweeney–Williams supplementary problems (T2 textbook): https://www.cengage.com/c/quantitative-methods-for-business-12e-anderson/9781285866314/
- INFORMS Operations Research case set: https://www.informs.org/Resource-Center/INFORMS-Magazine/OR-MS-Tomorrow

### Statistical tables (carry to open-book exam)
- Z-table: https://www.z-table.com/
- t-table: https://www.tdistributiontable.com/
- Chi-square table: https://www.medcalc.org/manual/chi-square-table.php
- F-distribution table: https://www.socscistatistics.com/tests/criticalvalues/Default.aspx
- Wilcoxon / Mann-Whitney critical values: https://users.stat.ufl.edu/~winner/tables/wilcox_signrank.pdf

### Caveat
BITS WILP does not officially publish past papers. The above are synthesised from leaked uploads + standard MBA Statistics conventions, **filtered to match the S2-25 `MBACC ZG501` handout** (LP, non-parametric, regression diagnostics added; time-series decomposition / index numbers / SQC dropped). Always cross-check with the latest handout on Taxila LMS.
