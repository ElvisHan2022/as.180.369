## 3. Methodology

### 3.1 Data and Variables
Hospital-level data will be merged from the CMS HRRP Supplemental Files, the FY2019 NPRM DRG weight tables, and the Hospital Compare datasets. Key variables include:
- **Excess Readmission Ratio (ERR)** — dependent variable measuring risk-adjusted readmission performance.
- **Dual Proportion** — share of dual-eligible Medicare–Medicaid patients, proxying for social risk.
- **DRG Weight** — proxy for case severity and reimbursement intensity.
- **Peer Group Median ERR** — contextual benchmark controlling for condition-specific clustering.
- **Observation Substitution Index (OSI)** — constructed ratio of observation to readmission discharges, capturing behavioral adaptation.

### 3.2 Empirical Specification
The baseline model regresses ERR on social and structural factors:
\[
ERR_{it} = \beta_0 + \beta_1 Dual_{it} + \beta_2 DRGWeight_{it} + \beta_3 PeerMedian_{it} + \epsilon_{it}
\]

A **Difference-in-Differences (DiD)** extension will exploit time variation in penalty thresholds across fiscal years and conditions:
\[
ERR_{it} = \alpha + \delta_1 Post_t + \delta_2 Treated_i + \delta_3 (Post_t \times Treated_i) + X_{it}\gamma + \epsilon_{it}
\]
where \( Treated_i \) identifies hospitals facing penalty escalation after FY2017 adjustments.

### 3.3 Proposed Analysis
1. **Descriptive exploration:** visualize ERR, DRG weight, and dual-proportion distributions by peer group and region.
2. **Regression diagnostics:** compare OLS, fixed-effects, and negative binomial specifications.
3. **Observation behavior:** calculate OSI and correlate with penalty magnitude and DRG case mix.
4. **Robustness checks:** exclude top/bottom deciles by case volume and perform placebo DiD for non-penalized conditions.

### 3.4 Next Steps
Subsequent work will incorporate cost data to connect HRRP penalties with reimbursement outcomes, test potential welfare implications, and explore whether policy adjustments (e.g., refined social-risk adjustment) could improve program equity and efficiency.
