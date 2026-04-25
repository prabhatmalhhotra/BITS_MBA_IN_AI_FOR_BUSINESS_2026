# Business Statistics — Long Questions

> 12 long-answer / numerical questions, each worth 10–15 marks. Each question is followed by a structured answer framework so you can replicate it under exam pressure.

---

### Q1. (15 marks) Explain the role of statistics in modern business decision-making with at least 5 functional examples. Discuss limitations of statistical analysis.

**Answer framework**

1. *Definition (2 m)* — Statistics is the science of collecting, organising, summarising, analysing and interpreting numerical data to support decision-making.
2. *Five functional examples (5 m)* —
   - **Marketing**: A/B testing of email campaigns, market-basket analysis, customer segmentation via cluster analysis.
   - **Operations**: Statistical process control charts, demand forecasting, EOQ.
   - **Finance**: Risk-return analysis (σ as risk), Monte Carlo simulation, beta estimation.
   - **HR**: Attrition modelling, hiring funnel analytics, engagement-survey analysis.
   - **Strategy**: Industry growth-rate analysis, market-share trends.
3. *Decision-making framework (3 m)* — Frame question → collect data → describe → infer → decide → monitor.
4. *Limitations (5 m)* —
   - Garbage-in / garbage-out — bad data nullifies analysis.
   - Statistical vs practical significance — p < 0.05 may have trivial business effect.
   - Correlation ≠ causation.
   - Non-quantifiable factors (culture, ethics) excluded.
   - Misuse: cherry-picking, p-hacking, misleading visualisations.

---

### Q2. (12 marks) From the following data on monthly sales of two salespeople over 6 months, compute mean, median, variance, standard deviation and coefficient of variation. Comment on consistency.

| Month | A (₹ lakh) | B (₹ lakh) |
|-------|-----------:|-----------:|
| 1 | 12 | 10 |
| 2 | 14 | 18 |
| 3 | 13 | 9 |
| 4 | 11 | 22 |
| 5 | 15 | 14 |
| 6 | 13 | 17 |

**Answer**

For A:
- Σx = 78 → Mean = 13.0
- Sorted: 11, 12, 13, 13, 14, 15 → Median = (13+13)/2 = 13.0
- Σ(x−x̄)² = 1 + 0 + 1 + 4 + 0 + 4 = 10 → s² = 10/5 = 2.0 → s = 1.41
- CV_A = (1.41 / 13.0) × 100 = **10.85%**

For B:
- Σy = 90 → Mean = 15.0
- Sorted: 9, 10, 14, 17, 18, 22 → Median = (14+17)/2 = 15.5
- Deviations: −5, 3, −6, 7, −1, 2 → Σd² = 25+9+36+49+1+4 = 124 → s² = 124/5 = 24.8 → s = 4.98
- CV_B = (4.98/15.0) × 100 = **33.20%**

**Comment**: A is far more consistent (CV ≈ 11%); B has higher mean but is highly variable (CV ≈ 33%). A salesperson is preferable when reliability matters; B for upside potential.

---

### Q3. (10 marks) A company manufactures 12% defective items. A random sample of 15 items is selected. Find the probability that (a) exactly 2 are defective, (b) at most 1 is defective, (c) at least 3 are defective.

**Answer**

X ~ Binomial(n = 15, p = 0.12).

(a) P(X = 2) = C(15, 2) × 0.12² × 0.88¹³ = 105 × 0.0144 × 0.1879 = **0.2841**

(b) P(X ≤ 1) = P(X=0) + P(X=1)
   = 0.88¹⁵ + 15 × 0.12 × 0.88¹⁴
   = 0.1470 + 15 × 0.12 × 0.1671
   = 0.1470 + 0.3008
   = **0.4478**

(c) P(X ≥ 3) = 1 − P(X ≤ 2) = 1 − [0.4478 + 0.2841] = 1 − 0.7319 = **0.2681**

---

