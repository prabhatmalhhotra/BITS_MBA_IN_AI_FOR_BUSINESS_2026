# Operations Management — Chapter-wise Notes

> Anchored to Heizer, Render & Munson (T1). India-aware examples.

---

## Chapter 1 — Operations & Productivity

**OM** = activities that create value in the form of goods/services by transforming inputs to outputs.

### Productivity
- Single-factor: Output / single input (e.g., units / labour-hour).
- Multi-factor: Output / (labour + capital + material + energy).
- Total productivity = Output / Total inputs.

### 10 strategic OM decisions
Design of goods/services · Quality management · Process & capacity · Location · Layout · HR & job design · Supply chain · Inventory · Scheduling · Maintenance.

### 60-second recap
OM converts inputs to value-added outputs. Productivity is the heartbeat metric. Ten strategic decisions span the lifecycle from product design to supply chain to maintenance.

---

## Chapter 2 — Operations Strategy in a Global Environment

Strategies: cost leadership (Walmart, JioMart), differentiation (Apple), response (Zara, Zomato).

Make-or-buy: cost vs strategic-control trade-off.

Outsourcing risks: quality, IP, dependence, hidden costs.

### 60-second recap
Operations strategy aligns capabilities to chosen competitive priority. Globalisation expands options but adds complexity, currency and supply-chain risks.

---

## Chapter 3 — Project Management

### CPM
1. List activities with durations and predecessors.
2. Build network (AON or AOA).
3. Compute ES, EF (forward pass), LS, LF (backward pass).
4. Slack = LS − ES = LF − EF.
5. Critical path = activities with zero slack.

### PERT (probabilistic)
- Activity time t = (a + 4m + b) / 6, variance σ² = ((b − a)/6)².
- Project duration distribution = sum of critical-path activities; project σ² = sum of variances on critical path.
- Probability of completing by date T → use Z-score.

### Crashing
Reduce duration of critical activities at cost — pick lowest cost-slope activities first until next iteration is non-economic.

### 60-second recap
CPM finds the longest path (= shortest possible project duration). PERT adds uncertainty. Crashing trades money for time on critical activities.

---

## Chapter 4 — Forecasting

### Methods
- Naïve: forecast next = last period actual.
- Moving Average: average of last n periods.
- Weighted MA: assign weights summing to 1.
- Exponential Smoothing: F(t+1) = α·A(t) + (1−α)·F(t). α high → responsive; α low → stable.
- Holt's (trend): adds trend smoothing β.
- Holt-Winters (seasonality): adds seasonal smoothing γ.
- Linear regression: y = a + bx (associative).

### Error measures
- MAD = Σ|error|/n
- MSE = Σ(error)²/n
- MAPE = Σ(|error|/A)·100/n
- Tracking signal = Σ(error)/MAD; alert if outside ±4 to ±6.

### ML-based forecasting (intro)
ARIMA, Prophet, LSTM/Transformer. Useful for high-frequency, multi-feature series.

### 60-second recap
Forecasting is structured guessing. Use moving averages for stable series, exponential smoothing for level/trend/seasonality, regression for causal drivers, ML for complex patterns. Always measure errors.

---

## Chapter 5 — Design of Goods and Services

### NPD process
Idea → Screening → Concept testing → Business analysis → Prototype → Test marketing → Launch.

### QFD (House of Quality)
Translates customer requirements ("voice of customer") into engineering specifications. Helps align design with what customers value.

### Other concepts
- **Concurrent engineering**: cross-functional teams design together — faster cycle.
- **Value engineering**: deliver same function at lower cost.
- **Modular design**: standardised modules → variety + economies of scale.
- **Robust design (Taguchi)**: insensitive to variations in inputs.

### Service design
- Customer contact intensity affects design (high contact = harder to standardise).
- Front-stage (visible to customer) vs back-stage.

### 60-second recap
Design influences ~70% of total cost. QFD anchors design to customer needs. Modular and robust design enable scale and reliability.

---

## Chapter 6 — Quality Management

### Cost of Quality (PAF)
Prevention + Appraisal + Internal Failure + External Failure. Investment in prevention pays back through reduced failure costs.

### TQM principles
Customer focus, continuous improvement (Kaizen), employee involvement, fact-based decisions, supplier partnership.

### Six Sigma DMAIC
Define → Measure → Analyse → Improve → Control. Target 3.4 defects per million opportunities (DPMO).

### 7 QC tools
1. Cause-effect (Ishikawa / fishbone)
2. Pareto chart (80/20)
3. Control chart
4. Scatter diagram
5. Histogram
6. Check sheet
7. Flow chart

### ISO 9000
Process standards for quality management systems; certification audited externally.

### 60-second recap
Quality is built in, not inspected in. PAF reframes quality as investment. TQM = culture, Six Sigma = methodology, ISO = compliance framework.

