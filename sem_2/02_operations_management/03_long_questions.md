# Operations Management — Long Questions

> 12 numerical/case questions. Mid + Comp prep.

---

### Q1. (15 m) A project has the following activities. Construct the network. Find ES, EF, LS, LF, slack. Identify critical path and project duration.

| Activity | Predecessor | Duration (days) |
|----------|-------------|----------------:|
| A | — | 4 |
| B | — | 6 |
| C | A | 3 |
| D | A | 5 |
| E | B | 4 |
| F | C, E | 6 |
| G | D | 5 |
| H | F, G | 4 |

**Forward pass**:
- A: ES=0, EF=4
- B: ES=0, EF=6
- C: ES=4, EF=7
- D: ES=4, EF=9
- E: ES=6, EF=10
- F: ES=max(7,10)=10, EF=16
- G: ES=9, EF=14
- H: ES=max(16,14)=16, EF=20

**Project duration = 20 days.**

**Backward pass** (from H, LF=20):
- H: LF=20, LS=16
- F: LF=16, LS=10
- G: LF=16, LS=11
- E: LF=10, LS=6
- D: LF=11, LS=6
- C: LF=10, LS=7
- B: LF=6, LS=0
- A: LF=min(7,6)=6, LS=2

**Slack** = LS − ES:
| Act | A | B | C | D | E | F | G | H |
|-----|--:|--:|--:|--:|--:|--:|--:|--:|
| Slack | 2 | 0 | 3 | 2 | 0 | 0 | 2 | 0 |

**Critical path: B → E → F → H** (slack = 0).

---

### Q2. (10 m) A demand series for 6 months: 100, 110, 120, 115, 130, 140. Compute 3-month MA forecast for month 7. Also exponential smoothing forecast (α = 0.3, F1 = 100). Compare MAD.

**3-month MA** (months 4-6 → forecast 7) = (115 + 130 + 140)/3 = **128.33**.

**Exponential smoothing** (α=0.3, F1=100, A1=100):
- F2 = 0.3×100 + 0.7×100 = 100
- F3 = 0.3×110 + 0.7×100 = 103
- F4 = 0.3×120 + 0.7×103 = 108.1
- F5 = 0.3×115 + 0.7×108.1 = 110.17
- F6 = 0.3×130 + 0.7×110.17 = 116.12
- F7 = 0.3×140 + 0.7×116.12 = **123.28**

**MAD comparison** for available periods (use months 4-6 actual):
- MA: forecasts at months 4-6 = (100+110+120)/3=110, (110+120+115)/3=115, (120+115+130)/3=121.67. Errors = 5, 15, 18.33. MAD = 12.78.
- ES: F4=108.1, F5=110.17, F6=116.12. Errors = 6.9, 19.83, 23.88. MAD = 16.87.

**MA is more accurate here**; series has trend, so ES with low α lags.

---

### Q3. (12 m) A bottling plant produces a single SKU. Annual demand 50,000 cases. Setup cost ₹2,500 per run. Holding cost ₹20 per case per year. Production rate 500/day, demand 200/day. (a) EPQ, (b) Max inventory, (c) Number of runs/yr, (d) Total cost.

(a) **EPQ** = √[2DS / (H × (1 − d/p))] = √[2×50,000×2,500 / (20×(1−200/500))]
   = √[2.5×10⁸ / (20×0.6)] = √[2.083×10⁷] = **4,564 cases**.

(b) **Max inventory** = Q* × (1 − d/p) = 4,564 × 0.6 = **2,738 cases**.

(c) **Runs per year** = D/Q* = 50,000/4,564 = **10.96 ≈ 11 runs**.

(d) **Total cost** = (D/Q)·S + (max inv / 2)·H = (50,000/4,564)×2,500 + (2,738/2)×20
   = 27,389 + 27,380 = **₹54,769/yr**.

(Setup and holding ≈ equal at EPQ — sanity check.)

---

### Q4. (12 m) Three product layouts: workstation tasks and times below. Daily working time 480 min, demand 96 units/day. (a) Cycle time, (b) Theoretical min stations, (c) Assign tasks to stations using longest-task rule, (d) Efficiency.