### Q4. (12 marks) The lifetime of a bulb is normally distributed with mean 1,200 hours and standard deviation 100 hours. (a) What is the probability a bulb lasts > 1,400 hours? (b) Below 1,000 hours? (c) Between 1,100 and 1,300? (d) The company offers replacement on bulbs failing in the bottom 5% lifetime. What is the cutoff?

**Answer**

X ~ N(1200, 100²).

(a) Z = (1400 − 1200)/100 = 2.0; P(Z > 2.0) = 1 − 0.9772 = **0.0228** (~2.28%).

(b) Z = (1000 − 1200)/100 = −2.0; P(Z < −2.0) = **0.0228**.

(c) Z₁ = (1100 − 1200)/100 = −1; Z₂ = (1300 − 1200)/100 = 1; P(−1 < Z < 1) = 0.8413 − 0.1587 = **0.6826** (~68%).

(d) Bottom 5% → Z = −1.645; X = 1200 + (−1.645 × 100) = **1035.5 hours**.

---

### Q5. (10 marks) A sample of 50 transactions has mean ₹820 and standard deviation ₹120. Construct a 95% confidence interval for the population mean transaction value.

**Answer**

n = 50, x̄ = 820, s = 120. Use t-distribution (σ unknown), df = 49. t_(0.025, 49) ≈ 2.010.

CI = x̄ ± t × (s/√n) = 820 ± 2.010 × (120/√50) = 820 ± 2.010 × 16.97 = 820 ± 34.11

**CI = (₹785.89, ₹854.11)**.

We are 95% confident the population mean transaction value lies between ₹786 and ₹854.

---

### Q6. (15 marks) A bank claims its average customer wait time is ≤ 5 minutes. A consumer group surveys 36 customers and finds mean = 5.6 min, σ = 1.5 min. Test at α = 0.05 whether the bank's claim is supported.

**Answer**

H₀: μ ≤ 5 (claim valid). H₁: μ > 5 (claim violated). Right-tailed test.

n = 36 ≥ 30, σ given → use Z-test.

Z = (x̄ − μ₀) / (σ/√n) = (5.6 − 5) / (1.5/6) = 0.6 / 0.25 = **2.40**.

Critical value at α = 0.05 (right-tailed) = 1.645. Since 2.40 > 1.645, **reject H₀**.

p-value = P(Z > 2.40) = 1 − 0.9918 = 0.0082 < 0.05 → reject.

**Conclusion**: There is sufficient evidence at 5% level to reject the bank's claim. Average wait time exceeds 5 minutes.

---

### Q7. (12 marks) The following table shows survey results on preference for three brands across four cities. Test at α = 0.05 whether brand preference is independent of city. (Chi-square test of independence.)

| City \ Brand | A | B | C | Total |
|-----|----:|----:|----:|----:|
| Mumbai | 35 | 25 | 40 | 100 |
| Delhi | 50 | 30 | 20 | 100 |
| Bangalore | 30 | 45 | 25 | 100 |
| Chennai | 25 | 40 | 35 | 100 |
| Total | 140 | 140 | 120 | 400 |

**Answer**

H₀: Brand preference and city are independent. H₁: They are dependent.

Expected E_ij = (Row total × Column total) / Grand total.

Each row total = 100, so E for column A = 100×140/400 = 35; B = 35; C = 30. Same for every row.

| City | (O−E)²/E for A | for B | for C |
|------|---------------:|------:|------:|
| Mumbai | 0 | 2.857 | 3.333 |
| Delhi | 6.428 | 0.714 | 3.333 |
| Bangalore | 0.714 | 2.857 | 0.833 |
| Chennai | 2.857 | 0.714 | 0.833 |

χ² ≈ 0 + 2.857 + 3.333 + 6.428 + 0.714 + 3.333 + 0.714 + 2.857 + 0.833 + 2.857 + 0.714 + 0.833 ≈ **25.47**.

