# Business Statistics — One-Page Revision Sheet

> Print this. Carry it for open-book exam.

---

## Descriptive

| Quantity | Formula |
|----------|---------|
| Mean | x̄ = Σx / n |
| Sample variance | s² = Σ(x − x̄)² / (n − 1) |
| Sample SD | s = √s² |
| CV | (s / x̄) × 100% |
| Pearson skewness | 3(mean − median) / σ |
| IQR | Q3 − Q1 |
| Outlier rule | < Q1 − 1.5·IQR or > Q3 + 1.5·IQR |

## Probability rules

- P(A ∪ B) = P(A) + P(B) − P(A ∩ B)
- P(A ∩ B) = P(A) × P(B|A)
- Independent: P(A ∩ B) = P(A)P(B)
- Bayes: P(A|B) = P(B|A) P(A) / P(B)

## Distributions

| Dist | Mean | Variance | Use |
|------|-----:|---------:|-----|
| Bernoulli | p | p(1−p) | Single trial |
| Binomial(n,p) | np | np(1−p) | n trials |
| Poisson(λ) | λ | λ | Rare events |
| Uniform(a,b) | (a+b)/2 | (b−a)²/12 | Equal likelihood |
| Normal(μ,σ²) | μ | σ² | Default continuous |
| Exponential(λ) | 1/λ | 1/λ² | Waiting time |

Standard normal: Z = (X − μ)/σ.
68-95-99.7 rule.

## Sampling distributions

- σ_x̄ = σ/√n
- σ_p = √(p(1−p)/n)
- CLT: x̄ approximately normal for n ≥ 30.

## Confidence intervals

| Parameter | Formula |
|-----------|---------|
| μ (σ known) | x̄ ± Z·σ/√n |
| μ (σ unknown) | x̄ ± t_(α/2, n−1)·s/√n |
| π | p̂ ± Z · √(p̂(1−p̂)/n) |

Common Z: 90% → 1.645; 95% → 1.96; 99% → 2.576.

Sample-size:
- For mean: n = (Zσ/E)²
- For proportion: n = Z² p̂(1−p̂) / E²

## Hypothesis tests

| Test | Statistic | df |
|------|-----------|----|
| Z-mean (σ known) | (x̄ − μ₀)/(σ/√n) | — |
| t-mean (σ unknown) | (x̄ − μ₀)/(s/√n) | n−1 |
| Z-proportion | (p̂ − π₀)/√(π₀(1−π₀)/n) | — |
| 2-sample t (pooled) | (x̄₁ − x̄₂)/SE_pooled | n₁+n₂−2 |
| Paired t | d̄/(s_d/√n) | n−1 |
| χ² independence | Σ(O−E)²/E | (r−1)(c−1) |
| 1-way ANOVA F | MSB/MSW | (k−1, N−k) |

Reject if |stat| > critical OR p < α.

## Regression

- b₁ = Σ(x−x̄)(y−ȳ) / Σ(x−x̄)²
- b₀ = ȳ − b₁ x̄
- R² = SSR/SST = 1 − SSE/SST
- s_e = √(SSE/(n−2))
- t = b₁ / SE(b₁), df = n−2
- VIF > 10 → multicollinearity flag

## Time-series accuracy

- MAD = Σ|e|/n
- MSE = Σe²/n
- MAPE = (Σ|e/Y|)/n × 100%

Simple exponential smoothing: F_(t+1) = αY_t + (1−α)F_t.

## Indices

- Laspeyres = Σ(P_t Q_0)/Σ(P_0 Q_0) × 100
- Paasche = Σ(P_t Q_t)/Σ(P_0 Q_t) × 100
- Fisher = √(Laspeyres × Paasche)

## Critical values cheat (memorise)

| Z (two-tailed) | α = 0.10 | 0.05 | 0.01 |
|---|--:|--:|--:|
| | 1.645 | 1.96 | 2.576 |

| t (two-tailed, α = 0.05) | df = 10 | 20 | 30 | 60 | ∞ |
|---|--:|--:|--:|--:|--:|
| | 2.228 | 2.086 | 2.042 | 2.000 | 1.96 |

| χ² (α = 0.05) | df = 1 | 2 | 5 | 10 | 20 |
|---|--:|--:|--:|--:|--:|
| | 3.84 | 5.99 | 11.07 | 18.31 | 31.41 |

| F (α=0.05, df₁=2) | df₂ = 5 | 10 | 20 | 30 |
|---|--:|--:|--:|--:|
| | 5.79 | 4.10 | 3.49 | 3.32 |

## Calculator quick keys (Casio FX-991EX)

- Mode → 6 (Statistics) → 1 (1-Var) → enter data → AC → OPTN
- 1: 1-Var summary (mean, σ, x̄)
- 4: Min/Max
- For regression: Mode → 6 → 2 (Y = a + bX)

## Last-90-second mental checks

1. Is the question asking for CI, hypothesis test, or just descriptive? Read again.
2. Two-tailed or one-tailed? Look for "differs" (two-tailed) vs "greater/less than" (one-tailed).
3. σ known → Z; σ unknown → t.
4. Round answers to 4 decimal places for probabilities, 2 for ₹.
5. State conclusion in business language.

---

## References & Sources

### Quick-reference resources
- NIST/SEMATECH e-Handbook of Statistical Methods (single page lookup): https://www.itl.nist.gov/div898/handbook/
- StatTrek formula sheet: https://stattrek.com/statistics/formulas
- Cheatography — Statistics Cheat Sheet: https://www.cheatography.com/explore/search/?search=statistics
- Real Statistics Excel formulas reference: https://real-statistics.com/

### Calculator and Excel
- Casio FX-991EX manual: https://support.casio.com/global/en/calc/manual/fx-991EX_570EX_en/
- Microsoft Excel statistical functions reference: https://support.microsoft.com/en-us/office/statistical-functions-reference-624dac86-a375-4435-bc25-76d659719ffd

### Visual learning (last-minute revision)
- 3Blue1Brown — Probability: https://www.3blue1bryan.com (note: official channel) https://www.youtube.com/c/3blue1brown
- StatQuest with Josh Starmer — concept videos: https://www.youtube.com/@statquest
