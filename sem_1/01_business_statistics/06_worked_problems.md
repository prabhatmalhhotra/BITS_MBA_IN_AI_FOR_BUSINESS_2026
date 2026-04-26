# Business Statistics — Worked Numerical Problems

> **Aligned to `MBACC ZG501` (S2-25)** 16-session learning plan.
> Each problem is original (not copied from any textbook). Format: **Problem → Given → Solution steps → Final answer → Common mistakes**.
> Use these for EC-2 (mid-sem, sessions 1-8) and EC-3 (comprehensive, all 16). Solve before reading the solution.

---

## Session 3 — Numerical Descriptive Measures

### Problem 3.1 — Mean, median, SD, CV
A small e-commerce firm records the daily order count for 7 days: **42, 51, 38, 47, 55, 39, 60**.
Compute mean, median, sample standard deviation, coefficient of variation. Comment on dispersion.

**Solution**
1. Sort: 38, 39, 42, 47, 51, 55, 60. n = 7.
2. **Mean** x̄ = (42+51+38+47+55+39+60) / 7 = 332 / 7 = **47.43**
3. **Median** = middle value (4th in sorted) = **47**
4. **Sample variance** s² = Σ(xᵢ−x̄)² / (n−1)
   - Deviations²: (38−47.43)²=88.92, (39−47.43)²=71.06, (42−47.43)²=29.49, (47−47.43)²=0.18, (51−47.43)²=12.74, (55−47.43)²=57.31, (60−47.43)²=158.00
   - Sum = 417.70
   - s² = 417.70 / 6 = **69.62**, s = **√69.62 ≈ 8.34**
5. **CV** = (s / x̄) × 100 = (8.34 / 47.43) × 100 ≈ **17.6 %**

**Final answer**: Mean 47.43, Median 47, SD 8.34, CV 17.6 %. Mean ≈ median → roughly symmetric. CV < 25 % → moderate dispersion.

**Common mistakes**: dividing by n instead of (n−1) for sample SD; forgetting to sort before finding median.

---

### Problem 3.2 — Covariance and Pearson r
Five customers' annual spend (₹k) and loyalty-points earned: (12, 240), (18, 380), (24, 510), (30, 690), (36, 820).
Compute Cov(X,Y) and Pearson r. Interpret.

**Solution**
- x̄ = (12+18+24+30+36)/5 = 24; ȳ = (240+380+510+690+820)/5 = 528
- Σ(xᵢ−x̄)(yᵢ−ȳ): (−12)(−288)+(−6)(−148)+(0)(−18)+(6)(162)+(12)(292) = 3456+888+0+972+3504 = 8820
- Cov = 8820 / (5−1) = **2205**
- Σ(xᵢ−x̄)² = 144+36+0+36+144 = 360 → sₓ = √(360/4) = √90 = 9.49
- Σ(yᵢ−ȳ)² = 82944+21904+324+26244+85264 = 216680 → sᵧ = √(216680/4) = √54170 = 232.74
- **r** = Cov / (sₓ · sᵧ) = 2205 / (9.49 × 232.74) ≈ **0.998**

**Final answer**: Cov = 2205, r ≈ 0.998 → near-perfect positive linear association.

**Common mistakes**: using n instead of n−1 for sample covariance; r outside [−1, +1] indicates calculation error.

---

## Session 4 — Basic Probability + Bayes' Theorem

### Problem 4.1 — Conditional probability (joint table)
A firm classifies 1,000 leads by source (Organic / Paid) and outcome (Converted / Not):

| | Converted | Not | Total |
|---|---:|---:|---:|
| Organic | 90 | 410 | 500 |
| Paid | 60 | 440 | 500 |
| **Total** | **150** | **850** | **1000** |

Find: (a) P(Converted), (b) P(Converted \| Paid), (c) Are *Converted* and *Paid* independent?

**Solution**
- (a) P(C) = 150 / 1000 = **0.15**
- (b) P(C \| Paid) = 60 / 500 = **0.12**
- (c) Independent iff P(C \| Paid) = P(C). 0.12 ≠ 0.15 → **not independent** (Paid leads convert at a lower rate).

---

### Problem 4.2 — Bayes' Theorem (medical/quality testing)
A defect-detection sensor flags 95 % of true defective parts (sensitivity) but also flags 4 % of good parts (false positive). Defect rate in production = 2 %. If a part is flagged, what is the probability it is genuinely defective?