---

## Chapter 7 — Statistical Process Control (SPC)

### Common vs special causes
Common = inherent process variation. Special = assignable cause (e.g., new operator, machine fault). SPC detects special causes.

### Control charts (variables)
**X̄ chart** (process mean):
UCL = X̄̄ + A₂R̄
LCL = X̄̄ − A₂R̄

**R chart** (process range):
UCL = D₄R̄
LCL = D₃R̄

A₂, D₃, D₄ from standard tables, depend on subgroup size n.

### Control charts (attributes)
**p chart** (proportion defective):
UCL = p̄ + 3√(p̄(1−p̄)/n); LCL = p̄ − 3√(p̄(1−p̄)/n).

**c chart** (defects per unit):
UCL = c̄ + 3√c̄; LCL = c̄ − 3√c̄.

### Process capability
- Cp = (USL − LSL) / 6σ.
- Cpk = min[(USL − μ)/3σ, (μ − LSL)/3σ].
- Cpk ≥ 1.33 typical industry target; 1.67 for safety-critical.

### 60-second recap
SPC distinguishes inherent noise from assignable signals. Cp = potential capability; Cpk = actual capability accounting for centring.

---

## Chapter 8 — Process Strategy & Capacity

### Process types
| Type | Volume | Variety | Example |
|------|-------|--------|---------|
| Process focus (job shop) | Low | High | Custom tailoring |
| Repetitive | Medium | Medium | Cars, appliances |
| Product focus (mass) | High | Low | Sugar, cement |
| Mass customization | High | High | Dell, Nike By You |

### Capacity terms
- Design capacity: max output under ideal conditions.
- Effective capacity: realistic max given product mix, scheduling, maintenance.
- Utilization = Actual / Design.
- Efficiency = Actual / Effective.
- Required capacity = Forecasted demand × (1 + safety margin) / (Utilization × Efficiency).

### 60-second recap
Match process type to volume/variety. Capacity planning requires distinguishing design from effective and accounting for utilization and efficiency.

---

## Chapter 9 — Location Decisions

### Factor rating method
Assign weights to factors (labour cost, infrastructure, market access). Score each location. Weighted sum → highest wins.

### Centre of gravity
Coordinates: x* = Σ(wᵢxᵢ)/Σwᵢ; y* = Σ(wᵢyᵢ)/Σwᵢ.

### Break-even location
Compute total cost (FC + VC × volume) for each location across volume range; pick lowest at expected volume.

### Transportation method (LP)
Minimise total transport cost subject to supply and demand constraints. Solve via NW corner / VAM / Solver.

### 60-second recap
Location is a long-horizon, hard-to-reverse decision. Use factor rating for qualitative weights, centre of gravity for distribution centres, LP for multi-source/multi-destination optimisation.

---

## Chapter 10 — Layout Strategies

### Layout types
- **Process layout**: similar machines grouped (job shop).
- **Product layout**: line layout for high volume (assembly line).
- **Fixed-position**: product stays put (ship building).
- **Cellular**: small group of dissimilar machines for product family.
- **Retail / warehouse / office**: optimise customer flow / storage / collaboration.

### Line balancing (product layout)
- Cycle time = Production time per day / Required units per day.
- Theoretical min stations = Σ task times / Cycle time (round up).
- Assign tasks to stations using rules (longest task time, most followers).
- Efficiency = Σ task times / (Actual stations × Cycle time).

### Process layout (load-distance)
Minimise total flow × distance between departments.

### 60-second recap
Layout determines flow efficiency. Match layout type to volume/variety. Line balancing for product layouts; load-distance for job shops.

---

## Chapter 11 — Inventory Management

### ABC analysis
Top 20% items → ~80% value (A items); next 30% → 15% (B); bottom 50% → 5% (C). Tighter control on A items.

### EOQ model
Q* = √(2DS/H).
- D = annual demand
- S = setup/order cost
- H = holding cost per unit per year
- Total cost at Q* = √(2DSH)
- Number of orders = D/Q*; Time between orders = Q*/D.

### Production Order Quantity (EPQ)
Q*p = √[2DS / (H × (1 − d/p))], where d = demand rate, p = production rate.

### Quantity discount
Compute total cost = D·P + (D/Q)·S + (Q/2)·H for each price break; pick lowest valid Q.

### Reorder point
ROP = (Demand per day) × (Lead time) + Safety stock.
Safety stock = Z × σ_d × √L (continuous review).

### Service level
P(no stockout during lead time). Common: 95% → Z=1.65; 99% → Z=2.33.

### 60-second recap
EOQ balances ordering and holding costs. Safety stock buys service level at the cost of holding. ABC focuses control where it matters.

---

## Chapter 12 — Aggregate Planning & MRP