df = (4−1)(3−1) = 6. Critical χ²₀.₀₅,₆ = 12.59. Since 25.47 > 12.59, **reject H₀**.

**Conclusion**: Brand preference depends on city. Marketing strategy should be city-specific.

---

### Q8. (15 marks) The data below shows advertising spend (₹ lakh) and sales (₹ crore) for 8 quarters. Estimate the regression line, interpret slope and intercept, compute R², and predict sales when ad spend = 12.

| Ad spend (X) | 6 | 8 | 9 | 10 | 11 | 12 | 14 | 16 |
|-------------:|--:|--:|--:|--:|--:|--:|--:|--:|
| Sales (Y) | 4.0 | 5.5 | 6.0 | 6.5 | 7.5 | 7.8 | 9.0 | 10.5 |

**Answer**

n = 8. Σx = 86, x̄ = 10.75. Σy = 56.8, ȳ = 7.10.

Σ(x − x̄)² = 22.75 + 7.5625 + 3.0625 + 0.5625 + 0.0625 + 1.5625 + 10.5625 + 27.5625 = 73.6875.
(Computed: 4.75² + 2.75² + 1.75² + 0.75² + 0.25² + 1.25² + 3.25² + 5.25² ≈ 73.69)

Σ(x − x̄)(y − ȳ) = (−4.75)(−3.1) + (−2.75)(−1.6) + (−1.75)(−1.1) + (−0.75)(−0.6) + (0.25)(0.4) + (1.25)(0.7) + (3.25)(1.9) + (5.25)(3.4)
= 14.725 + 4.40 + 1.925 + 0.45 + 0.10 + 0.875 + 6.175 + 17.85 = 46.50.

b₁ = 46.50 / 73.69 ≈ **0.631**.
b₀ = 7.10 − 0.631 × 10.75 ≈ **0.317**.

Regression: **Y = 0.317 + 0.631 X**.