**Solution**
- Let D = defective, F = flagged. Given P(D)=0.02, P(F\|D)=0.95, P(F\|D′)=0.04.
- P(F) = P(F\|D)·P(D) + P(F\|D′)·P(D′) = 0.95(0.02) + 0.04(0.98) = 0.019 + 0.0392 = **0.0582**
- **P(D \| F) = P(F\|D)·P(D) / P(F) = 0.019 / 0.0582 ≈ 0.3265 ≈ 32.6 %**

**Final answer**: Only **~32.6 %** of flagged parts are truly defective. Despite 95 % sensitivity, low base rate (2 %) makes most flags false alarms.

**Common mistakes**: confusing P(F\|D) with P(D\|F) (base-rate fallacy); forgetting to compute P(F) via total-probability law.

---

## Session 5 — Discrete Probability Distributions

### Problem 5.1 — Binomial
Historical conversion rate on a checkout page = 18 %. In a random sample of n = 12 visitors:
(a) Probability exactly 3 convert.
(b) Probability at least 1 converts.
(c) Mean and SD of number of conversions.

**Solution**
- X ~ Binomial(n=12, p=0.18).
- (a) P(X=3) = C(12,3) · (0.18)³ · (0.82)⁹ = 220 · 0.005832 · 0.16802 ≈ **0.2155**
- (b) P(X≥1) = 1 − P(X=0) = 1 − (0.82)¹² = 1 − 0.0921 ≈ **0.9079**
- (c) μ = np = 12 × 0.18 = **2.16**; σ = √[np(1−p)] = √(12·0.18·0.82) = √1.7712 ≈ **1.331**

---

### Problem 5.2 — Poisson
A call centre receives an average of **6.4 calls per 5-minute window**. Assuming Poisson:
(a) P(exactly 8 calls in next 5 min). (b) P(zero calls). (c) Expected calls per hour.

**Solution**
- λ = 6.4 per 5-minute window.
- (a) P(X=8) = e⁻⁶·⁴ · (6.4)⁸ / 8! = 0.001662 · 2814749.77 / 40320 ≈ **0.1160**
- (b) P(X=0) = e⁻⁶·⁴ ≈ **0.00166**
- (c) Per hour = 12 × 5-min windows → λ_hour = 12 × 6.4 = **76.8 calls**

**Common mistakes**: Using Binomial when "rate per time/area" is given (use Poisson); forgetting to scale λ when changing time window.

---

## Session 6 — Normal Distribution

### Problem 6.1 — Z-score, area under normal curve
Daily transaction values are normally distributed: μ = ₹4,500, σ = ₹800.
(a) P(X > 5,500). (b) P(3,800 < X < 5,200). (c) Cut-off X for top 10 % transactions.

**Solution**
- (a) Z = (5500 − 4500)/800 = 1.25 → P(Z>1.25) = 1 − 0.8944 = **0.1056** (~10.6 %)
- (b) Z₁ = (3800−4500)/800 = −0.875; Z₂ = (5200−4500)/800 = 0.875
   P(−0.875 < Z < 0.875) = 0.8092 − 0.1908 = **0.6184**
- (c) Top 10 % → Z₀.₉₀ = 1.28. X = μ + Zσ = 4500 + 1.28(800) = **₹5,524**

---

## Session 7 — Sampling Distributions / CLT

### Problem 7.1 — Sampling distribution of mean
Population: μ = 75, σ = 12. Sample size n = 36.
(a) Mean and SD of sampling distribution of x̄.  (b) P(x̄ > 78).

**Solution**
- μ_x̄ = μ = **75**; σ_x̄ = σ/√n = 12/6 = **2**
- Z = (78−75)/2 = 1.5 → P(x̄>78) = 1 − 0.9332 = **0.0668**

---

### Problem 7.2 — Sampling distribution of proportion
True conversion rate p = 0.20. Sample n = 200.
(a) Mean and SD of p̂. (b) P(p̂ < 0.17).

**Solution**
- μ_p̂ = 0.20; σ_p̂ = √[p(1−p)/n] = √(0.20·0.80/200) = √0.0008 = **0.02828**
- Z = (0.17−0.20)/0.02828 = −1.061 → P(p̂<0.17) = P(Z<−1.061) ≈ **0.1444**

---

