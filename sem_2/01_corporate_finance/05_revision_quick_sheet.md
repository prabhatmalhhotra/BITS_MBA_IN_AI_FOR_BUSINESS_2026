# Corporate Finance — One-Page Revision

## TVM
- FV = PV(1+r)ⁿ
- PV = FV/(1+r)ⁿ
- FVA = PMT × [((1+r)ⁿ − 1)/r]
- PVA = PMT × [(1 − (1+r)⁻ⁿ)/r]
- Perpetuity PV = PMT/r; Growing PV = PMT/(r−g)
- EAR = (1 + r/m)^m − 1

## Risk & return
- E(R) = ΣP·R; σ² = ΣP·(R−E(R))²
- Portfolio σ² = w₁²σ₁² + w₂²σ₂² + 2w₁w₂σ₁σ₂ρ
- CAPM: ke = Rf + β(Rm − Rf)
- β = Cov(Ri,Rm)/Var(Rm)
- Systematic = market, undiversifiable. Unsystematic = firm-specific, diversifiable.

## Cost of capital
- After-tax kd = kd × (1−t)
- ke (CAPM, DCF: D₁/P₀ + g, Bond yield + premium)
- WACC = (E/V)·ke + (D/V)·kd(1−t) + (P/V)·kp

## Capital budgeting
- NPV = Σ CFt/(1+r)^t − Investment ; accept if > 0
- IRR: r where NPV = 0; accept if > WACC
- PI = PV inflows / Investment; accept if > 1
- Payback = years till cum CF = investment
- For mutually exclusive: NPV > IRR

## Capital structure
- NI: more debt → lower WACC → linear value increase
- NOI/MM (no tax): structure irrelevant
- MM with tax: V_levered = V_unlevered + t·D
- Trade-off: tax shield vs distress
- Pecking order: internal → debt → equity
- DOL = Contribution / EBIT
- DFL = EBIT / (EBIT − Interest)
- DCL = DOL × DFL

## Dividend
- Walter: P = (D + (r/k)(E−D))/k. r > k → retain; r < k → pay out.
- Gordon: P = D₁/(k−g)
- MM irrelevance under perfect markets
- Bonus: more shares, no cash, price falls proportionally
- Buyback: tax-efficient alt to dividend

## Working capital
- Operating cycle = Inv days + Recv days
- CCC = OC − Pay days
- EOQ = √(2DS/H)
- Reduce CCC: lower inv, faster collection, longer payables

## Valuation
- Bond price = Σ Coupon/(1+y)^t + Face/(1+y)^n
- DDM: P = D₁/(k−g)
- DCF (FCFF): EV = Σ FCFFt/(1+WACC)^t + TV/(1+WACC)^n
- TV = FCFF_(n+1)/(WACC − g)
- FCFF = EBIT(1−t) + Dep − Capex − ΔWC
- Equity value = EV − Debt

## M&A
- Synergy = combined value > sum of parts
- Premium = offer − pre-deal price
- Most M&A fail due to integration / culture, not bad valuation alone

## Forex
- Direct ₹/USD vs Indirect USD/₹
- IRP: Forward = Spot × (1+r_home)/(1+r_foreign)
- PPP: Δexchange rate ≈ Δinflation differential

## Behavioural
Anchoring · Loss aversion · Overconfidence · Herding · Confirmation bias · Mental accounting.

## Excel functions
- =PV(rate, nper, pmt, fv)
- =FV(rate, nper, pmt, pv)
- =PMT(rate, nper, pv)
- =RATE(nper, pmt, pv, fv)
- =NPV(rate, cf1, cf2, …) + initial
- =IRR(values)
- =MIRR(values, finance_rate, reinvest_rate)
- =XNPV / =XIRR for irregular cash flows

## Sanity checks
1. PV factor never > 1 for r > 0.
2. NPV at IRR = 0 by definition.
3. WACC < cost of equity always (since debt is cheaper after-tax).
4. CCC negative → industry-leading (Amazon, Apple).
5. β = 0 → risk-free; β = 1 → market.