Interpretation: Each ₹1 lakh extra advertising spend yields ~₹63.1 lakh extra sales (since Y is in ₹ crore, slope is in crore/lakh = 63.1 lakh/lakh? — careful with units; with given units one extra unit of X (1 lakh) increases Y by 0.631 crore = ₹63.1 lakh.

For R²: SST = Σ(y − ȳ)² ≈ 9.61 + 2.56 + 1.21 + 0.36 + 0.16 + 0.49 + 3.61 + 11.56 = 29.56.
SSR = b₁ × Σ(x − x̄)(y − ȳ) = 0.631 × 46.50 ≈ 29.34.
R² = 29.34 / 29.56 ≈ **0.993** (~99%).

Prediction at X = 12: Y = 0.317 + 0.631 × 12 = **7.89 crore**.

---

### Q9. (10 marks) Quarterly sales (in ₹ crore) over 8 quarters: 50, 55, 53, 58, 62, 60, 65, 70. Apply 4-quarter moving average and 3-quarter weighted moving average (weights 0.5, 0.3, 0.2 for most recent, 2nd, 3rd). Compute MAD and MAPE for each.

**Answer**

**4-quarter MA forecasts** (centred for periods 5–8):

| Period | Actual | 4-MA forecast | Error |
|--------|-------:|--------------:|------:|
| 5 | 62 | (50+55+53+58)/4 = 54.0 | 8.0 |
| 6 | 60 | (55+53+58+62)/4 = 57.0 | 3.0 |
| 7 | 65 | (53+58+62+60)/4 = 58.25 | 6.75 |
| 8 | 70 | (58+62+60+65)/4 = 61.25 | 8.75 |

MAD = (8 + 3 + 6.75 + 8.75)/4 = 6.625
MAPE = mean(|e|/Y × 100) = mean(12.90, 5.00, 10.38, 12.50) = **10.20%**

**3-quarter weighted MA** (weights 0.5 to most recent):

Forecast for t = w₁·Y_(t−1) + w₂·Y_(t−2) + w₃·Y_(t−3).

| Period | Actual | Forecast | Error |
|--------|-------:|---------:|------:|
| 4 | 58 | 0.5×53 + 0.3×55 + 0.2×50 = 26.5+16.5+10 = 53.0 | 5.0 |
| 5 | 62 | 0.5×58 + 0.3×53 + 0.2×55 = 29+15.9+11 = 55.9 | 6.1 |
| 6 | 60 | 0.5×62 + 0.3×58 + 0.2×53 = 31+17.4+10.6 = 59.0 | 1.0 |
| 7 | 65 | 0.5×60 + 0.3×62 + 0.2×58 = 30+18.6+11.6 = 60.2 | 4.8 |
| 8 | 70 | 0.5×65 + 0.3×60 + 0.2×62 = 32.5+18+12.4 = 62.9 | 7.1 |

MAD = (5+6.1+1+4.8+7.1)/5 = 4.80
MAPE = mean(8.62, 9.84, 1.67, 7.38, 10.14) = **7.53%**

**Conclusion**: Weighted MA outperforms simple 4-MA on this data (lower MAD and MAPE), because it captures the rising trend.

---

### Q10. (15 marks) Three machines produce the same item. From production data:
- Machine A: 50 items sampled, 4 defective.
- Machine B: 60 items sampled, 9 defective.
- Machine C: 70 items sampled, 7 defective.

**(i) Test at 5% level whether the defective rates differ across machines (chi-square goodness-of-fit on independence).**
**(ii) Construct a 95% CI for the overall defective proportion.**

**Answer**

(i) Form a 2×3 contingency table:

|  | A | B | C | Total |
|--|--:|--:|--:|------:|
| Defective | 4 | 9 | 7 | 20 |
| Non-defective | 46 | 51 | 63 | 160 |
| Total | 50 | 60 | 70 | 180 |

Expected E_ij = Row total × Col total / Grand total.

Row totals: 20, 160. Col totals: 50, 60, 70.

E (Defective): 50×20/180 = 5.56, 60×20/180 = 6.67, 70×20/180 = 7.78.
E (Non): 44.44, 53.33, 62.22.

χ² = Σ (O−E)²/E
= (4−5.56)²/5.56 + (9−6.67)²/6.67 + (7−7.78)²/7.78 + (46−44.44)²/44.44 + (51−53.33)²/53.33 + (63−62.22)²/62.22
= 0.438 + 0.815 + 0.078 + 0.055 + 0.102 + 0.010 = **1.498**

df = (2−1)(3−1) = 2. Critical χ²₀.₀₅,₂ = 5.991. Since 1.498 < 5.991, **fail to reject H₀**.

**Conclusion**: No significant evidence at 5% that defective rates differ across machines.

(ii) Overall proportion p̂ = 20/180 = 0.1111. SE = √(0.1111 × 0.8889 / 180) = √(0.000549) = 0.0234.
95% CI = 0.1111 ± 1.96 × 0.0234 = 0.1111 ± 0.0459 = **(0.065, 0.157)** or 6.5%–15.7%.

---

### Q11. (12 marks) A retail chain wants to test whether store layout (3 types) affects average daily revenue. Daily revenue (₹ lakh) for 5 days each:
- Layout 1: 12, 14, 13, 15, 11
- Layout 2: 16, 18, 17, 15, 14
- Layout 3: 13, 12, 14, 11, 13

Conduct a one-way ANOVA at α = 0.05.

**Answer**

Means: Layout 1 = 13.0, Layout 2 = 16.0, Layout 3 = 12.6. Grand mean = 13.867.

Sum of Squares Between (SSB):
SSB = Σ nⱼ × (x̄ⱼ − x̄)² = 5 × [(13.0−13.867)² + (16.0−13.867)² + (12.6−13.867)²]
   = 5 × [0.752 + 4.551 + 1.605] = 5 × 6.908 = **34.54**

Sum of Squares Within (SSW):
For Layout 1: deviations −1, 1, 0, 2, −2 → 1+1+0+4+4 = 10
For Layout 2: 0, 4, 1, −1, −4 → 0+4+1+1+4? Recompute: (16−16)² + (18−16)² + (17−16)² + (15−16)² + (14−16)² = 0+4+1+1+4 = **10**
For Layout 3: (13−12.6)² + (12−12.6)² + (14−12.6)² + (11−12.6)² + (13−12.6)² = 0.16 + 0.36 + 1.96 + 2.56 + 0.16 = **5.20**
SSW = 10 + 10 + 5.20 = **25.20**

df_B = k − 1 = 2; df_W = N − k = 12.
MSB = 34.54 / 2 = 17.27. MSW = 25.20 / 12 = 2.10.
F = MSB / MSW = 17.27 / 2.10 = **8.22**.

Critical F_(0.05, 2, 12) = 3.89. Since 8.22 > 3.89, **reject H₀**.

**Conclusion**: At least one layout's mean revenue differs. Layout 2 looks superior; recommend post-hoc Tukey's HSD to confirm pairwise differences.

---

### Q12. (10 marks) Explain how Bayes' theorem is used in (i) medical diagnostics and (ii) spam filtering. Use a worked example for medical diagnostics with a disease prevalence of 1%, test sensitivity 99%, and specificity 95%.

**Answer**

Bayes flips conditionals: P(A | B) = [P(B | A) × P(A)] / P(B).

**(i) Medical diagnostics**: We know P(positive test | disease). We want P(disease | positive test).

Worked example:
- P(D) = 0.01, P(¬D) = 0.99.
- P(+ | D) = 0.99 (sensitivity), P(− | ¬D) = 0.95 → P(+ | ¬D) = 0.05 (false positive rate).
- P(+) = P(+|D)P(D) + P(+|¬D)P(¬D) = 0.99 × 0.01 + 0.05 × 0.99 = 0.0099 + 0.0495 = 0.0594.
- P(D | +) = 0.0099 / 0.0594 = **0.167** (~16.7%).

Even with a "99% accurate" test, only 1 in 6 positive results actually has the disease — because the disease itself is rare. This is the **base-rate fallacy**, and explains why mass screening uses two-stage protocols.

**(ii) Spam filtering**: Treat each word as evidence.
- P(spam | word_i) ∝ P(word_i | spam) × P(spam).
- Naive Bayes assumes word independence given class.
- Combine across words (via log probabilities) → final spam score.

Mature spam filters use millions of word-level priors trained on labelled email corpora. Despite the naive independence assumption, these models work surprisingly well in practice and form a foundational technique in modern ML.

---

## References & Sources

### Numerical patterns based on
- Anderson, Sweeney & Williams — chapter-end case problems.
- Levine — practice problems and case-style questions.
- Aczel & Sounderpandian — Indian business case problems.

### Worked-example libraries
- StatTrek worked examples: https://stattrek.com/tutorials/statistics-tutorial
- Real Statistics Using Excel (Charles Zaiontz): https://real-statistics.com/
- Penn State STAT 500 (full course): https://online.stat.psu.edu/stat500/
- MIT OCW 18.05 — Probability & Statistics: https://ocw.mit.edu/courses/18-05-introduction-to-probability-and-statistics-spring-2014/

### Topic-specific deep dives
- Bayes worked examples: https://betterexplained.com/articles/an-intuitive-and-short-explanation-of-bayes-theorem/
- Hypothesis testing intuition: https://www.scribbr.com/statistics/hypothesis-testing/
- Regression assumptions diagnostics: https://www.statisticssolutions.com/free-resources/directory-of-statistical-analyses/
- ANOVA primer: https://www.scribbr.com/statistics/anova/

### Indian business data for case practice
- RBI DBIE: https://dbie.rbi.org.in/
- NSE corporate data: https://www.nseindia.com/companies-listing/corporate-filings-financial-results
- Screener.in (free company financials): https://www.screener.in/
