# Corporate Finance — Chapter-wise Notes

> Anchored to Prasanna Chandra (T1). Indian context throughout.

---

## Chapter 1 — Introduction to Corporate Finance

### 1.1 Goal of the firm
**Maximise shareholder wealth** (i.e., long-term market value per share), not short-term profit. Wealth maximisation accounts for risk, time value of money, and stakeholders.

### 1.2 Agency problem
Conflict between managers (agents) and shareholders (principals). Solutions: incentive alignment (ESOPs), monitoring (board, auditors), market discipline (takeovers).

### 1.3 Time value of money

| Concept | Formula |
|---------|---------|
| Future Value (single sum) | FV = PV × (1 + r)ⁿ |
| Present Value (single sum) | PV = FV / (1 + r)ⁿ |
| FV of annuity | FVA = PMT × [((1+r)ⁿ − 1)/r] |
| PV of annuity | PVA = PMT × [(1 − (1+r)⁻ⁿ)/r] |
| PV of perpetuity | PV = PMT / r |
| PV of growing perpetuity | PV = PMT / (r − g) |

Effective Annual Rate: EAR = (1 + r/m)^m − 1, where m = compounding periods per year.

### 60-second recap
Goal = maximise long-term shareholder value. Rupees today ≠ rupees tomorrow — discount everything. Annuities and perpetuities are common shortcuts.

---

## Chapter 2 — Risk and Return

### 2.1 Expected return and risk
E(R) = Σ Pᵢ × Rᵢ. Variance σ² = Σ Pᵢ × (Rᵢ − E(R))². σ = √σ².

### 2.2 Portfolio
Two-asset portfolio:
- E(Rp) = w₁E(R₁) + w₂E(R₂).
- σp² = w₁²σ₁² + w₂²σ₂² + 2w₁w₂σ₁σ₂ρ₁₂.

Diversification benefit grows when ρ < 1.

### 2.3 CAPM
E(R) = Rf + β × (Rm − Rf).
- Rf = risk-free rate (10-yr GoI bond, ~7% in India, 2026)
- β = sensitivity of asset returns to market returns
- Rm − Rf = equity risk premium (typically 5–7% in India)

### 2.4 Beta
β = Cov(Ri, Rm) / Var(Rm). β = 1 → moves with market; β > 1 → more volatile; β < 1 → less.

### 2.5 Systematic vs unsystematic risk
- **Systematic** (market) risk — un-diversifiable; rewarded.
- **Unsystematic** (firm-specific) — diversifiable; not rewarded by market.

### 60-second recap
Higher return demands higher risk. CAPM prices systematic risk. Diversify within sector and across sectors, geographies, asset classes to kill unsystematic risk.

---

## Chapter 3 — Valuation

### 3.1 Bond valuation
P = Σ (Coupon)/(1+y)^t + Face value / (1+y)^n.
- YTM = the discount rate that equates PV of cash flows to current price.
- Premium bond: coupon > YTM. Discount bond: coupon < YTM.

### 3.2 Equity valuation

**Dividend Discount Model (Gordon)**: P₀ = D₁ / (k − g), valid only for k > g.

**Two-stage DDM**: high-growth phase + stable-growth perpetuity.

**Free Cash Flow to Firm (FCFF)**:
FCFF = EBIT(1−t) + Depreciation − Capex − ΔWC.
Enterprise Value = Σ FCFFt/(1+WACC)^t + Terminal Value/(1+WACC)^n.
Terminal value (Gordon) = FCFF_(n+1)/(WACC − g).

**Free Cash Flow to Equity (FCFE)** = FCFF − Interest(1−t) + Net borrowings.

### 3.3 Relative valuation
- **P/E**: Price ÷ EPS. Compare to peers, growth-adjusted (PEG).
- **EV/EBITDA**: Enterprise value / EBITDA. Capital-structure neutral.
- **P/B**: For asset-heavy industries.

### 60-second recap
Valuation = future cash flows discounted at appropriate rate. DDM for stable dividend payers; DCF (FCFF/FCFE) for everything else; relative valuation as sanity-check.

---

## Chapter 4 — Capital Budgeting

### 4.1 Decision rules

