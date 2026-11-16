---
trigger: always_on
description: "Quantitative economics, portfolio risk, and dimensionless Base-100 rules for sci-economic (E2)."
---

# `sci-economic` Quantitative Economics & Risk Corpus Rules (`E2`)

> Governed by `system/zcg-node.json` (`layer_id: sci-economic`, `stewardship_stage: public-community`).

## Normative Invariants (`ECON-SCI-01..03`)
1. **Dimensionless Simplex & `Base-100` Rigor**: Express portfolio weights on $\Delta^{n-1}$ ($\sum w_i = 1$) and drift in `bps` so mathematical risk proofs remain independent of private nominal balances.
2. **Fractional Kelly & Drawdown Cut-Points**: Enforce $0 < \kappa \le 0.5$ (*Half-Kelly ceiling*) and positive-semidefinite covariance $\Sigma \succeq 0$ (`OVER_KELLY_RUIN_REGIME` rejected).
3. **Pre-OpEx Tax Reserve Segregation**: Partition gross inflows ($B_{\text{profit}} + B_{\text{tax}} + B_{\text{payout}} + B_{\text{opex}} = 100\%$) before discretionary capital deployment.
