# sci-economic — Sovereign Epistemic Knowledge Corpus (`v1.0.0`)

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](VERSION)
[![ZeroCloudGravity](https://img.shields.io/badge/ZeroCloudGravity-v1.2.0-0F766E.svg)](https://github.com/mtwuser/zero-cloud-gravity)
[![Epistemic Grade](https://img.shields.io/badge/epistemic_grade-E2-1D4ED8.svg)](docs/architecture/01_portfolio_risk_kelly_and_rebalance_laws.md)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

> **Quantitative Economics, Portfolio Risk, Fractional Kelly Sizing & Cashflow Invariants** (`layer_role: knowledge`, `precedence: 20`, `stewardship_stage: public-community`).

## 1. Epistemic Corpus Index (`1:1:1` Progressive Disclosure)

All sections expose deterministic `rcap1` (`L0 -> L3`) capsules and cryptographic `citation_receipt` anchors (`<layer>::<file>#<slug>@<sha256_16>:<E3..E0>`):

| Tier | Credibility | Document |
| :--- | :--- | :--- |
| **Spec / Law** | `E2` | [`docs/architecture/01_portfolio_risk_kelly_and_rebalance_laws.md`](docs/architecture/01_portfolio_risk_kelly_and_rebalance_laws.md) |

## 2. Mounting & Querying from Any `ZeroCloudGravity` Node

Link or mount this corpus into a personal (`<persona>-profile`, `<persona>-wallet`), research, or enterprise node without cloud dependencies:

```bash
zcg link <your-node-dir> --target https://github.com/mtwuser/sci-economic.git --relation knowledge-feed
zcg consult-layer <your-node-dir> --layer sci-economic --query "<topic>" --tier flash
```

## 3. Layer Setup Blueprint (`State U2: configured`)

- **Node ID & Role**: `sci-economic` (`knowledge`, `precedence: 20`, `surface_veracity_mode: full-open-source`)
- **1-Hop Upstream Engine**: [`mtwuser/zero-cloud-gravity`](https://github.com/mtwuser/zero-cloud-gravity)
- **Active Template Packs**: `science-base`, `scientific-methodology`, `sci-economic`, `knowledge-stewardship-portal`
- **Mission, Scope & Core Invariants**: Quantitative economics & portfolio risk corpus (`E2`) governing double-entry accounting invariants, fractional Kelly sizing, drawdown cut-points, and cashflow bucket partitions.
- **Downstream Topology**: Consumed read-only via `knowledge-feed` links or `layers/*` subtrees across personal `wallet`, corporate `finance-supply`, and academic nodes.
- **Authorized Layer Steward**: `sci-economic Knowledge Steward <mtwuser@users.noreply.github.com>`
