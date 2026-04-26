# Business Statistics — One-Page Revision Sheet (handout-aligned)

> Aligned to `MBACC ZG501` 16-session plan. Print this. Carry it for the **open-book Comprehensive** exam.

---

## Descriptive

| Quantity | Formula |
|----------|---------|
| Mean | x̄ = Σx / n |
| Sample variance | s² = Σ(x − x̄)² / (n − 1) |
| Sample SD | s = √s² |
| CV | (s / x̄) × 100 % |
| Pearson skewness | 3(mean − median) / σ |
| IQR | Q3 − Q1 |
| Outlier rule | < Q1 − 1.5·IQR or > Q3 + 1.5·IQR |
| Pearson r | Σ(x−x̄)(y−ȳ) / √[Σ(x−x̄)²·Σ(y−ȳ)²] |
| Spearman r_s | 1 − 6Σd² / (n(n²−1)) |

## Probability rules

- P(A ∪ B) = P(A) + P(B) − P(A ∩ B)
- P(A ∩ B) = P(A) × P(B|A)
- Independent: P(A ∩ B) = P(A)P(B)
- **Bayes**: P(A|B) = P(B|A)·P(A) / Σ P(B|Aᵢ)·P(Aᵢ)

## Distributions

| Dist | Mean | Variance | Use |
|------|-----:|---------:|-----|
| Bernoulli | p | p(1−p) | Single trial |
| Binomial(n,p) | np | np(1−p) | n trials |
| Poisson(λ) | λ | λ | Rare events |
| Uniform(a,b) | (a+b)/2 | (b−a)²/12 | Equal likelihood |
| Normal(μ,σ²) | μ | σ² | Default continuous |
| Exponential(λ) | 1/λ | 1/λ² | Memoryless wait time |

Standard normal: Z = (X − μ)/σ. **68-95-99.7 rule**.

Approximations: B(n,p) → Poisson(np) when n ≥ 20, p ≤ 0.05. B(n,p) → N(np, np(1−p)) when np ≥ 5 and n(1−p) ≥ 5.

## Sampling distributions

- σ_x̄ = σ/√n  (Standard error of mean)
- σ_p = √(p(1−p)/n)  (SE of proportion)
- **CLT**: x̄ approximately normal for n ≥ 30 regardless of population shape.
- **FPC** (n/N > 5 %): multiply SE by √((N−n)/(N−1)).

## Confidence intervals

| Parameter | Formula |
|-----------|---------|
| μ (σ known) | x̄ ± Z_(α/2)·σ/√n |
| μ (σ unknown) | x̄ ± t_(α/2, n−1)·s/√n |
| π | p̂ ± Z_(α/2) · √(p̂(1−p̂)/n) |
| μ₁ − μ₂ (pooled) | (x̄₁−x̄₂) ± t·s_p√(1/n₁+1/n₂) |

Common Z: 90 % → 1.645; 95 % → 1.96; 99 % → 2.576.

Sample-size:
- Mean: n = (Z·σ/E)²
- Proportion: n = Z²·p̂(1−p̂)/E²  (use 0.5 if p̂ unknown to be conservative)

---

## Hypothesis tests (parametric)

| Test | Statistic | df |
|------|-----------|----|
| Z-mean (σ known) | (x̄ − μ₀)/(σ/√n) | — |
| t-mean (σ unknown) | (x̄ − μ₀)/(s/√n) | n−1 |
| Z-proportion | (p̂ − π₀)/√(π₀(1−π₀)/n) | — |
| 2-sample t (pooled) | (x̄₁ − x̄₂)/SE_pooled | n₁+n₂−2 |
| 2-sample t (Welch) | (x̄₁ − x̄₂)/√(s₁²/n₁+s₂²/n₂) | Welch–Satterthwaite |
| Paired t | d̄/(s_d/√n) | n−1 |
| F (variance ratio) | s₁²/s₂² | (n₁−1, n₂−1) |
| 1-way ANOVA F | MSB/MSW | (k−1, N−k) |
| χ² independence / GoF | Σ(O−E)²/E | (r−1)(c−1) / k−1−p |

Reject if |stat| > critical OR p < α.

**Type I (α)** = reject true H₀. **Type II (β)** = accept false H₀. **Power** = 1 − β.

## Non-parametric tests (Session 12)

| Parametric | Non-parametric counterpart | Use when |
|------------|----------------------------|---------|
| 2-sample t (independent) | Mann-Whitney U / Wilcoxon Rank-Sum | Ordinal / non-normal |
| Paired t | Wilcoxon Signed-Rank | Paired ordinal / non-normal |
| One-way ANOVA | Kruskal-Wallis H (df = k−1) | Compare ≥3 medians |
| Pearson r | Spearman r_s | Monotonic, non-linear |
| Chi-square (small E) | Fisher's exact | Any E_ij < 5 |

## Regression (Sessions 13-14)

- b₁ = Σ(x−x̄)(y−ȳ) / Σ(x−x̄)²
- b₀ = ȳ − b₁·x̄
- R² = SSR/SST = 1 − SSE/SST
- Adjusted R² = 1 − (1−R²)·(n−1)/(n−k−1)
- s_e (RMSE) = √(SSE/(n−k−1))
- t-test on β: t = b_i / SE(b_i), df = n−k−1
- F-test (overall): F = MSR/MSE, df = (k, n−k−1)