| Task | Time (min) | Predecessor |
|------|-----------:|-------------|
| A | 1 | — |
| B | 2 | A |
| C | 3 | A |
| D | 2 | B |
| E | 3 | C |
| F | 1 | D, E |
| G | 4 | F |

Total task time = 16 min.

(a) **Cycle time** = 480/96 = **5 min/unit**.

(b) **Theoretical min stations** = 16/5 = 3.2 → **4 stations**.

(c) **Assignment** (longest task rule, respecting precedence):

| Station | Tasks | Time used | Idle |
|---------|-------|----------:|-----:|
| 1 | A (1), C (3) | 4 | 1 |
| 2 | B (2), E (3) — wait, E needs C done. After Station 1, C is done so E available. Better: B(2), D(2) | 4 | 1 |

Let me re-do clean assignment:
- Station 1: A(1), C(3) = 4 min ✓
- Station 2: B(2), D(2) = 4 min ✓ (E needs C; C done in S1)
- Station 3: E(3), F(1) = 4 min ✓ (F needs D done; D done in S2)
- Station 4: G(4) = 4 min ✓

Total stations = 4.

(d) **Efficiency** = Σ task times / (n × Cycle time) = 16 / (4 × 5) = **80%**.

---

### Q5. (10 m) Service-level inventory: Daily demand normal mean 50, σ=15. Lead time 4 days (constant). Annual demand 365×50=18,250. Holding cost ₹10/unit/yr. Order cost ₹500. Service level 95%. Compute (a) EOQ, (b) Safety stock, (c) ROP.

(a) **EOQ** = √(2×18,250×500/10) = √1,825,000 = **1,351 units**.

(b) **Safety stock** at 95% (Z=1.65): SS = Z × σ_d × √L = 1.65 × 15 × √4 = 1.65 × 15 × 2 = **49.5 ≈ 50 units**.

(c) **ROP** = d × L + SS = 50 × 4 + 50 = **250 units**.

So order 1,351 units when stock falls to 250.

---

### Q6. (15 m) Discuss the Bullwhip Effect. Explain the four root causes with examples. Recommend mitigation strategies.

**Definition**: Bullwhip = amplification of demand variability as orders move upstream from retailer → distributor → factory → supplier. Small retail-level variation triggers large swings upstream.

**Root causes (8 m)**

1. **Demand-forecast updating** — Each tier forecasts off the prior tier's orders (not actual end demand), exaggerating with each step. Example: a 10% retail spike → distributor adds buffer → factory adds more → raw-material supplier double-orders.

2. **Order batching** — Cost of ordering encourages batched orders; downstream sees lumpy demand vs smooth consumption. Example: weekly purchase orders cause weekly factory peaks.

3. **Price fluctuation / Promotions** — Forward buying during discounts then under-buying after. Example: P&G promo causes pull-forward demand, then a trough.

4. **Rationing & shortage gaming** — When supply tight, customers over-order to secure allocation; when shortage clears, a glut appears. Example: chip shortage 2021–22 — auto OEMs over-ordered to safeguard build plans.

**Mitigation (7 m)**

1. **Information sharing** — share point-of-sale data upstream (Walmart Retail Link, Apple supplier data feed).
2. **Vendor-managed inventory (VMI)** — supplier monitors and replenishes; smooths tier-level variability.
3. **Reduce order batching** — smaller, more-frequent orders enabled by lower transaction costs (EDI, auto-replenishment).
4. **EDLP (Every Day Low Price)** — smooth demand by avoiding promotional spikes.
5. **Allocation rules tied to past sales** — discourage gaming during shortages.
6. **Collaborative forecasting (CPFR)** — joint planning between trading partners.
7. **Shortened lead times** — smaller forecasting horizon → smaller error → smaller buffer.
8. **AI/ML demand sensing** — incorporate POS, weather, social signals to forecast end demand directly.

**Result**: well-known case studies (P&G with Pampers, Cisco) show 30-60% inventory reduction and improved service levels post-mitigation.

---

