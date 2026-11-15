# ASQ CSSBB — DMAIC & BBQ Bible Note-Taking Cheat Sheet

> **Purpose:** Every time you write a short & sweet note in your **BBQ Bible**, ASQ tests **which specific phase or BoK section** a tool/concept belongs to. Other Six Sigma institutions (IASSC, Villanova, company belts) sometimes place tools in different phases—on your March 2027 exam, **ONLY ASQ's classification counts!**

---

## 1. High-ROI Exam Priorities (Where the 150 Scored Questions Come From)

| Priority Tier | ASQ Domains | Scored Qs | Share of Exam | Study Strategy |
| :--- | :--- | :---: | :---: | :--- |
| **Tier 1: The Core Quantitative Engine** | **V. Measure (25)** + **VI. Analyze (22)** + **VII. Improve (21)** | **68 Qs** | **45.3%** | Nearly half the exam! Master MSA, $C_p/C_{pk}$ vs $P_p/P_{pk}$, Hypothesis Testing, Regression, FMEA, DOE ($2^k$ & Resolution), and Lean/OEE/TOC. |
| **Tier 2: Project Setup & Sustainment** | **IV. Define (20)** + **VIII. Control (17)** | **37 Qs** | **24.7%** | Easy-to-medium points if you know ASQ's exact rules on Problem Statements, VOC/CTQ/QFD, 7 M&P Tools, SPC Chart Selection, and Control Plans. |
| **Tier 3: Enterprise & People Leadership** | **III. Team Mgmt (15)** + **I. Org Planning (12)** + **II. Org Measures (12)** | **39 Qs** | **26.0%** | Fast conceptual & financial questions (NPV, ROI, COQ/PAF, Balanced Scorecard, Tuckman, Lencioni, Conflict Resolution, Roles). Great score booster! |
| **Tier 4: New Design (DFSS)** | **IX. DFSS (6)** | **6 Qs** | **4.0%** | Know DMADV vs DMADOV, DFX, Taguchi Loss Function $L(y)=k(y-T)^2$, Parameter vs Tolerance Design, and RSS tolerance stacking. |

---

## 2. Strict ASQ Phase-Placement Traps (Must-Know for BBQ Bible Notes!)

Watch out for these classic ASQ CSSBB exam distinctions:

| Tool / Topic | Where ASQ BoK Places It | Common Exam Trap to Avoid |
| :--- | :--- | :--- |
| **Financial Metrics (ROI, NPV, IRR, COQ/COPQ)** | **Domain I.A.4 & II.C.2** (Pre-DMAIC Enterprise) + **IV.B.1** (Business Case) | Don't confuse Prevention vs. Appraisal costs in COQ (audits/inspections/calibrations = **Appraisal**; training/FMEA/quality planning = **Prevention**). |
| **7 Management & Planning Tools** (Affinity, ID, Tree, Matrix, Prioritization, PDPC, Activity Network) | **Domain IV.D (Define Phase)** (used across DMAIC, tested under Define) | Know **Interrelationship Digraph (ID)** arrow counting: more **outgoing** arrows = **root driver/cause**; more **incoming** arrows = **key effect/outcome**. |
| **SIPOC vs. Detailed Process Maps / VSM** | High-level **SIPOC** scopes boundaries in **Define (IV.B.3)** & **Measure (V.A.2)**; **Detailed Process Maps, Swimlanes, Value Stream Maps (VSM), Takt Time, Little's Law** are in **Measure (V.A)**! | Many non-ASQ courses put VSM only in Lean/Improve—ASQ tests current-state VSM & flow metrics in **Measure (V.A)**! |
| **MSA / Gage R&R & Process Capability ($C_p, C_{pk}, P_p, P_{pk}$)** | **Measure Phase (V.C & V.F)** (re-verified in Control VIII.C) | Always check **MSA first**, then **SPC stability**, then **Normality** BEFORE trusting $C_p/C_{pk}$! |
| **Multi-Vari Charts** | **Measure Phase (V.D.4)** (Graphical Methods) | Plots positional (within-piece), cyclical (piece-to-piece), and temporal (time-to-time) variation before formal DOE. |
| **FMEA & Risk Management** | **Analyze Phase (VI.C)** in the 2022 ASQ BoK! | Other bodies put FMEA in Measure or Improve. In ASQ 2022 BoK, **VI.C Risk Analysis & Management (FMEA)** is explicitly tested under **Analyze** (and updated in Improve/Control). |
| **7 Wastes (TIMWOODS / DOWNTIME)** | **Waste Analysis** = **Analyze (VI.D.3)**; **Waste Elimination (5S, Kanban, Poka-Yoke, SMED)** = **Improve (VII.B)** | Analyzing/identifying waste = **Analyze**; removing waste with Lean tools = **Improve**! |
| **Design of Experiments (DOE)** | **Improve Phase (VII.A)** | Screening fractional factorials ($2^{k-p}$, Resolution III/IV) and full factorials ($2^k$) live in **Improve** in ASQ BoK. |
| **SPC Control Charts & OCAP** | **Control Phase (VIII.A & VIII.C)** | Control limits are calculated from **process data ($\pm 3\hat{\sigma}$)**, NEVER from customer specification limits! |

---

## 3. Green Belt (GB) -> Black Belt (BB) Refresher Bridge

Since you already passed **ASQ CSSGB** (even if rusty!), here is what we will rebuild cleanly:
1. **GB Topics We Will Refresh Slowly:** DMAIC flow, Charter/VOC/Kano/QFD, Basic Stats & Probability, MSA/Gage R&R, $C_p/C_{pk}$ vs $P_p/P_{pk}$, Fishbone/5 Whys, Basic $t$/$F$/$\chi^2$/ANOVA tests, $2^k$ DOE basics, Lean (5S, Kanban, SMED, Poka-Yoke), and Shewhart SPC charts ($\bar{X}\text{-}R, I\text{-}MR, p, np, c, u$).
2. **BB-Specific Upgrades ASQ Tests Heavily:**
   - Enterprise Deployment, Maturity Models, Business Planning, NPV/IRR, OKRs & KBIs (Domains I–II)
   - Lencioni's 5 Dysfunctions, Coaching GBs, Adult Training Evaluation (Domain III)
   - Non-normal capability (Box-Cox/Weibull), Attribute Agreement Kappa (Domain V)
   - Multiple Regression (VIF, adjusted $R^2$, residuals) & **Non-Parametric Tests** (Mann-Whitney, Wilcoxon, Kruskal-Wallis, Friedman) (Domain VI)
   - **Fractional Factorial DOE ($2^{k-p}$, Resolution III/IV/V, Aliasing/Confounding, Center Points, Blocking, RSM)** + OEE & TOC calculations (Domain VII)
   - **CUSUM, EWMA, Short-Run SPC, Pre-Control** (Domain VIII)
   - **DFSS (DMADV/DMADOV), Taguchi Loss Function $L(y)=k(y-T)^2$, Parameter vs. Tolerance Design, RSS Tolerance Stack-up** (Domain IX)

---

## 4. BBQ Bible Short-Note Template (Used in Every Coaching Turn)

Whenever Qwen or Antigravity teaches a concept or reviews a question, you will get a crisp 3-line **BBQ Bible Note** ready to write down:
- **📍 Phase / ASQ BoK:** `[DMAIC Phase] — [ASQ BoK Code & Title] (Cognitive Level)`
- **🔑 Core Rule / Formula:** *1–2 ultra-short bullet lines (zero fluff)*
- **⚠️ ASQ Exam Trap:** *1 line on how ASQ tricks candidates on this topic*