## Session 8 — Confidence Interval Estimation

### Problem 8.1 — CI for mean (σ unknown, t-distribution)
Sample of n = 16 widget weights: x̄ = 252 g, s = 8 g. Build a 95 % CI for μ.

**Solution**
- df = n−1 = 15. t₀.₀₂₅,₁₅ = **2.131**
- Margin = t · s/√n = 2.131 · 8/4 = **4.262**
- 95 % CI: 252 ± 4.262 → **(247.74, 256.26) g**

---

### Problem 8.2 — CI for proportion + sample size
A poll of n = 400 customers shows 96 favour a redesign.
(a) 95 % CI for true p. (b) What sample size for margin of error 2 % at 95 % CI (using p̂ from this poll)?

**Solution**
- p̂ = 96/400 = 0.24
- (a) Margin = 1.96 · √(0.24·0.76/400) = 1.96 · √0.000456 = 1.96 · 0.02135 = **0.0419**
   95 % CI = 0.24 ± 0.0419 = **(0.198, 0.282)** ≈ (19.8 %, 28.2 %)
- (b) n = (Z² · p̂(1−p̂)) / E² = (1.96² · 0.24 · 0.76) / 0.02² = (3.8416 · 0.1824) / 0.0004 = 0.7007 / 0.0004 ≈ **1,752**

**Common mistakes**: using Z when σ unknown and n small (use t); forgetting to round n UP for sample-size questions.

---

## Session 9 — Hypothesis Testing (one-sample)

### Problem 9.1 — One-sample t-test (mean, σ unknown)
Claim: average delivery time = 30 min. Sample n = 25, x̄ = 31.8, s = 4.5. Test at α = 0.05 (two-tailed).

**Solution (7-step framework)**
1. **H₀**: μ = 30. **H₁**: μ ≠ 30.
2. α = 0.05, two-tailed.
3. Test stat: t = (x̄ − μ₀) / (s/√n) since σ unknown, n small.
4. df = 24. Critical: ±t₀.₀₂₅,₂₄ = **±2.064**.
5. t_calc = (31.8 − 30) / (4.5/√25) = 1.8 / 0.9 = **2.00**.
6. \|2.00\| < 2.064 → **fail to reject H₀**.
7. Conclusion: Insufficient evidence at 5 % to claim avg delivery differs from 30 min. (p-value ≈ 0.057, just above α.)

---

### Problem 9.2 — One-sample Z-test (proportion)
Last year: 12 % churn. New retention programme; n = 500, churned = 48 (p̂ = 0.096). Has churn reduced? (α = 0.05, one-tailed.)

**Solution**
- H₀: p = 0.12. H₁: p < 0.12.
- Z = (p̂ − p₀) / √[p₀(1−p₀)/n] = (0.096 − 0.12) / √(0.12·0.88/500) = −0.024 / 0.01453 = **−1.652**.
- Critical: −Z₀.₀₅ = −1.645.
- −1.652 < −1.645 → **reject H₀** (just barely). Churn has likely reduced.

**Common mistakes**: using p̂ in denominator (always use p₀ for hypothesis-testing variance); wrong tail.

---

## Session 10 — Two-sample tests + ANOVA

### Problem 10.1 — Two-sample t (independent, pooled)
Group A (n₁=10, x̄₁=82, s₁=6) vs Group B (n₂=12, x̄₂=78, s₂=5). Test μ_A ≠ μ_B at α = 0.05, assume equal variances.

**Solution**
- Pooled s²_p = [(n₁−1)s₁² + (n₂−1)s₂²] / (n₁+n₂−2) = [9·36 + 11·25] / 20 = (324 + 275) / 20 = 29.95
- s_p = 5.473
- t = (82 − 78) / [5.473 · √(1/10 + 1/12)] = 4 / [5.473 · √0.1833] = 4 / [5.473 · 0.4282] = 4 / 2.343 = **1.707**
- df = 20. t₀.₀₂₅,₂₀ = ±2.086.
- \|1.707\| < 2.086 → **fail to reject H₀**. No significant difference at 5 %.

---

### Problem 10.2 — Paired t-test
Same 8 subjects pre/post training. Differences d = post − pre: 5, 3, 7, 2, 6, 4, 8, 5.
Test if training increased score. (α = 0.05, one-tailed.)