### Q7. (12 m) An Indian textile mill makes shirts. Quality data: Defect rate 4%. Daily output 5,000. Cost of internal defect ₹50/shirt; external defect ₹500/shirt (warranty + brand damage). Currently 80% caught internally. Quality manager proposes ₹15 lakh investment in inspection raising internal catch to 95%. Justify with cost analysis.

**Current state**:
Total defects/day = 5,000 × 0.04 = 200.
Internal: 200 × 0.80 = 160 → cost = 160 × 50 = ₹8,000/day.
External: 200 × 0.20 = 40 → cost = 40 × 500 = ₹20,000/day.
Total quality cost = ₹28,000/day = ₹28,000 × 300 days = ₹84 lakh/yr.

**After investment**:
Internal: 200 × 0.95 = 190 → cost = 190 × 50 = ₹9,500/day.
External: 200 × 0.05 = 10 → cost = 10 × 500 = ₹5,000/day.
Total = ₹14,500/day = ₹14,500 × 300 = ₹43.5 lakh/yr.

**Annual saving** = 84 − 43.5 = **₹40.5 lakh/yr**.

**Payback** = 15 / 40.5 = **0.37 years (~4.5 months)**.

**Recommendation**: Proceed. ROI is overwhelming. Additionally, external defect costs underestimate brand damage and customer churn; the true benefit is even higher. Long-term, invest in **prevention** (process improvement, training) to reduce defect rate from 4% itself (Cost of Quality philosophy: prevention < appraisal < failure).

---

### Q8. (15 m) Discuss lean manufacturing. Explain 8 wastes (TIMWOODS) with one example each from a software services company.

