# Corporate Finance — Long Questions

> 10 long-form numericals + theory. Designed for Mid/Comp papers.

---

### Q1. (15 m) A project requires investment of ₹12 cr. Cash flows for 5 years: ₹4 cr, ₹4 cr, ₹3 cr, ₹3 cr, ₹2 cr. Cost of capital = 12%. Compute (a) Payback, (b) Discounted Payback, (c) NPV, (d) IRR (approximate), (e) PI. Recommend.

PV factor at 12%: yr1=0.8929, yr2=0.7972, yr3=0.7118, yr4=0.6355, yr5=0.5674.

| Year | CF (₹ cr) | Cum CF | PV CF | Cum PV CF |
|-----:|----------:|------:|-----:|---------:|
| 1 | 4 | 4 | 3.572 | 3.572 |
| 2 | 4 | 8 | 3.189 | 6.761 |
| 3 | 3 | 11 | 2.135 | 8.896 |
| 4 | 3 | 14 | 1.907 | 10.803 |
| 5 | 2 | 16 | 1.135 | 11.938 |

(a) **Payback**: cumulative CF reaches 12 between yr 3 (11) and yr 4 (14). Fraction = (12−11)/3 = 0.33. Payback = **3.33 years**.

(b) **Discounted payback**: cumulative PV reaches 12 after yr 5? Cum PV at end of yr 5 = 11.94 < 12. Project does not pay back within life on a discounted basis (off by ~₹6 lakh).

(c) **NPV** = 11.94 − 12 = **−₹0.06 cr** (slightly negative).

(d) **IRR**: NPV = 0 at IRR. Try 11%: PVF = 0.901, 0.812, 0.731, 0.659, 0.593 → PV = 3.604+3.248+2.193+1.977+1.186 = 12.21. NPV at 11% = 0.21. Interpolate: IRR ≈ 11 + 0.21/(0.21+0.06) × 1% ≈ **11.78%**.

(e) **PI** = PV inflows / Investment = 11.94 / 12 = **0.995**.

**Recommendation**: NPV slightly negative, IRR (11.78%) below cost of capital (12%), PI < 1. **Reject** on a strict NPV basis. Could revisit if cash-flow estimates improve or cost of capital is overstated.

---

### Q2. (12 m) Compute WACC for a firm with: market value of equity ₹400 cr, market value of debt ₹200 cr, beta 1.2, Rf 7%, market premium 6%, pre-tax cost of debt 9%, tax rate 30%.

ke (CAPM) = 7 + 1.2 × 6 = **14.2%**.
After-tax kd = 9 × (1 − 0.3) = **6.3%**.
Total V = 400 + 200 = 600.
Weights: E/V = 0.667, D/V = 0.333.
WACC = 0.667 × 14.2 + 0.333 × 6.3 = 9.47 + 2.10 = **11.57%**.

This is the firm's discount rate for projects of average risk.

---

### Q3. (15 m) Discuss capital structure theories: NI, NOI, MM (with and without tax), Trade-off, Pecking order. Which best describes Indian corporate behaviour?

**NI (Durand)**: Higher debt → lower WACC, linear. Unrealistic at high leverage.

**NOI (Durand)**: Equity holders compensate higher leverage with higher ke; WACC unchanged → capital structure irrelevant.

**MM without tax**: Same as NOI conclusion with rigorous arbitrage proof. Proposition I: V = V_unlevered. Proposition II: ke = k₀ + (k₀ − kd)(D/E).

**MM with tax**: V_levered = V_unlevered + t·D (interest tax shield). Optimal = 100% debt (theoretical).

**Trade-off theory**: Add financial-distress costs (bankruptcy, customer flight, supplier credit tightening). Optimal at marginal trade-off.

**Pecking Order (Myers)**: Information asymmetry — internal funds first, then debt, then equity (signalling). Most aligned with observed behaviour.

**Indian context**: Most listed firms follow pecking order — high reliance on retained earnings + debt; equity issuance only when growth opportunities outpace internal funding (or as IPO/QIP windows open). Family-owned firms underweight equity to avoid dilution.

---

