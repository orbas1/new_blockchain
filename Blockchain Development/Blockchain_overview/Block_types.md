# Block Types

## Execution Blocks
- Contain full transactions and state transitions.
- Primary vehicle for fee revenue and MEV capture.

## Data Blobs / Availability Blocks
- Carry large calldata for rollups, not directly executed by L1.
- Require sampling-based validation and erasure coding.

## Finality/Checkpoint Blocks
- Aggregated validator signatures establishing irreversible checkpoints.
- Aid light clients and cross-chain bridges.

## Epoch Summary Blocks
- Summaries of validator performance, reward distribution, slash events.
- Feed into governance analytics and compliance reporting.

## Special Blocks
- **Genesis Block**: Bootstraps chain state.
- **Emergency Blocks**: Trigger protocol-level circuit breakers under governance approval.
