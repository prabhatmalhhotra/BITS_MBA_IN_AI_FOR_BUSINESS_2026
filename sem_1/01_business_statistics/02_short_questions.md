# Business Statistics — Short Questions (with Answers)

> 35 short-answer questions, each worth 2–5 marks. Designed for EC-1 quizzes and the short-answer section of Mid-Sem / Comprehensive.

---

## Set A — Foundational concepts

**Q1. Differentiate between descriptive and inferential statistics.**
Descriptive summarises observed data (mean, σ, charts). Inferential uses sample data to draw conclusions about the population (CIs, hypothesis tests).

**Q2. List the four scales of measurement with examples.**
Nominal (gender), Ordinal (satisfaction 1–5), Interval (°C), Ratio (revenue).

**Q3. Define population, sample, parameter and statistic.**
Population = all elements; Sample = subset; Parameter = numeric summary of population (μ); Statistic = numeric summary of sample (x̄).

**Q4. State three differences between primary and secondary data.**
Primary is fresh, expensive, fit-for-purpose; Secondary is existing, cheap, may not match the exact need.

**Q5. Why do we use n−1 in sample variance?**
Bessel's correction: produces an unbiased estimate of population variance, since one degree of freedom is "spent" computing x̄.

---

## Set B — Descriptive statistics

**Q6. When is the median preferred over the mean?**
When data are skewed or contain outliers — median is robust; mean is pulled by extremes.

**Q7. Define coefficient of variation. Why is it useful?**
CV = (σ / μ) × 100%. Unit-free, lets us compare variability across data sets with different units (₹ vs kg).

**Q8. Distinguish positive and negative skew.**
Positive: long right tail, mean > median (income). Negative: long left tail, mean < median (easy exam).

**Q9. What is kurtosis? Name the three categories.**
Tailedness of distribution. Mesokurtic (normal), Leptokurtic (heavy tails), Platykurtic (thin tails).

**Q10. How are outliers identified using IQR?**
Outlier if value < Q1 − 1.5·IQR or > Q3 + 1.5·IQR.

---

## Set C — Probability

**Q11. State the addition rule for two non-mutually-exclusive events.**
P(A ∪ B) = P(A) + P(B) − P(A ∩ B).

**Q12. When are two events independent?**
P(A ∩ B) = P(A) · P(B), or equivalently P(A | B) = P(A).

**Q13. State Bayes' theorem.**
P(A | B) = [P(B | A) · P(A)] / P(B).

**Q14. A bag has 4 red and 6 blue balls. Two are drawn without replacement. P(both red)?**
(4/10) × (3/9) = 12/90 = 2/15 ≈ 0.133.

**Q15. What is the difference between mutually exclusive and independent events?**
Mutually exclusive: A and B cannot both occur (P(A ∩ B) = 0). Independent: occurrence of A doesn't change P(B). They are not the same; in fact, mutually exclusive events with positive probability are *not* independent.

---

## Set D — Distributions

**Q16. State the assumptions of the binomial distribution.**
Fixed n trials, two outcomes (success/failure), constant p, independent trials.

**Q17. When can a binomial be approximated by a Poisson?**
Large n (≥30), small p (≤0.05), np ≤ 10.

**Q18. What is the memoryless property of the exponential distribution?**
P(X > s + t | X > s) = P(X > t). Past waiting time doesn't affect future waiting time.

**Q19. Calculate P(Z ≤ 1.96) and P(−1.96 ≤ Z ≤ 1.96).**
P(Z ≤ 1.96) = 0.975; P(−1.96 ≤ Z ≤ 1.96) = 0.95.

**Q20. The mean and variance of a Poisson distribution are both equal to ___.**
λ.

---

## Set E — Sampling and CLT

**Q21. State the Central Limit Theorem.**
For a sufficiently large sample size (n ≥ 30), the sampling distribution of the sample mean is approximately normal with mean μ and SE σ/√n, regardless of the population distribution.

**Q22. Differentiate stratified and cluster sampling.**
Stratified: divide into homogeneous strata, sample from each. Cluster: divide into heterogeneous clusters, sample whole clusters. Stratified gives better precision; cluster is cheaper.

**Q23. Standard error of the sample mean is ___.**
σ/√n (or s/√n if σ unknown).

**Q24. To halve the standard error, sample size should be ___.**
Multiplied by 4 (since SE ∝ 1/√n).

---

## Set F — Estimation

**Q25. Interpret a 95% confidence interval (35, 45) for population mean.**
We are 95% confident that the population mean lies between 35 and 45 — meaning if we repeated the sampling process, ~95% of such intervals would contain μ.

**Q26. List 3 properties of a good estimator.**
Unbiased, consistent, efficient (also: sufficient).

**Q27. To estimate a proportion when no prior estimate of p is available, use p̂ = ___.**
0.5 (gives the most conservative, i.e., largest, sample size).

---

## Set G — Hypothesis testing

**Q28. Differentiate Type I and Type II errors.**
Type I: reject H₀ when true (false positive, controlled by α). Type II: fail to reject H₀ when false (false negative, β).

**Q29. What is power of a test?**
1 − β = probability of correctly rejecting a false H₀.

**Q30. Define p-value.**
Probability of observing a test statistic at least as extreme as the one computed, assuming H₀ is true.

**Q31. When do we use the t-distribution instead of Z?**
When σ is unknown and the sample is small (typically n < 30); also useful even for larger samples when σ unknown.

**Q32. State H₀ for a chi-square test of independence.**
The two categorical variables are independent (no association).

---

## Set H — Regression & forecasting

**Q33. State two assumptions of simple linear regression.**
(i) Linear relationship between X and Y; (ii) Errors are independent, normally distributed with constant variance (homoscedasticity).

**Q34. What does R² = 0.8 mean?**
80% of the variation in Y is explained by the regression on X.

**Q35. Define MAPE in forecasting.**
Mean Absolute Percentage Error = (Σ|(Actual − Forecast)/Actual| / n) × 100%. Lower is better; common forecast accuracy KPI.

---

## Bonus — One-liners often appearing in EC-1 quizzes

| Question | Answer |
|----------|--------|
| Mean of standard normal | 0 |
| Variance of standard normal | 1 |
| Sum of all probabilities in a distribution | 1 |
| df for one-sample t-test (n=20) | 19 |
| df for chi-square independence (3×4 table) | 6 |
| Critical Z for 99% two-tailed | ±2.576 |
| Sampling distribution shape for proportion (large n) | Approximately normal |
| Symmetry of normal distribution | Yes, around μ |
| Skewness of normal distribution | 0 |
| Kurtosis (excess) of normal | 0 |

---

## References & Sources

### Question patterns drawn from
- Anderson, Sweeney & Williams — chapter-end review questions and self-test problems.
- Levine — *Business Statistics: A First Course* — practice problem sets.
- Aczel & Sounderpandian — Indian-context numerical problems.
- BITS WILP MBA ZC417 sample question patterns (Scribd uploads, unverified): https://www.scribd.com/document/515064632/MBA-ZC417

### Practice resources
- OpenIntro Statistics — end-of-chapter exercises: https://www.openintro.org/book/os/
- Khan Academy practice exercises: https://www.khanacademy.org/math/statistics-probability
- StatTrek practice problems: https://stattrek.com/practice/quiz
- Investopedia for definitions cross-check: https://www.investopedia.com/financial-term-dictionary-4769738

### Calculator quick references
- Casio FX-991EX manual (statistics mode): https://support.casio.com/global/en/calc/manual/fx-991EX_570EX_en/