### LINE assumptions and diagnostics

| Assumption | Diagnostic | Threshold | Fix |
|-----------|-----------|----------|-----|
| **L**inearity | Residuals vs Fitted plot | No pattern | Add polynomial / transform |
| **I**ndependence | Durbin-Watson | ≈ 2 (1.5–2.5 ok) | Add lag, ARIMA |
| **N**ormality | Shapiro-Wilk, Q-Q plot | p > 0.05 | Box-Cox / log-Y |
| **E**qual variance | Residual funnel, Breusch-Pagan | p > 0.05 | Log Y / WLS / robust SE |
| Multicollinearity | VIF | < 5 (warn 5-10, drop ≥10) | Remove / combine vars |

## Linear Programming (Session 15)

- **Form**: Max/Min Z = c·x  s.t.  A·x ≤ b, x ≥ 0
- Optimum lies at a **corner** of the feasible region.
- **Shadow price** = Δobjective per +1 unit RHS of a binding constraint.
- **Reduced cost** = penalty for forcing a non-basic variable into the solution.
- Special cases: multiple optima (parallel obj line), infeasible (no overlap), unbounded (open feasible region), degeneracy.
- Excel **Solver** → choose **Simplex LP** for linear models.

---

## Critical values cheat sheet (memorise)

**Z (two-tailed)**

| α | 0.10 | 0.05 | 0.01 |
|---|--:|--:|--:|
| Z* | 1.645 | 1.96 | 2.576 |

**t (two-tailed, α = 0.05)**

| df | 10 | 20 | 30 | 60 | ∞ |
|---|--:|--:|--:|--:|--:|
| t* | 2.228 | 2.086 | 2.042 | 2.000 | 1.96 |

**χ² (α = 0.05)**

| df | 1 | 2 | 5 | 10 | 20 |
|---|--:|--:|--:|--:|--:|
| χ²* | 3.84 | 5.99 | 11.07 | 18.31 | 31.41 |

**F (α = 0.05, df₁ = 2)**

| df₂ | 5 | 10 | 20 | 30 |
|---|--:|--:|--:|--:|
| F* | 5.79 | 4.10 | 3.49 | 3.32 |

---

## Excel & Python quick-reference

| Task | Excel | Python |
|------|-------|--------|
| Mean / SD | `AVERAGE` / `STDEV.S` | `np.mean()` / `np.std(ddof=1)` |
| Bin / Poisson / Normal | `BINOM.DIST` / `POISSON.DIST` / `NORM.DIST` | `scipy.stats.binom/poisson/norm` |
| Z / t test | `Z.TEST` / `T.TEST` | `scipy.stats.ttest_1samp/ind/rel` |
| Chi-square | `CHISQ.TEST` | `scipy.stats.chi2_contingency` |
| ANOVA | Data Analysis ToolPak → ANOVA | `scipy.stats.f_oneway` |
| Mann-Whitney | n/a | `scipy.stats.mannwhitneyu` |
| Kruskal-Wallis | n/a | `scipy.stats.kruskal` |
| Wilcoxon Signed-Rank | n/a | `scipy.stats.wilcoxon` |
| Regression + diagnostics | Data Analysis → Regression | `statsmodels.api.OLS().fit()` → `.summary()` |
| LP | Solver add-in (Simplex LP) | `scipy.optimize.linprog` / `pulp` |

## Calculator quick keys (Casio FX-991EX)

- Mode → 6 (Statistics) → 1 (1-Var) → enter data → AC → OPTN
- 1: 1-Var summary (mean, σ, x̄)
- For regression: Mode → 6 → 2 (Y = a + bX) → reads slope, intercept, r

## Last-90-second mental checks

1. Is the question asking for CI, hypothesis test, or just descriptive? Read again.
2. Two-tailed or one-tailed? Look for "differs" (two) vs "greater/less than" (one).
3. σ known → Z; σ unknown → t.
4. Data normal & interval? → parametric. Ordinal / small n / non-normal? → non-parametric.
5. Round answers to 4 decimals for probabilities, 2 for ₹.
6. State conclusion in **business language**, not just "reject H₀".

---

## References & Sources

### Quick-reference resources
- NIST/SEMATECH e-Handbook of Statistical Methods: https://www.itl.nist.gov/div898/handbook/
- StatTrek formula sheet: https://stattrek.com/statistics/formulas
- Real Statistics Excel formulas reference: https://real-statistics.com/
- scipy.stats reference: https://docs.scipy.org/doc/scipy/reference/stats.html
- statsmodels regression diagnostics: https://www.statsmodels.org/stable/diagnostic.html

### Calculator and Excel
- Casio FX-991EX manual: https://support.casio.com/global/en/calc/manual/fx-991EX_570EX_en/
- Excel statistical functions reference: https://support.microsoft.com/en-us/office/statistical-functions-reference-624dac86-a375-4435-bc25-76d659719ffd
- Excel Solver tutorial (LP): https://www.solver.com/excel-solver-online-help

### Visual learning (last-minute revision)
- 3Blue1Brown — Probability: https://www.youtube.com/c/3blue1brown
- StatQuest with Josh Starmer — concept videos: https://www.youtube.com/@statquest
