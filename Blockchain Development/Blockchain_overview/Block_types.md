# Block Typology

## 1. Classification
- **Execution blocks:** Carry transactions and state transitions.
- **Attestation blocks:** Contain votes attestations (e.g., Ethereum Beacon chain).
- **Checkpoint blocks:** Mark governance-approved milestones or emergency restarts.
- **Empty blocks:** Produced under congestion or when proposer is offline; must be monitored for abuse.
- **MEV bundles:** Auxiliary blocks containing ordered transactions for builder markets.

## 2. Metadata Standards
- Field definitions for gas metrics, proposer identity, randomness seeds.
- Extensions for rollup payloads, cross-chain messages, and embedded proofs.

## 3. Governance Hooks
- Policy for empty block frequency, slashing thresholds, and reward adjustments.
- Specialized block types (e.g., upgrade activation blocks) requiring DAO approval.

## 4. Research Agenda
- Dynamic block classification using machine learning for anomaly detection.
- Formal grammars for block metadata enabling composability across chains.