**Solution**
- d̄ = 40/8 = 5.0; s_d²: deviations² = 0+4+4+9+1+1+9+0 = 28; s_d² = 28/7 = 4; s_d = 2.
- t = d̄ / (s_d/√n) = 5 / (2/√8) = 5 / 0.707 = **7.07**.
- df = 7. t₀.₀₅,₇ = 1.895.
- 7.07 > 1.895 → **reject H₀**. Training significantly increased scores.

---

### Problem 10.3 — One-way ANOVA
Three branches' weekly sales (₹lakh): A: 12, 14, 13, 15 ; B: 18, 17, 19, 16 ; C: 11, 13, 10, 12. Test H₀: μ_A = μ_B = μ_C at α = 0.05.

**Solution**
- Means: x̄_A = 13.5, x̄_B = 17.5, x̄_C = 11.5. Grand mean x̄̄ = (13.5+17.5+11.5)/3 = 14.17 (or sum of all 12 / 12 = 170/12 = 14.17).
- **SSB** (between) = Σ nⱼ(x̄ⱼ − x̄̄)² = 4(13.5−14.17)² + 4(17.5−14.17)² + 4(11.5−14.17)² = 4(0.4489) + 4(11.0889) + 4(7.1289) = 1.7956 + 44.3556 + 28.5156 = **74.667**
- **SSW** (within): A: (12−13.5)²+(14−13.5)²+(13−13.5)²+(15−13.5)² = 2.25+0.25+0.25+2.25 = 5.0; B: 0.25+0.25+2.25+2.25 = 5.0; C: 0.25+2.25+2.25+0.25 = 5.0. SSW = 15.
- df_B = k−1 = 2; df_W = N−k = 9.
- MSB = 74.667/2 = 37.33; MSW = 15/9 = 1.667.
- F = MSB / MSW = 37.33 / 1.667 = **22.40**
- F_critical (2,9, α=0.05) = 4.26. 22.40 > 4.26 → **reject H₀**. At least one branch differs.

**Common mistakes**: dividing SSB by N−1 instead of k−1; forgetting post-hoc (Tukey/Bonferroni) when ANOVA is significant.

---

## Session 11 — Chi-square Test

### Problem 11.1 — Goodness-of-fit
Expected dice fair: each face 1/6. Observed in 120 rolls: 18, 22, 16, 24, 20, 20.
Test H₀: die is fair, α = 0.05.

**Solution**
- Expected per face = 120/6 = 20.
- χ² = Σ(O−E)²/E = (18−20)²/20 + (22−20)²/20 + (16−20)²/20 + (24−20)²/20 + 0 + 0
   = 4/20 + 4/20 + 16/20 + 16/20 + 0 + 0 = 40/20 = **2.0**
- df = k−1 = 5. χ²₀.₀₅,₅ = 11.07.
- 2.0 < 11.07 → **fail to reject H₀**. No evidence of bias.

---

### Problem 11.2 — Test of independence
500 customers cross-tabbed by region (N/S) and product preference (X/Y/Z):

| | X | Y | Z | Total |
|---|---:|---:|---:|---:|
| North | 80 | 60 | 110 | 250 |
| South | 70 | 90 | 90 | 250 |
| **Total** | **150** | **150** | **200** | **500** |

Test independence (α = 0.05).

**Solution**
- Expected E_ij = (row total × col total)/grand total
- E(N,X)=E(S,X)=250·150/500=75; E(N,Y)=E(S,Y)=75; E(N,Z)=E(S,Z)=100.
- χ² = Σ(O−E)²/E = (5²+15²+10²+5²+15²+10²)/(75 to 100…)
   = 25/75 + 225/75 + 100/100 + 25/75 + 225/75 + 100/100
   = 0.333 + 3.0 + 1.0 + 0.333 + 3.0 + 1.0 = **8.667**
- df = (r−1)(c−1) = (1)(2) = 2. χ²₀.₀₅,₂ = 5.991.
- 8.667 > 5.991 → **reject H₀**. Region and product preference are NOT independent.

**Common mistakes**: wrong df formula for independence vs goodness-of-fit; using row totals as E.

---

## Session 12 — Non-parametric Tests

### Problem 12.1 — Sign test
Paired data, n = 10. Differences (post − pre): +, +, −, +, +, +, 0, +, −, +. (1 zero, 7 plus, 2 minus). Test H₀: no median change, α = 0.05.

