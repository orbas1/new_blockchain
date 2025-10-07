# Consensus Model Comparative Matrix (Doctoral-Level Assessment)

## Abstract
This matrix benchmarks candidate consensus models against operational criteria relevant to institutional deployments. Scores are on a 1-5 scale derived from expert analysis and empirical data.

| Model | Safety Guarantees | Liveness under Adversity | Performance (Throughput/Latency) | Implementation Maturity | Regulatory Friendliness | Notes |
|-------|-------------------|--------------------------|----------------------------------|-------------------------|------------------------|-------|
| HotStuff (Optimistic BFT) | 5 | 4 | 4 | 4 | 4 | Strong formal proofs; requires reliable networking for optimal performance. |
| HoneyBadgerBFT | 5 | 5 | 2 | 3 | 3 | Fully asynchronous; higher latency but robust to unpredictable networks. |
| Algorand | 4 | 4 | 4 | 4 | 4 | VRF committees; probabilistic finality negligible failure probability. |
| Ouroboros Praos | 4 | 3 | 3 | 5 | 4 | Well-studied academically; probabilistic finality with slot leaders. |
| Avalanche | 3 | 4 | 5 | 3 | 3 | High throughput; needs careful parameter tuning for safety margins. |
| BABE + GRANDPA | 4 | 4 | 4 | 4 | 4 | Separation of block production and finality enhances flexibility. |
| Nakamoto PoW | 3 | 3 | 2 | 5 | 3 | Proven security but energy intensive; probabilistic finality. |
| Hybrid HotStuff + HoneyBadger | 5 | 5 | 4 | 3 | 4 | Combines optimistic responsiveness with asynchronous fallback; added complexity. |

## Methodology
- Safety and liveness scores derived from formal proofs and peer-reviewed literature.
- Performance scores based on benchmark studies and simulation results.
- Regulatory friendliness assesses auditability, compliance tooling, and energy footprint considerations.
