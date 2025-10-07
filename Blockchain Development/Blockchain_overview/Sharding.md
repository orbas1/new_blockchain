# Sharding

## Goals
- Partition blockchain state and transaction processing across multiple shards to scale throughput.

## Architectures
- **Execution Sharding**: Different shards execute transactions with cross-shard messaging (Eth2 vision).
- **Data Availability Sharding**: Shards provide data sampling security (Danksharding, Proto-Danksharding).
- **Network Sharding**: Separate gossip layers for shards with cross-link committees.

## Key Components
- Beacon chain coordinating shard committees.
- Cross-shard communication protocols (asynchronous message queues, receipts).
- Collation builders and proposer-builder separation for MEV mitigation.

## Challenges
- Ensuring atomic composability across shards (use asynchronous bridging or rollup overlays).
- Load balancing and hotspot mitigation.
- Validator assignment randomness and unbiasable sampling.
- Handling shard reconfiguration and data availability attacks.

## Research Directions
- Use of zero-knowledge proofs for cross-shard validation.
- Adaptive sharding where shard count expands/shrinks based on demand.
- Integration with rollup-centric roadmap for modular scalability.