**Solution**
- Drop ties → n_eff = 9. n⁺ = 7, n⁻ = 2.
- Under H₀, n⁺ ~ Binomial(9, 0.5).
- p-value (two-tailed) = 2 · P(X ≥ 7) where X~Bin(9, 0.5)
   = 2 · [C(9,7)+C(9,8)+C(9,9)] / 2⁹ = 2 · (36+9+1)/512 = 2 · 46/512 = **0.180**
- p > 0.05 → **fail to reject H₀**. No significant median change.

---

### Problem 12.2 — Wilcoxon Rank-Sum / Mann-Whitney U
Group A: 12, 15, 18, 22. Group B: 10, 14, 16, 20. n₁ = n₂ = 4.
Test H₀: same distribution, α = 0.05 (two-tailed).

**Solution**
- Combined ranking ascending: 10(1), 12(2), 14(3), 15(4), 16(5), 18(6), 20(7), 22(8).
- Sum of A ranks: 2+4+6+8 = **20**. Sum of B ranks: 1+3+5+7 = 16. Check: 20+16 = 36 = n(n+1)/2 = 8·9/2 ✓
- W = 20.
- For n₁=n₂=4, α=0.05 two-tailed: critical W lower = 11, upper = 25.
- 11 < 20 < 25 → **fail to reject H₀**. No significant difference.

---

### Problem 12.3 — Spearman rank correlation
Two judges rank 5 candidates: J1: 1,2,3,4,5; J2: 2,1,4,3,5.

**Solution**
- d_i = rank diff: −1, +1, −1, +1, 0.  d² = 1, 1, 1, 1, 0. Σd² = 4.
- r_s = 1 − 6·Σd² / [n(n²−1)] = 1 − 24 / [5·24] = 1 − 0.20 = **0.80**

---

## Session 13-14 — Linear Regression

### Problem 13.1 — Simple linear regression
Promotional spend X (₹k) vs Sales Y (units): (10, 80), (15, 110), (20, 130), (25, 170), (30, 200), (35, 230). n=6.

**Solution**
- Σx = 135, Σy = 920, Σxy = 23,200 → no, let me recompute carefully:
   - x · y: 10·80=800, 15·110=1650, 20·130=2600, 25·170=4250, 30·200=6000, 35·230=8050; **Σxy = 23,350**
- Σx² = 100+225+400+625+900+1225 = **3475**
- x̄ = 135/6 = 22.5; ȳ = 920/6 = 153.33
- **b₁** = [Σxy − n·x̄·ȳ] / [Σx² − n·x̄²] = [23350 − 6·22.5·153.33] / [3475 − 6·506.25]
   = [23350 − 20700] / [3475 − 3037.5] = 2650 / 437.5 = **6.057**
- **b₀** = ȳ − b₁·x̄ = 153.33 − 6.057·22.5 = 153.33 − 136.29 = **17.04**
- Regression equation: **Ŷ = 17.04 + 6.057 X**
- Interpretation: each ₹1k extra spend → ~6.06 extra units sold.

---

### Problem 13.2 — R² and prediction
Using regression above, predict sales at X = 28. Compute R².

**Solution**
- Ŷ at X=28: 17.04 + 6.057·28 = 17.04 + 169.60 = **186.64 units**.
- SST = Σ(yᵢ−ȳ)²: dev²: (80−153.33)²=5377.36, (110−153.33)²=1877.51, (130−153.33)²=544.29, (170−153.33)²=277.89, (200−153.33)²=2178.13, (230−153.33)²=5878.27. SST ≈ **16,133.5**
- SSE = Σ(yᵢ−Ŷᵢ)²:
   - Ŷ values: 17.04+6.057·10=77.61; +6.057·15=107.89; +6.057·20=138.18; +6.057·25=168.46; +6.057·30=198.75; +6.057·35=229.04
   - Residuals: 80−77.61=2.39, 110−107.89=2.11, 130−138.18=−8.18, 170−168.46=1.54, 200−198.75=1.25, 230−229.04=0.96
   - Squared: 5.71+4.45+66.91+2.37+1.56+0.92 = **81.92**
- **R² = 1 − SSE/SST = 1 − 81.92 / 16133.5 ≈ 0.9949 ≈ 99.5 %**.

**Common mistakes**: confusing SSR with SSE; forgetting R² = SSR/SST not SSE/SST.