### Aggregate planning options
- **Chase**: produce exactly to demand (vary workforce).
- **Level**: constant production; absorb variation in inventory.
- **Mixed**: blend (e.g., level workforce + overtime + subcontracting).

### MRP
1. MPS (Master Production Schedule) — what end items, when.
2. BOM (Bill of Materials) — what components per unit.
3. Inventory records — what's on hand / on order.
4. Logic: Net req = Gross req − On hand + Safety stock; offset by lead time.

### ERP
Integrates MRP with finance, HR, sales, procurement (SAP, Oracle, Microsoft Dynamics).

### 60-second recap
Aggregate planning sets the volume game. MPS converts it to specific items. MRP explodes that into raw-material requirements via BOM and lead times. ERP integrates everything.

---

## Chapter 13 — Short-Term Scheduling

### Loading methods
- **Gantt chart**: visual timeline.
- **Assignment method (Hungarian)**: assign n jobs to n workers minimising total cost.

### Sequencing rules (single machine)
- **FCFS**: First come first served.
- **SPT**: Shortest processing time first → minimises avg flow time.
- **EDD**: Earliest due date → minimises max lateness.
- **LPT**: Longest first → useful in parallel-machine load balancing.
- **CR (Critical Ratio)** = Time remaining / Work days remaining.

### Johnson's rule (2 machines)
1. List jobs with times on M1, M2.
2. Find shortest. If on M1 → schedule first. If on M2 → schedule last.
3. Cross out and repeat.

### Theory of Constraints (TOC)
Throughput limited by bottleneck. Steps: Identify → Exploit → Subordinate → Elevate → Repeat.

### 60-second recap
Sequencing rules optimise different objectives (avg flow time vs lateness vs makespan). Johnson's rule for 2-machine flow shop. TOC focuses improvement at the bottleneck.

---

## Chapter 14 — JIT, Lean & TPS

### JIT
Inventory is waste. Pull system (kanban) — produce only when downstream signals need.

### Lean — 8 wastes (TIMWOODS)
Transportation · Inventory · Motion · Waiting · Overproduction · Overprocessing · Defects · Skills (under-utilised people).

### 5S
Sort · Set in order · Shine · Standardize · Sustain.

### Value Stream Mapping (VSM)
Visualise material + information flow; identify value-added vs non-value-added time; reduce lead time.

### TPS pillars
- **JIT**: right thing at right time, right quantity.
- **Jidoka**: build quality in; stop the line on defect (Andon cord).

### 60-second recap
Lean = relentless waste elimination across material, time, motion. JIT pulls only what's needed. Jidoka empowers the line to stop on quality issues. 5S enforces workplace discipline.

---

## Chapter 15 — Maintenance & Reliability

### Reliability of system
- Series: R = R₁ × R₂ × … × Rₙ. Total reliability falls with each component.
- Parallel (redundancy): R = 1 − Π(1 − Rᵢ). Redundancy raises reliability.

### MTBF
Mean Time Between Failures = Total operating time / Number of failures.

### Maintenance types
- Breakdown: fix when broken (cheap to plan, expensive when fails).
- Preventive: scheduled (calendar/usage-based).
- Predictive: condition-based using sensors / IoT / ML — increasingly common with Industry 4.0.

### TPM
Total Productive Maintenance — operator-led routine maintenance + planned preventive + reliability-centred.

### 60-second recap
Reliability multiplies in series, blocks failure in parallel. MTBF measures reliability. Predictive maintenance (sensor + ML) is replacing fixed-schedule preventive in modern plants.

---

## Chapter 16 — Supply Chain Management

### Bullwhip effect
Demand variability amplifies upstream. Causes: order batching, price fluctuations, rationing/shortage gaming, demand forecasting in series. Mitigation: information sharing (POS data), VMI, EDLP pricing, smaller batches.

### Sourcing
- Outsourcing: focus on core competency; risks IP and dependence.
- Single vs multi-sourcing: cost vs resilience.
- Insourcing: reverse outsourcing trend (chip manufacturing).

### Logistics
- Modes: rail, road, air, sea, pipeline, intermodal.
- Cost-time-flexibility trade-off.

### Industry 4.0 in supply chain
- IoT for tracking
- Blockchain for provenance/payments
- AI/ML for demand forecasting, route optimisation, dynamic pricing
- Digital twins for what-if simulation

### Sustainability & resilience
Post-COVID: shift from "JIT-only" to "JIT + JIC (Just in Case)" buffers; near-shoring; multi-sourcing; ESG-aligned suppliers.

### 60-second recap
SCM = end-to-end orchestration. Bullwhip is the canonical pathology — fix with information sharing. Modern supply chains balance efficiency with resilience and sustainability, leaning on Industry 4.0 tech.