| Method | Formula | Rule |
|--------|---------|------|
| Payback | Years till cumulative CF = investment | Accept if < target |
| Discounted Payback | As above with discounted CF | Same; fixes time-value gap |
| ARR | Avg accounting profit / Avg investment | Accept if > target |
| NPV | Σ CFt/(1+r)^t − Initial | Accept if > 0 |
| IRR | r where NPV = 0 | Accept if > cost of capital |
| MIRR | Adjusts IRR for reinvestment rate | Eliminates multi-IRR problem |
| PI | PV inflows / Investment | Accept if > 1 |

NPV theoretically best; for mutually exclusive projects, NPV > IRR.

### 4.2 Cash flow estimation
- Use **incremental** cash flows (with-vs-without project).
- Use **after-tax** cash flows.
- Include: opportunity costs, working-capital changes, terminal value, tax savings on depreciation.
- Ignore: sunk costs, allocated overhead (unless incremental), financing costs (handled in r).

### 4.3 Risk in capital budgeting
- **Sensitivity analysis**: change one variable, observe NPV change.
- **Scenario analysis**: best/base/worst combinations.
- **Monte Carlo**: probabilistic via simulation.
- **Decision trees**: sequential decisions.
- **Real options**: flexibility to expand, abandon, defer (Black-Scholes adapted).

### 60-second recap
Capital budgeting = NPV-led, with IRR as cross-check. Estimate after-tax incremental cash flows. Quantify uncertainty before betting big.

---

## Chapter 5 — Cost of Capital

### 5.1 Components
- **Cost of debt** (after tax) = kd × (1 − t). Use YTM of comparable bonds.
- **Cost of preference** = Preferred dividend / Net price.
- **Cost of equity**:
  - CAPM: ke = Rf + β(Rm − Rf)
  - DCF: ke = D₁/P₀ + g
  - Bond yield + risk premium: ke = YTM of debt + 3–5% premium

### 5.2 WACC
WACC = (E/V) × ke + (D/V) × kd × (1 − t) + (P/V) × kp.
Use **market values** (not book), and **target capital structure** if available.

### 5.3 Marginal cost of capital
WACC at the margin (next ₹ raised). Steps up as cheaper sources exhaust.

### 60-second recap
WACC = blended cost of all capital, weighted by market value, after tax. It's the discount rate for any project of average risk.

---

## Chapter 6 — Capital Structure

### 6.1 Key concepts
- **Capital structure** = mix of debt, equity, preference.
- **Optimal structure** = mix that minimises WACC (and maximises value).
- **Financial leverage**: debt magnifies EPS at the cost of higher risk.

### 6.2 Theories

**Net Income (NI) approach (Durand)**: Debt is cheaper; more debt → lower WACC → higher value. Linear, no equilibrium.

**Net Operating Income (NOI) approach**: Capital structure irrelevant; equity holders compensate via higher ke. WACC unchanged.

**Modigliani-Miller (MM)**:
- Without tax: Value of firm independent of capital structure (Proposition I). Cost of equity rises linearly with leverage (Proposition II).
- With tax: Value increases with debt due to tax shield. Optimal = 100% debt (theoretical).

**Trade-off theory**: Tax shield benefit of debt vs financial-distress costs (bankruptcy, lost flexibility). Optimum at the marginal trade-off.

**Pecking Order theory** (Myers): Firms prefer internal funds → debt → equity (last resort), to avoid signalling negative information.

### 6.3 Operating, financial, combined leverage
- DOL = % change in EBIT / % change in Sales = Contribution / EBIT.
- DFL = % change in EPS / % change in EBIT = EBIT / (EBIT − Interest).
- DCL = DOL × DFL.

### 60-second recap
Theories tell us debt has tax benefits but distress costs. Most Indian firms follow pecking order in practice. DCL measures total business+financial risk.

---

## Chapter 7 — Dividend Policy

### 7.1 Theories
- **Walter's model**: Optimal D depends on r vs k. If r > k, retain (growth firm); if r < k, pay out (declining firm); r = k → indifferent.
- **Gordon's model**: Investors prefer current dividends ("bird in hand") because of risk aversion.
- **MM irrelevance**: In perfect markets, dividend policy doesn't affect firm value.
- **Signalling theory**: Dividends signal management's confidence in future earnings.
- **Clientele effect**: Different investors prefer different payout policies.

### 7.2 Practical determinants
Profitability, cash flow stability, growth opportunities, leverage, tax considerations, shareholder preference, legal restrictions.

### 7.3 Forms
- **Cash dividend**: regular, special, interim.
- **Stock dividend (bonus)**: more shares, no cash; reduces price proportionally.
- **Stock split**: similar; more shares, lower face value.
- **Buyback**: repurchase shares; alternative to dividend; signals undervaluation; tax-advantaged for shareholders in some regimes.

