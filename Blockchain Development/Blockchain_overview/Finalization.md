# Finalization Framework

## 1. Definition
Finalization denotes the point at which a block becomes irreversible under defined adversary assumptions.

## 2. Types
- **Deterministic finality:** BFT protocols provide explicit commit certificates.
- **Economic finality:** Probabilistic assurance via cost of reorg (Nakamoto).
- **Hybrid:** Chain finality plus explicit checkpoints (Casper, GRANDPA).

## 3. Metrics
- Time-to-finality distribution, measured at p50/p95.
- Reorg depth statistics and stale block rates.
- Finality reversion risk under observed network health.

## 4. Operational Policies
- Finality thresholds for exchanges, bridges, and dApps.
- Alerting on delayed finality or excessive view changes.
- Governance-defined emergency finalization overrides.

## 5. Research Agenda
- Asynchronous finality gadgets resilient to adaptive adversaries.
- Verifiable delay functions for unbiased finality timers.
- Machine-learned predictors of finality stalls for proactive mitigation.
