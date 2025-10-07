# Algorithms Overviews

This chapter catalogs the core algorithms employed across the blockchain stack and explains their roles, complexity, and implementation considerations.

## Consensus Algorithms
- **HotStuff Variant**: provides linear communication complexity for leader-driven BFT consensus; optimized with pipelining and threshold signatures.
- **Verifiable Delay Function (VDF)**: based on Wesolowski proof for unpredictable leader election; ensures fairness under partial synchrony.
- **Committee Selection VRF**: cryptographic lottery using stake-weighted randomness to select voting committees per round.

## Networking Algorithms
- **Kademlia DHT**: logarithmic-time peer lookup supporting scalable discovery across thousands of nodes.
- **GossipSub**: adaptive gossip protocol optimizing message propagation through mesh maintenance and score-based peer selection.
- **Reed-Solomon Coding**: erasure coding algorithm for block data resilience, enabling reconstruction with partial data.

## Cryptographic Primitives
- **BLS Signatures**: aggregatable signatures reducing communication overhead; implemented with pairing-friendly curves (BLS12-381).
- **Poseidon Hash**: SNARK-friendly hash function used for Merkle commitments and zero-knowledge circuits.
- **zk-SNARK Provers**: Groth16 for low-latency proofs and Plonk for universal setup rollup circuits.

## Execution & State Algorithms
- **Merkle-Patricia Trie**: hybrid trie enabling efficient state proof generation; optimized via path compression.
- **Gas Pricing Algorithm**: EIP-1559-inspired base fee adjustment with multi-resource vector and congestion feedback.
- **State Sync Protocol**: snapshot-based sync using range proofs and bloom-filtered chunk requests.

## Analytics & Monitoring Algorithms
- **Anomaly Detection**: isolation forests and temporal convolutional networks (TCNs) for detecting irregular telemetry patterns.
- **Validator Scoring**: weighted multi-criteria decision algorithm evaluating uptime, latency, governance participation, and security posture.
- **MEV Detection**: subgraph pattern matching to identify sandwich attacks, front-running, and back-running strategies.

These algorithms interlock to deliver a secure, efficient, and observable blockchain platform, with each algorithm selected for its proven robustness and suitability for institutional-grade deployments.
