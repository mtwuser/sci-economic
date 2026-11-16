---
epistemic_grade: E2
---

# Quantitative Portfolio Risk, Fractional Kelly Growth & Cashflow Partition Laws (`sci-economic`)

> *"Capital allocation policies shall bound geometric drawdown via fractional Kelly sizing and positive-semidefinite covariance constraints, partition gross inflows deterministically before discretionary deployment, and evaluate drift strictly in dimensionless Base-100 / % weights."*

This specification formalizes the mathematical portfolio, risk, and treasury invariants consumed by `sovereign-wallet-cockpit` and quantitative strategy nodes (`ECON-PORT-01..04`).

---

## 1. Normalized Simplex Weights, Covariance Risk & Rebalance Drift (`ECON-PORT-01` — `E2`)

 Portfolio positions are represented on the dimensionless probability simplex $\mathbf{w} \in \Delta^{n-1}$ ($\sum_{i=1}^n w_i = 1,\ w_i \ge 0$), enabling `Base-100 / %` analysis without disclosing nominal currency balances:

$$\sigma_p^2 = \mathbf{w}^\top \Sigma \mathbf{w} \ge 0, \qquad \text{MDD}(T) = \max_{0 \le \tau \le t \le T} \frac{V(\tau) - V(t)}{V(\tau)} \in [0, 1)$$

| Quantitative Law | Mathematical Formulation | Mandatory Cut-Point & Guard |
| :--- | :--- | :--- |
| **Simplex & `Base-100` Invariance** | $w_i = V_i / \sum_{j=1}^n V_j$, drift $\delta_i = w_i - w_i^\star$ (`bps`). | Trigger rebalance review only when $|\delta_i| > \tau_{\text{band}}$ (avoiding fee churn inside tolerance band). |
| **Fractional Kelly Criterion** | Full Kelly $f^\star = \Sigma^{-1}\boldsymbol{\mu}$; operational sizing $f = \kappa f^\star$ with $0 < \kappa \le 0.5$ (*Half-Kelly ceiling*). | Reject $\kappa > 1.0$ (`OVER_KELLY_RUIN_REGIME`, where geometric growth rate turns negative under estimation error). |
| **Cashflow Bucket Partition** | $C_{\text{in}} = B_{\text{profit}} + B_{\text{tax}} + B_{\text{payout}} + B_{\text{opex}}$ with $\sum b_k = 100\%$. | Statutory tax reserve $B_{\text{tax}}$ is segregated *prior* to net OpEx or venture allocation. |
| **4-Ring Thesis Exposure Drift** | $\mathbf{w}_{\text{thesis}} = (w_{\text{index}}, w_{\text{stack}}, w_{\text{supply}}, w_{\text{cons}})$ vs. target $\mathbf{w}_{\text{thesis}}^\star$. | Enforce $L_1$ drift $\frac{1}{2}\sum_r |w_r - w_r^\star| \in [0, 1]$ with `0` leverage-induced negative reserve cash. |
