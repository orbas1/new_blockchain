# Consensus Models Catalog (Advanced Enumeration)

## Abstract
This catalog lists consensus models relevant for modular blockchain design, summarizing key properties and deployment contexts.

| Model | Category | Fault Tolerance | Finality | Communication Complexity | Deployment Notes |
|-------|----------|-----------------|----------|---------------------------|------------------|
| HotStuff | BFT | f < n/3 Byzantine | Deterministic | O(n) with aggregation | Basis for many modern PoS chains; simple pipelining. |
| Tendermint | BFT | f < n/3 | Deterministic | O(n^2) | Mature ecosystem, moderate throughput. |
| HoneyBadgerBFT | Asynchronous BFT | f < n/3 | Deterministic | O(n^2 log n) | Resilient to network delays; higher latency. |
| Algorand | Committee-based PoS | f < n/3 | Probabilistic (low) | O(n) | VRF-based committees, fast finality under synchrony. |
| Ouroboros Praos | Chain-based PoS | < 50% adversarial stake | Probabilistic | O(n) | Strong formal proofs; slot-based leader election. |
| Casper FFG | Finality gadget | f < n/3 | Deterministic overlay | O(n^2) | Adds finality to PoW chains; partial liveness reliance on PoW. |
| Avalanche | Probabilistic consensus | < 80% honest | Probabilistic | O(k) sampling | High throughput; metastability properties. |
| BABE + GRANDPA | Hybrid | f < n/3 | Deterministic finality + probabilistic block production | O(n) | Separation of production and finality phases. |
| Proof-of-Elapsed-Time | Trusted hardware | Crash faults (TEE reliant) | Deterministic | O(n) | Depends on TEEs; suitable for permissioned networks. |
| Nakamoto (PoW) | Longest-chain | < 50% hashpower | Probabilistic | O(n) | Battle-tested security; energy intensive. |

## Research Considerations
- Evaluate composability of multiple models via consensus switching frameworks.
- Investigate security under adaptive adversaries and network partitions.
- Quantify cost-benefit trade-offs for hybridizing deterministic and probabilistic mechanisms.
