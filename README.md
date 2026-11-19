# sci-economic (`knowledge`, `precedence: 20`)

## Layer Setup Blueprint (Epistemic Knowledge Atlas Node (gov-*, sci-*, geo-*, org-*))

- **Node ID & Role**: `sci-economic` (`knowledge`, `precedence: 20`)
- **1-Hop Upstream Parent**: `mtwuser/zero-cloud-gravity`
- **Active Template Packs**: `science-base`, `scientific-methodology`, `knowledge-stewardship-portal`, `sci-economic`
- **Branch & Promotion Pipeline (`promotion_pipeline`)**: `staged` (`['dev', 'tst', 'pre', 'pro']` — `master` = enacted `pro` baseline + optional `context_branches` (`specialty/*`, `hat/*`, `machine/*`); work promotes via `feature/*` or `directive/*` (`dev`) -> `env/tst` -> `env/pre` -> `master` (`pro`))
- **Human-Stack Profile (Optional)**: [Optional: leave blank for default, or compose Human-Stack facets: domain-<area>:M1..M4 | bridge-* | soft-* | hat-*]
- **Interaction Language (`--lang`)**: `es` (`Spanish (es)` — repo artifacts 100% English)
- **Mission, Scope & Core Invariants**: [Fill: Epistemic domain, E3..E0 credibility invariants, and citation_receipt scope]
- **Downstream Topology (Next Tier)**: [Fill: Consumer nodes mounting this knowledge corpus]
- **Authorized Layer Owner (`set-authority`)**: [Fill: Role title & owner email]

## Initial Chat Kickoff Prompt (4-Phase Customizable Progression)

```text
/sopen — Configure Zero-Cloud Node 'sci-economic' (Epistemic Knowledge Atlas Node (gov-*, sci-*, geo-*, org-*), lang=es):
- Mission & Scope: [Customize: [Fill: Epistemic domain, E3..E0 credibility invariants, and citation_receipt scope]]
- Authorized Owner: [Customize: Role title & owner@domain]
Phase A (Setup & Purpose Alignment): Write the Mission & Authorized Owner above into README.md (replacing all [Fill: ...] placeholders) and system/zcg-node.json (zcg set-authority). Tailor templates/sci-economic/rules/sci-economic.md with our mission and invariants without duplicating upstream rules, then run make sync && make diff and initialize WORKROAD.md / WORKTASK.md.
Phase B (Epistemic Knowledge & Spec Atlas): Structure docs/{reference,architecture,guides}/ (< 465 lines) with E3..E0 epistemic grades and citation_receipt anchors.
Phase C (Daily Bounded-Lot Execution & Verification): Claim work via make task TASK="<id>", execute 1 bounded lot per turn (3-5 files) with active-layer verification, and checkpoint via /continue.
Phase D (Upward Enrichment & Sync Reconciliation): Reconcile upstream updates via make sync STRATEGY=reconcile (make upstream-diff), verify make env-gate ENV=tst|pre|pro, and promote reusable rules upward via /enrich and make promote before /sclose. Finally, mark '- [x] Complete `Layer Setup Blueprint`' in WORKTASK.md and run make activate-plugin to unlock the configured Node Workspace web UI.
```

## Upstream Upgrade & Version Reconciliation Prompt (4-Step Guided Flow)

```text
Step 1 (Topology & Horizon Audit): /sopen — Run make status (inspect sync_topology 4-stage DAG & promotion_pipeline), make horizon, and make upstream-diff against `mtwuser/zero-cloud-gravity`.
Step 2 (Zero-Loss Node & Schema Reconciliation): Run make sync STRATEGY=reconcile (or STRATEGY=merge) to upgrade Makefile, system/zcg-node.json, and inherited templates while preserving sovereign rules in templates/sci-economic/rules/sci-economic.md.
Step 3 (Selective Stack & Node Plugin Review): Evaluate whether any newly available context-stack, tool-stack, or plugin-stack pack adds genuine value without saturating context, then verify make diff (0 drift).
Step 4 (Environment / Mastery Gate & Closure): Validate make env-gate ENV=pro (or ENV=tst|pre|pro on staged enterprise nodes) and close via /sclose.
```