### Q4. (12 m) An Indian firm has EBIT ₹50 cr, interest ₹15 cr, tax rate 30%. Sales ₹400 cr, Variable cost ₹250 cr, Fixed cost (excl. dep) ₹70 cr, Depreciation ₹30 cr. Compute DOL, DFL, DCL. Comment.

Contribution = Sales − VC = 400 − 250 = ₹150 cr.
EBIT = Contribution − FC − Dep = 150 − 70 − 30 = ₹50 cr (matches).

**DOL** = Contribution / EBIT = 150 / 50 = **3.0**. A 1% change in sales changes EBIT by 3%.

**DFL** = EBIT / (EBIT − Interest) = 50 / 35 = **1.43**. A 1% change in EBIT changes EPS by 1.43%.

**DCL** = DOL × DFL = 3.0 × 1.43 = **4.29**. A 1% change in sales changes EPS by 4.29%.

**Comment**: High DOL signals heavy fixed costs — earnings sensitive to sales; risky in downturns. Adding leverage further amplifies risk (DCL = 4.29). Management should be cautious about taking on more debt unless confident in revenue stability.

---

### Q5. (15 m) Estimate the value of an Indian IT services firm using DCF (FCFF method) given: 3-year forecast cash flows ₹100, 120, 140 cr; thereafter perpetuity growth 5%; WACC 11%; debt ₹300 cr.

Step 1 — PV of explicit forecast CF (3 years at 11%):
PV = 100/1.11 + 120/1.11² + 140/1.11³
   = 90.09 + 97.39 + 102.36 = **₹289.84 cr**.

Step 2 — Terminal value at end of year 3:
FCFF₄ = 140 × 1.05 = ₹147 cr.
TV₃ = 147 / (0.11 − 0.05) = ₹2,450 cr.
PV(TV) = 2,450 / 1.11³ = 2,450 / 1.3676 = **₹1,791.40 cr**.

Step 3 — Enterprise value = 289.84 + 1,791.40 = **₹2,081.24 cr**.

Step 4 — Equity value = EV − Debt = 2,081.24 − 300 = **₹1,781.24 cr**.

Step 5 — Sensitivity check: small change in g (say +1%) lifts TV substantially — always run sensitivity on g and WACC.

---

### Q6. (10 m) A firm pays ₹15 dividend with growth 8% and required return 12%. Find the share price (Gordon model). What if growth rises to 10%? Discuss sensitivity.

P = D₁ / (k − g) = 15 / (0.12 − 0.08) = **₹375**.

If g = 10%: P = 15 / (0.12 − 0.10) = **₹750** — doubles!

**Sensitivity**: Gordon model is highly sensitive to small changes in g, especially when (k − g) is small. Hence DCF practitioners always run scenario analysis on growth and discount rate, and use multi-stage models for high-growth firms.

---

### Q7. (12 m) Discuss working capital management. Compute the cash conversion cycle for: Inventory days 60, Receivables days 45, Payables days 30. Recommend three strategies to reduce CCC.

**CCC** = 60 + 45 − 30 = **75 days**.

Operating cycle = 60 + 45 = 105 days. Firm needs 75 days of working capital funded by other sources.

**Strategies to reduce CCC**

1. **Reduce inventory days** (target 45 from 60):
   - Demand forecasting (ML/AI), JIT with reliable suppliers, ABC analysis to right-size stock, vendor-managed inventory for fast movers.

2. **Reduce receivables days** (target 30 from 45):
   - Tighter credit policy, dynamic discounting (Pay early get 2% off), automated reminders, factoring/invoice discounting for the long tail.

3. **Stretch payables days** (target 45 from 30):
   - Negotiate longer terms with suppliers (using payment volume as leverage), use supply-chain finance to extend without straining suppliers.

Combined effect → CCC reduced from 75 to 30 days (45 + 30 − 45). Working capital frees up ~60% of current investment, lifting ROCE.

---

### Q8. (10 m) An Indian exporter expects USD 1 mn receivable in 3 months. Spot rate ₹83/USD. 3-month forward ₹83.50. 3-month USD interest rate 5%, INR 7%. (a) Should the firm hedge using forward? (b) What is the cost / benefit of hedging?

(a) **Hedging via forward** locks in ₹83.50/USD = ₹8.35 cr revenue. Without hedging, the firm bears forex risk: if rupee strengthens to ₹81, revenue = ₹8.10 cr (loss ₹25 lakh); if rupee weakens to ₹85, revenue = ₹8.50 cr (gain ₹15 lakh).

