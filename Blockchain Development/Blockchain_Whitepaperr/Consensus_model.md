# Consensus Model

The consensus mechanism adopts a hybrid Byzantine fault-tolerant architecture combining leader-based HotStuff rounds with verifiable delay function (VDF) randomness and stake-weighted committee selection. This design ensures fast finality, equitable proposer selection, and resilience against adaptive adversaries.

## Protocol Overview
- **Leader Election**: VDF output seeds a verifiable random function (VRF) lottery that selects proposers and voting committees per round.
- **Proposal Phase**: elected leader constructs a block from prioritized mempool transactions, attaching zero-knowledge compliance attestations.
- **Voting Phase**: committee members validate block integrity, execute pre-state checks, and sign using BLS threshold signatures.
- **Commit Phase**: aggregated signatures exceeding 2/3 stake weight finalize the block; fallback rounds trigger if quorum not reached within latency bounds.

## Safety & Liveness Guarantees
- **Safety**: quorum intersection ensures no two conflicting blocks achieve finality. Formal proofs follow TLA+ specifications validated through model checking.
- **Liveness**: partial synchrony assumption with adaptive timeouts; VDF randomness prevents predictable leader targeting.
- **Accountability**: slashable offenses (double-sign, invalid attestations, censorship) logged on-chain with appeal procedures.

## Performance Characteristics
- **Throughput**: pipeline processing allows simultaneous proposal preparation and vote aggregation, achieving 5,000+ TPS under benchmarked workloads.
- **Finality**: two-round finality with aggregated BLS signatures delivers sub-6-second confirmations.
- **Scalability**: sharded committees and rollup attestations offload state execution while preserving security via shared finality checkpoints.

## Security Enhancements
- **Committee Diversity**: selection constraints enforce geographic and jurisdictional diversity to mitigate correlated failures.
- **Adaptive Weighting**: stake caps, reputation modifiers, and activity scores prevent excessive centralization.
- **Disaster Recovery**: protocol supports emergency council overrides requiring multi-signature approval to pause or reconfigure parameters during catastrophic events.

## Upgrade Path
- **Formal Verification**: consensus code annotated with formal semantics; upgrades undergo Coq proof obligations.
- **Testnets**: multi-stage release across devnet, testnet, and canary networks with telemetry thresholds gating progression.
- **On-chain Governance**: parameter adjustments (timeout, committee size) executed through governance proposals with automated rollout scripts.

The consensus model fuses academic robustness with operational pragmatism, ensuring the network maintains integrity, availability, and equitable participation across diverse market conditions.
