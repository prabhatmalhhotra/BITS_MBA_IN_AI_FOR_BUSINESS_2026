# Managerial Accounting — Session-wise Notes (handout-aligned)

> Built from the official `MBACC ZG502` handout (S2-25, v1.0).
> Primary text **T1** = SN Maheswari & SK Maheswari, *Financial and Management Accounting*, **Sultan Chand & Sons 6e (2022)**.
> 16 contact sessions (some grouped per handout). Mid-Sem (closed book) covers sessions 1-8; Comprehensive (open book) covers 1-16.

## Quick session map

| # | Session | Source | Mid-Sem? |
|--:|---------|--------|:--------:|
| 1 | [Introduction to Accounting](#session-1--introduction-to-accounting) | T1 Ch. 1 | ✅ |
| 2 | [GAAP & Accounting Principles](#session-2--gaap--accounting-principles) | T1 Ch. 2 | ✅ |
| 3-4 | [Journal, Ledger, Trial Balance, Financial Statements](#session-3-4--journal-ledger-trial-balance-financial-statements) | T1 Ch. 3-7 | ✅ |
| 5 | [IFRS / IAS & Quality of Financial Reporting](#session-5--ifrs--ias--quality-of-financial-reporting) | Selected IFRS/IAS | ✅ |
| 6-7 | [Understanding & Analysing Financial Statements](#session-6-7--understanding--analysing-financial-statements) | T1 Ch. 12-15 | ✅ |
| 8-10 | [Ratio Analysis](#session-8-10--ratio-analysis) | T1 Ch. 16-17 | partial (8 only) |
| 11-13 | [Empirical / Case Study FS Analysis](#session-11-13--empirical--case-study-fs-analysis) | T1 Ch. 18 | — |
| 14-15 | [Cost Accounting and CVP](#session-14-15--cost-accounting-and-cvp) | T1 Ch. 22-23 | — |
| 16 | [Budgeting & Variance Analysis](#session-16--budgeting--variance-analysis) | T1 Ch. 25 | — |

> **Self-reading (pre-class):** Types of business structures — Sole Proprietorship, Partnership, LLP, OPC, Private and Public Companies. Maheswari Ch. 1 also.

---

## Session 1 — Introduction to Accounting

**Why accounting matters managerially.** Beyond compliance, accounting is a **value-creation lens**: it links the business strategy to outcomes (cash, margin, ROCE) that top management uses to allocate capital.

**Definition** — Accounting is "the art of recording, classifying and summarising in a significant manner and in terms of money, transactions and events which are, in part at least, of a financial character, and interpreting the results thereof" (AICPA).

**Branches**
- **Financial Accounting** — historical record + statutory reporting (P&L, B/S, CF) for external stakeholders (shareholders, lenders, tax authorities).
- **Management (Cost) Accounting** — decision-support for internal users; flexible, forward-looking; not bound by statute.
- **Tax Accounting** — Income-tax/GST compliance.
- **Sustainability Accounting** — ESG/IFRS S1, S2.

**Linkage: Business Strategy ↔ Financial Statements**
- Differentiation strategy → high gross margin, high R&D in P&L.
- Cost-leadership → asset-turnover focus, lean cost structure.
- Vertical integration → high fixed assets, longer cash conversion cycle.

**Financial Accounting Process (Cycle)**
1. Identify transaction with monetary impact.
2. Record in **Journal** (book of original entry).
3. Post to **Ledger** accounts.
4. Prepare **Trial Balance** (TB).
5. Adjustments (accruals, prepayments, depreciation, bad debts).
6. Prepare **Financial Statements** (P&L, B/S, Cash Flow).

**FMA → Financial Analytics → Business Analytics**
- Modern firms layer ML/AI on top of FA data: variance prediction, anomaly detection, forecasting CFO dashboards.

---

## Session 2 — GAAP & Accounting Principles

**Concepts (the "why")**
1. **Business entity** — owner is separate from business.
2. **Money measurement** — only money-quantifiable transactions recorded.
3. **Going concern** — entity will continue indefinitely (justifies historical cost over liquidation value).
4. **Cost (historical)** — assets recorded at acquisition cost.
5. **Dual aspect** (foundation of double-entry) — every Dr has a corresponding Cr.
6. **Accounting period** — financial reporting at regular intervals.
7. **Realisation** — revenue recognised when earned (control transferred), not when cash received.
8. **Matching** — expenses matched with the revenue they generated.
9. **Accrual** — record economic events when they occur, not when cash flows.

**Conventions (the "how")**
- **Consistency** — same methods across periods (allows trend analysis).
- **Conservatism (prudence)** — anticipate losses, not gains.
- **Full disclosure** — all material information in notes.
- **Materiality** — only significant items need separate treatment.

**Why these matter**
- They explain *why* financial statements look the way they do, and the boundary cases where rules permit judgement (and hence allow management to introduce **bias**).
- Common red flags: aggressive revenue recognition; off-balance-sheet financing; capitalising operating costs.

---

## Session 3-4 — Journal, Ledger, Trial Balance, Financial Statements

**Accounting equation** — Assets = Liabilities + Equity (always balances).

**Account types & rules** (Modern: debit increases / decreases)
| Type | Increase | Decrease | Normal balance |
|------|----------|----------|----------------|
| Asset | Dr | Cr | Dr |
| Expense | Dr | Cr | Dr |
| Liability | Cr | Dr | Cr |
| Income | Cr | Dr | Cr |
| Capital/Equity | Cr | Dr | Cr |

**Journal entry format**
```
Date  | Particulars                         | LF | Dr (₹) | Cr (₹)
xx/yy | Cash A/c             Dr             |    | 50,000 |
      |    To Sales A/c                     |    |        | 50,000
      | (Being cash sale of goods)          |    |        |
```

**Posting to ledger** — group by account; running balance maintained.

**Trial Balance**
- Lists every ledger account with Dr/Cr balances at a date.
- Checks arithmetic accuracy of postings (Dr total = Cr total).
- **Errors NOT detected by TB**: error of omission (transaction missed), error of commission (wrong account, same side), error of principle (wrong category), compensating errors.

**From TB to Financial Statements**
- **Trading account** (manufacturing/trading firms) → Gross Profit.
- **Profit & Loss A/c** → Net Profit (after operating + non-operating items).
- **Balance Sheet** → financial position at a point in time.
- **Cash Flow Statement** → cash from Operating, Investing, Financing (Direct or Indirect method).

**Adjusting entries (must do before P&L/B/S)**
- Outstanding expenses (accrue), Prepaid expenses (defer), Accrued income, Income received in advance, Depreciation, Bad debts, Provision for doubtful debts, Closing stock.

**Cash vs Profit**
- "Cash is King" — a profitable company can still go bust if working capital is mismanaged. Profit is opinion (driven by accruals); cash is fact.

---

## Session 5 — IFRS / IAS & Quality of Financial Reporting

**Why IFRS matter** — Indian listed companies follow Ind-AS (converged with IFRS); MNCs prepare consolidated reports under IFRS. Investor comparability across geographies depends on a single high-quality framework.

**Selected IFRS standards (per handout)**

| Standard | Topic | Key principle |
|----------|-------|---------------|
| **IFRS S1** | General sustainability disclosures | Disclose material sustainability risks/opportunities affecting cash flows |
| **IFRS S2** | Climate-related disclosures | Climate risks (physical, transition), GHG metrics, transition plans |
| **IFRS 5** | Non-current assets held for sale & discontinued operations | Measure at lower of carrying amount and FV − costs to sell; present discontinued ops separately |
| **IFRS 7** | Financial instruments — disclosures | Risk exposures (credit/liquidity/market) and how they are managed |
| **IFRS 8** | Operating segments | Disclose segments as the CODM views them ("management approach") |
| **IFRS 13** | Fair Value Measurement | Define FV; 3-level hierarchy (Level 1 quoted, Level 2 observable, Level 3 unobservable) |
| **IFRS 15** | Revenue from contracts with customers | **5-step model**: identify contract → identify performance obligations → determine TP → allocate → recognise as obligation satisfied |
| **IAS 2** | Inventories | Lower of cost and NRV; **LIFO prohibited** under IFRS (FIFO/Weighted average allowed) |
| **IAS 16** | Property, Plant & Equipment | Cost or revaluation model; depreciate over useful life; capitalise component costs |

**US GAAP vs IFRS — R&D**
- **US GAAP**: R&D expensed as incurred (very few exceptions).
- **IFRS (IAS 38)**: Research expensed; **Development capitalised** if 6 PIRATE criteria met (technical feasibility, intent, ability to use/sell, future benefits, resources, reliable cost measurement). Result: tech firms reporting under IFRS may show higher assets and EBITDA.

**Quality of Financial Reporting — Red Flags**
- Aggressive revenue recognition (channel stuffing, bill-and-hold).
- Capitalising R&D / repairs that should be expensed.
- Frequent "one-time" charges that recur.
- Big bath restructurings.
- Off-balance-sheet financing (operating leases pre-IFRS 16, SPVs).
- Related-party transactions on non-arm's-length terms.
- Sudden auditor changes.

**Where reporting falls short**
- Intangible assets (brands, customer relationships, R&D) often invisible.
- Conservatism creates a downward bias in modern asset-light businesses.
- ESG/non-financial impact only now emerging via IFRS S1/S2.

---

> **Mid-Semester scope ends here (Sessions 1–8).** Closed Book, 2 hrs, 30 % weight, **20-Jun-2026 (AN)**.
> Note: per handout, mid-sem covers sessions 1–8, which means the first part of ratio analysis (session 8) is in scope; deeper case-study work (sessions 11-13) is not.

---

## Session 6-7 — Understanding & Analysing Financial Statements

**Income Statement (P&L)** — performance over a period
- Revenue → Gross Profit → Operating Profit (EBIT) → Profit before Tax → Net Profit (PAT).
- Schedule III format (India) follows function-of-expense.
- Non-operating: interest income, FX gains, exceptional items.

**Balance Sheet** — financial position at a date
- **Assets**: Non-current (PPE, Intangibles, Investments) + Current (Inventory, Receivables, Cash).
- **Liabilities**: Non-current (long-term debt, deferred tax) + Current (payables, short-term debt, taxes due).
- **Equity**: Share capital + Reserves & Surplus.
- Schedule III India: liquidity order (current assets first under "current assets" heading).

**Cash Flow Statement** — cash movement
- **Operating** = cash from core business (use Indirect: PAT + non-cash + WC changes).
- **Investing** = capex, divestments, investments bought/sold.
- **Financing** = debt raised/repaid, dividends paid, share issues/buybacks.

**Reading between the lines**
- Profit growth without cash flow growth → potential channel stuffing or working-capital bloat.
- High depreciation but low capex → ageing asset base.
- Negative operating cash but positive financing → debt-funded operations (unsustainable).
- Sudden jump in receivables vs sales → quality of revenue concern.

**Significance**
- Predict bankruptcy (Altman Z-score uses ratios).
- Benchmark vs industry (asset-light vs asset-heavy).
- Spot inflexion points before they show in profit.

---

## Session 8-10 — Ratio Analysis

> Session 8 is included in mid-sem scope; sessions 9–10 are comprehensive scope only.

**Liquidity ratios** (short-term solvency)
- **Current Ratio** = Current Assets / Current Liabilities (norm 1.5–2.0).
- **Quick (Acid Test) Ratio** = (CA − Inventory − Prepaid) / CL (norm ≥ 1.0).
- **Cash Ratio** = (Cash + Marketable Securities) / CL.
- **Working Capital** = CA − CL.

**Solvency / Leverage** (long-term)
- **Debt-Equity** = Long-term Debt / Equity.
- **Debt Ratio** = Total Debt / Total Assets.
- **Interest Coverage (TIE)** = EBIT / Interest Expense.
- **Equity Multiplier** = Total Assets / Equity.

**Profitability**
- **Gross Margin** = GP / Sales.
- **Operating Margin** = EBIT / Sales.
- **Net Margin** = PAT / Sales.
- **Return on Assets (ROA)** = PAT / Total Assets.
- **Return on Equity (ROE)** = PAT / Equity.
- **Return on Capital Employed (ROCE)** = EBIT / Capital Employed.

**Efficiency / Activity**
- **Inventory Turnover** = COGS / Avg Inventory; **Days Inventory** = 365/Inv. T/O.
- **Receivable Turnover** = Credit Sales / Avg Receivables; **Days Sales Outstanding (DSO)** = 365/RT.
- **Payable Turnover** = Credit Purchases / Avg Payables; **DPO** = 365/PT.
- **Cash Conversion Cycle (CCC)** = DSI + DSO − DPO. Lower is better.
- **Asset Turnover** = Sales / Total Assets.

**DuPont Decomposition**
- **3-step ROE** = Net Margin × Asset Turnover × Equity Multiplier.
- **5-step ROE** = Tax Burden × Interest Burden × EBIT Margin × Asset Turnover × Equity Multiplier.

**Identifying organisations from ratios**
| Industry profile | Tell-tale ratios |
|------------------|-----------------|
| FMCG / Consumer | Low margin, high asset turnover, low DSO, modest debt |
| Pharma / Tech | High margin, high R&D, low asset turnover (intangibles invisible) |
| Banking | Very high leverage (12-15× equity multiplier), thin margin |
| Power / Infra | Heavy fixed assets, high D/E, cyclical earnings |
| E-commerce | Negative working capital (collect first, pay later), low margin, high revenue growth |
| NGO | No equity / no profit motive; revenue = grants; expense ratio scrutiny |

**Limitations of ratios**
- Historical data, may not predict future.
- Inflation distorts comparisons.
- Window-dressing: year-end transactions designed to flatter ratios.
- Industry comparison only meaningful with apples-to-apples accounting policies.
- Single ratio in isolation misleading — always interpret in groups.

---

## Session 11-13 — Empirical / Case Study FS Analysis

**Approach**
1. Pick 1-4 listed companies (per ELC group size).
2. Pull last 5 years annual reports (Bloomberg/Capitaline/screener.in/company website).
3. Compute all key ratios; do **trend analysis** (year-on-year), **comparative analysis** (vs peers), **industry analysis** (vs sector average).
4. Comment on:
   - **Cost-structure risk** (operating leverage from CVP).
   - **Liquidity** (CR, QR, CCC).
   - **Leverage** (D/E, ICR; operating leverage = %ΔEBIT / %ΔRevenue; financial leverage = %ΔEPS / %ΔEBIT).
   - **Profitability** (Economic = ROCE, Commercial = Margins, Owners' = ROE/EPS/Dividend yield).

**Common-size statements** (vertical analysis)
- P&L items expressed as % of Revenue.
- B/S items expressed as % of Total Assets.
- Useful for cross-firm comparison irrespective of size.

**Comparative statements** (horizontal analysis)
- Show absolute and % changes year-on-year.
- Spots growth, decline, abnormal items.

**Trend analysis**
- Index numbers with base year (Year 1 = 100).
- 5-year CAGR for revenue, profit, dividends.

**Cross-checks for case work**
- Free Cash Flow to Firm (FCFF) = EBIT(1−t) + D&A − Capex − ΔWC.
- Working capital trend.
- Receivable concentration.
- Auditors' qualifications, KAMs (Key Audit Matters), notes to accounts.

**Sample interpretation phrases (for the report)**
- "EBITDA margin expanded 220 bps over FY21-25 driven by operating leverage as revenue grew 18 % CAGR."
- "Cash conversion cycle deteriorated from 32 days to 51 days, suggesting weakening collection discipline."
- "ROCE of 22 % is 600 bps above the industry median of 16 %, reflecting superior asset utilisation."

---

## Session 14-15 — Cost Accounting and CVP

**Cost classification**
- **Behaviour**: Fixed (constant in total), Variable (constant per unit), Mixed/Semi-variable, Step.
- **Function**: Production, Selling & Distribution, Administration, R&D.
- **Identifiability**: Direct (traceable) vs Indirect (overheads).
- **Decision relevance**: Relevant (future, differential) vs Sunk; Avoidable vs Unavoidable; Opportunity cost.
- **Element**: Material, Labour, Overheads.

**Prime Cost** = Direct Material + Direct Labour + Direct Expenses.
**Conversion Cost** = Direct Labour + Manufacturing Overhead.
**Cost of Goods Sold** = Opening Stock + Production Cost − Closing Stock.

**Cost sheet (illustrative)**
```
Direct Material Consumed                  X
+ Direct Labour                            X
+ Direct Expenses                          X
= Prime Cost                              XX
+ Factory Overheads                        X
= Works Cost                              XX
+ Office & Administrative Overheads        X
= Cost of Production                      XX
+ Selling & Distribution Overheads         X
= Cost of Sales                           XX
+ Profit                                   X
= Sales                                   XX
```

**Cost-Volume-Profit (CVP) Analysis**
- **Contribution Margin (per unit)** = Selling Price − Variable Cost.
- **Contribution Margin Ratio (P/V Ratio)** = CM/SP × 100 %.
- **Break-even Point (units)** = Fixed Cost / CM per unit.
- **Break-even Point (₹)** = Fixed Cost / P/V Ratio.
- **Margin of Safety** = Actual Sales − BE Sales (also %).
- **Target Profit Sales** = (Fixed Cost + Target Profit) / CM per unit.
- **Operating Leverage** = Contribution / EBIT — measures earnings sensitivity to revenue change.

**Decision-making applications (handout-emphasised)**
- **Make-or-buy** — compare relevant cost of making (variable + avoidable fixed) vs price of buying.
- **Special order** — accept if price ≥ relevant variable cost (assuming spare capacity, no impact on regular customers).
- **Pricing** — use variable cost as floor; consider full cost for long-run sustainability.
- **Product mix** — under capacity constraint, choose product with highest CM per unit of constrained resource.

---

## Session 16 — Budgeting & Variance Analysis

**Why budget?**
- Plan resources, coordinate functions, set performance benchmarks, motivate, control.

**Types of budgets** (per handout)
- **Master Budget** — consolidates all sub-budgets into projected P&L, B/S, CF.
- **Operating Budget** — Sales, Production, Material, Labour, Overhead, S&D, Admin.
- **Capital Budget** — long-term capex (NPV/IRR for project selection).
- **Financial Budget** — Cash, Capex, B/S.
- **Zero-Based Budget (ZBB)** — start every period from zero; justify every expense (vs incremental budgeting).
- Other classes: Fixed vs Flexible; Long-term vs Short-term.

**Cash budget format**
```
Opening Cash
+ Cash Receipts (collections, asset sales, loans, equity)
− Cash Payments (suppliers, wages, expenses, capex, tax, dividends, loan repayment)
= Closing Cash
```

**Variance Analysis** — actual vs standard/budget
- **Material Variance**:
  - Material Cost Variance (MCV) = (SQ × SP) − (AQ × AP).
  - Material Price Variance (MPV) = AQ × (SP − AP).
  - Material Usage Variance (MUV) = SP × (SQ − AQ).
- **Labour Variance**:
  - Labour Cost Variance.
  - Labour Rate Variance = AH × (SR − AR).
  - Labour Efficiency Variance = SR × (SH − AH).
- **Overhead Variance** — Variable & Fixed.
- **Sales Variance** — Volume + Price.

**Favourable (F)** vs **Adverse (A)** — F when actual better than standard; A when worse.

**Use in performance management**
- Investigate only material variances (management by exception).
- Trace variance to responsibility centres for accountability.
- Standard costing is the foundation for variance analysis (set realistic standards).

**Modern angle**
- Beyond Budgeting movement — rolling forecasts replace static annual plans.
- AI/ML driven driver-based forecasts in modern FP&A.

---

## Cross-cutting reference: ELC project framework

The ELC marks (15) hinge on:
- **5 marks** — calculate **appropriate ratios and parameters** (don't dump every ratio; pick those relevant to industry/firm).
- **10 marks** — **critical analysis and interpretation** (story, not numbers).

**Framework**
1. Industry context (size, growth, key players, regulatory environment).
2. Company background (business model, segments, geography).
3. 5-year financial highlights table.
4. Profitability deep-dive (DuPont 5-step).
5. Liquidity & working capital trends.
6. Leverage and risk (operating + financial leverage).
7. Cash flow analysis (quality of earnings = OCF / PAT).
8. Comparative / industry analysis.
9. Red-flag scan.
10. Investment / management recommendations.