Decision: hedge if firm is risk-averse and operating margins are thin. Given the forward premium is similar to the IRP-implied rate, no clear arbitrage. Hedging removes uncertainty.

(b) **Implied IRP**: Forward = Spot × (1 + r_INR × 3/12) / (1 + r_USD × 3/12) = 83 × (1.0175)/(1.0125) = 83.41. Actual forward = 83.50, very close — IRP holds approximately. The "cost" of hedging is the difference between forward and expected future spot, which is unknown ex ante.

**Practical recommendation**: hedge 50–80% of the receivable using a mix of forward + USD/INR options (collar strategy to participate in upside while floor-protecting downside).

---

### Q9. (15 m) Discuss Behavioural Finance. Identify five biases that affect corporate financial decisions. Recommend organisational practices to debiase decision-making.

**Behavioural finance** integrates psychology into finance, recognising that decision-makers are not perfectly rational.

**Five biases (5 m)**:

1. **Anchoring** — initial values disproportionately influence subsequent estimates (e.g., past acquisition price anchors current valuation).
2. **Loss aversion** — losses feel ~2× more painful than equivalent gains feel good. Causes risk aversion in some contexts and risk-seeking in losses (sunk-cost fallacy).
3. **Overconfidence** — managers overestimate their ability to forecast cash flows / synergies. Drives over-investment, M&A premium-paying.
4. **Herding** — copying peers (all firms suddenly diversify into renewables when one does).
5. **Confirmation bias** — seeking info that confirms existing belief. Capital-budgeting committees see what they want to see in proposals they already like.

**Debiasing practices (10 m)**:

1. **Pre-mortem analysis**: imagine the project failed; list 10 reasons why. Surfaces hidden risks.
2. **Independent reviews**: involve outside-the-team experts for capital decisions > ₹X cr.
3. **Reference-class forecasting** (Kahneman): use historical outliers from similar past projects, not internal optimistic forecasts.
4. **Stage-gates with kill criteria**: explicit milestones; if not met, project paused regardless of sunk cost.
5. **Devil's advocate**: appoint someone to argue the negative case at every major decision review.
6. **Diverse decision committees**: variation in background reduces groupthink.
7. **Anonymise estimates**: collect cash-flow estimates anonymously to avoid groupshift.
8. **Post-decision audits**: track outcome vs forecast → feedback for future calibration.
9. **Dual-track scenario analysis**: best/base/worst as default for any large decision.

These practices won't eliminate bias but materially reduce its cost.

---

### Q10. (12 m) Mini-case: An Indian company is acquiring a smaller competitor for ₹500 cr (60% cash, 40% stock). Estimated synergies: cost ₹50 cr/yr, revenue ₹30 cr/yr, integration cost ₹40 cr (one-time). WACC 11%. Tax 30%. Estimate NPV of the deal and discuss non-financial considerations.

**Annual after-tax synergy CF**: (50 + 30 − 0) × (1 − 0.30) = ₹56 cr/yr. Less integration cost ₹40 cr in year 1 (or year 0).

Assume synergies achieved fully from year 2 (typical 12-month integration), perpetual horizon, no growth.

**NPV of synergies**:
- Year 1: 56 − 40 = 16, PV = 16/1.11 = 14.41
- Year 2 onward perpetuity: 56 / 0.11 = 509.09, PV at year 1 = 509.09/1.11 = 458.64

Total PV of synergies = 14.41 + 458.64 = **₹473.05 cr**.

**Acquisition price** = ₹500 cr.

**Net value created** = 473 − 500 = **−₹27 cr**. Marginal — synergies barely cover the price; weakened by integration costs.

**Recommendation considerations**:
- Negotiate down by ₹30+ cr.
- Stress-test synergy estimates — typical realised synergies are 60-70% of plan.
- Consider escrow / earnouts to align seller incentives.
- **Non-financial**: cultural fit (often the single biggest value destroyer in M&A), customer/supplier reactions, regulatory clearance (CCI), retention of key talent, integration team & timeline, communication plan.

**Deal go/no-go**: marginal NPV with high uncertainty → push back on price OR walk away.