**Lean** = systematic elimination of waste (anything that doesn't add customer value), originating from Toyota Production System.

**8 wastes (TIMWOODS) — software example each**:

1. **Transportation** — Moving deliverables/tickets across teams unnecessarily. *Example*: A bug ticket bouncing between 4 teams before someone owns it.

2. **Inventory** — Unfinished work-in-progress (WIP). *Example*: Backlog of 200 user stories nobody will get to in 6 months.

3. **Motion** — Wasted human movement. *Example*: Switching between 8 tools per day; no single dashboard.

4. **Waiting** — Idle time. *Example*: Waiting for code review for 3 days.

5. **Overproduction** — Producing more than needed. *Example*: Building 10 features in a release where customer needed 3.

6. **Overprocessing** — Doing more work than the customer values. *Example*: Polishing UI of an internal admin tool that 5 power users will use.

7. **Defects** — Errors and rework. *Example*: Production bugs that weren't caught in testing.

8. **Skills (under-utilisation)** — Not using people's full talent. *Example*: A senior engineer doing manual ticket triage.

**Implementation tools**: 5S, kanban boards, value stream mapping (lead time → value-added time ratio), daily stand-ups, retrospectives. Many software-industry agile practices are direct lean descendants.

---

### Q9. (12 m) A 3-component series system has reliabilities 0.95, 0.92, 0.90. (a) System reliability. (b) If component 3 is paralleled with an identical backup (R=0.90), what is the new system reliability? (c) Comment.

(a) **Series**: R = 0.95 × 0.92 × 0.90 = **0.7866**.

(b) Component 3 with backup (parallel): R₃' = 1 − (1 − 0.90)² = 1 − 0.01 = **0.99**.
   New system: R = 0.95 × 0.92 × 0.99 = **0.8653**.

(c) **Comment**: Adding a single redundancy raised reliability from 0.787 → 0.865 (10% improvement). Redundancy is most cost-effective on the **weakest** component. Industries (aerospace, healthcare, data centres) routinely use redundancy on critical paths.

---

### Q10. (15 m) Discuss the Theory of Constraints (TOC). A factory has 4 stations with capacities (units/day) 100, 80, 60, 90. Daily demand 100. (a) Identify bottleneck and throughput. (b) Apply TOC's 5 focusing steps to maximise throughput. (c) Discuss DBR (drum-buffer-rope).

(a) **Bottleneck = Station 3 (60 units/day)**. System throughput = 60 units/day (cannot exceed bottleneck). Loss vs demand = 100 − 60 = 40 units/day.

(b) **TOC 5 focusing steps**:

1. **Identify**: Station 3 is the constraint.
2. **Exploit**: Maximise Station 3 utilisation — eliminate setup time, breaks, micro-stoppages; ensure no defective parts reach it (waste of bottleneck time).
3. **Subordinate**: Other stations should NOT produce more than Station 3 can consume; otherwise WIP piles up. Pull system: Station 1 produces only when Station 3 signals. (Drum-Buffer-Rope.)
4. **Elevate**: Add capacity to bottleneck — extra shift, parallel machine, automation. Possibly raise capacity from 60 to 100.
5. **Repeat**: After elevating Station 3, the new bottleneck might be Station 2 (80). Repeat the cycle.

(c) **DBR**:
- **Drum**: bottleneck sets the production rhythm.
- **Buffer**: small protective inventory before bottleneck so it never starves.
- **Rope**: signal back to first operation (Station 1) to release work only at bottleneck rate.

This eliminates over-production at non-bottlenecks and protects throughput.

---

### Q11. (10 m) Six-sigma case: A call centre has avg call handling time 360 sec, σ=30 sec. Customer requirement: 360 ± 60 sec. (a) Cp, Cpk. (b) DPMO if mean shifts to 380 sec. (c) Recommend.

(a) **Cp** = (USL − LSL) / 6σ = (420 − 300) / 180 = **0.667**. (Process not capable; below 1.0.)

**Cpk** = min[(USL − μ)/3σ, (μ − LSL)/3σ] = min[(420 − 360)/90, (360 − 300)/90] = min[0.667, 0.667] = **0.667** (process centred).

(b) **Mean shifts to 380**:
Cpk' = min[(420 − 380)/90, (380 − 300)/90] = min[0.444, 0.889] = **0.444**.

DPMO (one-sided upper, if normal): Z = (USL − μ)/σ = (420 − 380)/30 = 1.33. P(Z>1.33) = 0.0918 = 9.18% defects above. With ~0% below LSL (Z = (380-300)/30 = 2.67, very low tail), total ≈ 9.5% → 95,000 DPMO. Way above six-sigma target (3.4 DPMO).

(c) **Recommendations**: (i) Reduce variation σ first — root cause analysis, training; (ii) Re-centre mean to 360; (iii) Drive Cpk to ≥1.33 → σ must drop to ~15 sec while staying centred.

---

### Q12. (15 m) Mini-case: An Indian e-commerce firm wants to choose a fulfilment centre location. 3 candidate cities; 4 weighted factors. Apply factor rating method and recommend.

| Factor | Weight | City A | City B | City C |
|--------|------:|------:|------:|------:|
| Labour cost | 0.30 | 7 | 9 | 8 |
| Infrastructure | 0.25 | 9 | 7 | 8 |
| Proximity to market | 0.25 | 8 | 6 | 9 |
| Government incentives | 0.20 | 6 | 9 | 7 |

**Weighted scores**:
- A: 0.30×7 + 0.25×9 + 0.25×8 + 0.20×6 = 2.10 + 2.25 + 2.00 + 1.20 = **7.55**
- B: 0.30×9 + 0.25×7 + 0.25×6 + 0.20×9 = 2.70 + 1.75 + 1.50 + 1.80 = **7.75**
- C: 0.30×8 + 0.25×8 + 0.25×9 + 0.20×7 = 2.40 + 2.00 + 2.25 + 1.40 = **8.05**

**Recommendation: City C** (highest weighted score 8.05).

**Discussion**:
- C wins on proximity to market (highest weight after labour) — critical for last-mile delivery cost and SLA.
- B has best labour cost and incentives but loses on market proximity (long-tail logistics cost would erode short-term savings).
- A has best infrastructure but is balanced too thinly across other factors.

**Caveats**:
- Sensitivity analysis: if weights shift (e.g., labour 0.40 vs 0.30), B may win.
- Qualitative factors not in matrix: regulatory ease, ecosystem (3PLs), scalability, climate risk (flooding etc.).
- Consider hybrid: a large hub in C + smaller satellite in B for cost arbitrage.
