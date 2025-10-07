# Sharding Roadmap

## 1. Goals
Partition network responsibilities to achieve horizontal scalability while maintaining security via cryptographic sampling and robust cross-shard communication.

## 2. Shard Types
- **State sharding:** Partition global state, requiring cross-shard contract calls.
- **Transaction sharding:** Route transactions to shards without splitting state (useful for payments).
- **Data availability sharding:** Provide scalable data blobs for rollups (Danksharding).

## 3. Architecture
1. **Beacon/Coordinator chain:** Manages validator assignments, randomness, and cross-shard finality.
2. **Shard chains:** Execute transactions, maintain local state, produce shard blocks.
3. **Cross-shard messaging:** Employ asynchronous message queues or synchronous commits with receipts.
4. **Execution environments:** Could be homogeneous (identical VM) or heterogeneous (custom logic per shard).

## 4. Validator Workflow
- Random sampling with VRFs to resist adaptive corruption.
- Committee attestation aggregation using BLS to reduce bandwidth.
- Slashing for availability faults (missing attestations) and invalid block production.

## 5. Challenges & Mitigations
- **Cross-shard atomicity:** Use two-phase commit, optimistic concurrency, or rollup-style receipts.
- **Data availability:** Implement erasure-coded data and light-client sampling.
- **Complexity:** Provide developer tooling that abstracts shard topology and cross-shard messaging libraries.

## 6. Research Directions
- Executable formal models for cross-shard smart contracts.
- Prover markets for validity proofs ensuring shard correctness.
- Adaptive sharding where shard count adjusts to demand using on-chain auctions.