---

### Problem 14.1 — Residual diagnostics (conceptual + small calc)
Given the regression in 13.1, residuals are: 2.39, 2.11, −8.18, 1.54, 1.25, 0.96. Are these consistent with homoscedasticity? Apply quick visual judgement and Shapiro-Wilk-style intuition.

**Solution sketch**
- Residual 3 (X=20) is much larger in magnitude (−8.18) than others; possible outlier.
- No systematic increase in spread with X (residuals not fanning) → no obvious heteroscedasticity from this small sample.
- For Shapiro-Wilk W in Excel/Python, n=6 is too small; report sample mean of residuals ≈ 0 (as expected for OLS) and SD ≈ 3.7. Defer to formal AD/SW tests on bigger n.

---

## Session 15 — Linear Programming

### Problem 15.1 — LP graphical
A factory makes Product A (₹40 profit/unit) and Product B (₹30 profit/unit). Constraints:
- Machine: 2A + 1B ≤ 100 hours
- Labour: 1A + 1B ≤ 80 hours
- A, B ≥ 0

Maximise profit Z = 40A + 30B.

**Solution**
- Find corner points of feasible region.
   - (0,0): Z = 0
   - (50,0): from 2A=100; check labour: 50 ≤ 80 ✓ → Z = 2000
   - (0,80): from B=80; check machine: 80 ≤ 100 ✓ → Z = 2400
   - Intersection of 2A+B=100 and A+B=80: subtract → A = 20, B = 60. Z = 40·20 + 30·60 = 800 + 1800 = **2600**.
- **Optimal: A = 20, B = 60, Z = ₹2,600**.

---

### Problem 15.2 — LP with three constraints (interpret Excel Solver output)
A media planner allocates budget to TV (X) and Digital (Y) campaigns:
- Maximise reach: Z = 5X + 4Y (lakh impressions)
- Budget: X + Y ≤ 100 (₹lakh)
- TV cap: X ≤ 60
- Digital min: Y ≥ 20
- X, Y ≥ 0

**Solution**
- Corner points (feasible):
   - (0, 20): Z = 80
   - (0, 100): Z = 400
   - (60, 40): X=60 cap; budget left 40 → Y=40. Z = 5·60+4·40 = 300+160 = **460**
   - (60, 20): Z = 300+80 = 380
   - (80, 20): violates budget — not feasible
- **Optimal: X = 60, Y = 40, Z = 460 lakh impressions**.
- Slack: budget binding (used 100), TV cap binding (X=60), digital min slack = 20.

**Common mistakes**: ignoring boundary at Y ≥ 20; not checking *all* corner points.

---

## EC-2 / EC-3 quick exam map

| Topic | Likely problem type in EC-2 (closed-book) | Likely problem type in EC-3 (open-book) |
|-------|-------------------------------------------|-----------------------------------------|
| S3 Descriptive | Compute mean, median, SD, CV, r from raw data | Compare two datasets via CV; interpret skewness |
| S4 Probability | 2x2 joint table OR Bayes 2-state | Bayes 3-state; complex conditional |
| S5 Discrete | Binomial cumulative; Poisson exact | Binomial → Poisson approximation; Poisson process |
| S6 Normal | Z-table area; reverse Z (cut-off) | Mixture; Normal approximation to Binomial |
| S7 Sampling | μ_x̄, σ_x̄ + one P(x̄ > k) | CLT justification on non-normal |
| S8 CI | CI for mean (t) + sample size | CI for proportion + comparison |
| S9 Hypothesis | One-sample t OR Z for proportion | One-sample with non-trivial α / one-tailed |
| S10 Two-sample / ANOVA | Independent t OR paired t | Full ANOVA table + post-hoc |
| S11 Chi² | Goodness-of-fit OR independence | Both in one paper |
| S12 Non-parametric | Sign or Spearman | Wilcoxon / Mann-Whitney + interpretation |
| S13-14 Regression | Compute b₀, b₁; predict; R² | Residual diagnostics; normality test choice |
| S15 LP | Graphical 2-variable, 2-3 constraints | Solver output interpretation; sensitivity analysis |

> **Practice tactic**: time yourself. EC-2 is 2 hrs, ~50-60 marks. EC-3 is 2 hrs, ~80-100 marks. Average ≈ 2 min/mark. If a problem is taking >25 min, move on and come back.