### 60-second recap
Theories disagree but practice shows: dividends signal stability, buybacks signal undervaluation, retention signals growth investments. Match policy to firm life-cycle.

---

## Chapter 8 — Working Capital Management

### 8.1 Operating and cash conversion cycle
- **Operating cycle** = Inventory days + Receivables days.
- **Cash conversion cycle (CCC)** = Operating cycle − Payables days.

Lower CCC → less working capital tied up → higher ROCE.

### 8.2 Inventory management
- ABC analysis (top 20% items = 80% value).
- EOQ = √(2DS/H), where D = annual demand, S = order cost, H = holding cost.
- JIT (Just-in-Time): minimise stock; demands reliable suppliers.
- Safety stock = z × σ_demand × √lead-time.

### 8.3 Receivables management
Credit policy: terms, standards, collection effort. Tools: aging schedule, factoring.

### 8.4 Cash management
- Baumol model (deterministic): C = √(2bT/i).
- Miller-Orr (stochastic): upper / lower limits + return point.

### 8.5 Working capital financing
- **Conservative**: more long-term financing → lower risk, lower return.
- **Aggressive**: more short-term → higher risk, higher return.
- **Matching/Hedging**: long-term assets with long-term capital, short-term assets with short-term.

### 60-second recap
Working capital is the operational lifeblood. Shorten CCC; right-size inventory and receivables. Match financing maturity to asset maturity.

---

## Chapter 9 — Mergers, Acquisitions & Restructuring

### 9.1 Types
- Horizontal (same industry), Vertical (supply-chain), Conglomerate (unrelated).

### 9.2 Motives
- Synergy (cost, revenue), market power, tax shields, diversification, growth, defence.

### 9.3 Valuation in M&A
- DCF of target standalone + value of synergies.
- Premium = offer price − pre-deal price.
- EPS accretion/dilution analysis.

### 9.4 Post-merger integration
Often the source of M&A failure. Cultural integration > financial integration.

### 60-second recap
M&A creates value only when synergies exceed premium paid + integration costs. Most fail to deliver expected synergies. Integration is the real work.

---

## Chapter 10 — International Finance (overview)

### 10.1 Exchange rates
- Spot vs Forward. Direct (₹/USD) vs Indirect (USD/₹).
- Appreciation/Depreciation; revaluation/devaluation (managed regimes).

### 10.2 Theories
- Purchasing Power Parity (PPP): exchange rate adjusts to inflation differentials.
- Interest Rate Parity (IRP): forward premium ≈ interest-rate differential.

### 10.3 Hedging
- Forwards, futures, options, swaps.
- Natural hedge (revenue and cost in same currency).

### 60-second recap
Forex moves with inflation (PPP) and interest-rate (IRP) differentials. Hedge transaction exposure systematically; don't speculate.

---

## Chapter 11 — Behavioural Finance

### 11.1 Common biases
- **Anchoring**: over-reliance on first piece of info (e.g., target price set by IPO).
- **Loss aversion**: losses hurt ~2× more than equivalent gains feel good.
- **Overconfidence**: overestimating one's forecasts.
- **Herding**: following the crowd.
- **Confirmation bias**: seeking info that confirms existing belief.
- **Mental accounting**: treating same money differently based on source.

### 11.2 Implications for corporate decisions
- Capital budgeting: managers anchor on initial estimates; require independent reviews.
- M&A: hubris drives over-payment.
- Dividend policy: clients expect persistence; cuts punished disproportionately.

### 60-second recap
We're not as rational as classical finance assumes. Build processes, debiasing reviews, devil's advocates into financial decisions.

---

## Chapter 12 — Sustainability & ESG Finance (overview)

### 12.1 Green and sustainability-linked finance
- **Green bonds**: proceeds for environmentally beneficial projects.
- **Sustainability-linked loans**: interest rate adjusts based on ESG KPIs.

### 12.2 Climate risk in capital decisions
Physical risk (assets at risk from climate change) + transition risk (regulatory, technology shifts). Companies increasingly disclose via TCFD.

### 12.3 ESG ratings
MSCI, Sustainalytics. Influence cost of capital and investor base.

### 60-second recap
Climate and ESG are now financial considerations, not philanthropy. Discount rates and access to capital depend on credible ESG performance.
