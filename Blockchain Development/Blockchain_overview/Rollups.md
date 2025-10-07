# Rollups Overview

## Definition
Rollups execute transactions off-chain while posting succinct proofs and data commitments on the base layer to inherit security.

## Types
- **Optimistic Rollups**: Assume validity; challenge mechanism with fraud proofs (e.g., Arbitrum, Optimism).
- **ZK-Rollups**: Publish zero-knowledge validity proofs (Groth16, PLONK, STARK) ensuring correctness without challenges.
- **Sovereign Rollups**: Use base layer purely for data availability; consensus and settlement handled by rollup governance.

## Design Considerations
- Data availability strategy (on-chain calldata vs. external DA layers like Celestia).
- Sequencer decentralization: single operator, rotating committee, or permissionless auction.
- Bridging architecture: message passing, finality windows, exit proofs.
- Upgradability: multi-signature vs. on-chain governance with timelocks.

## Performance Metrics
- Transactions per second off-chain vs. posting frequency.
- Proof generation latency and cost.
- Capital efficiency of bridges (liquidity providers, exit delays).

## Risk Management
- Sequencer misbehavior and censorship resistance.
- Fraud proof window design to prevent griefing.
- Circuit complexity for ZK proofs and trusted setup requirements.
- Dependency on L1 congestion and gas pricing.

## Roadmap
- Explore shared sequencer networks for interoperability.
- Implement cross-rollup composability via atomic swaps and message relayers.
- Integrate MEV mitigation (PBS, encrypted mempools) within rollup architecture.
