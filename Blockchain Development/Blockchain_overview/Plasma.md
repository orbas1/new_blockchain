# Plasma Architecture

## 1. Concept
Plasma chains offload transactions to child chains secured by periodic commitments to the root chain.

## 2. Components
- **Operator:** Aggregates transactions, produces Plasma blocks, submits commitments.
- **Exit mechanism:** Enables users to withdraw funds with fraud proofs and challenge periods.
- **Fraud proofs:** Verify invalid exits or double-spends using Merkle proofs.

## 3. Security Considerations
- Mass exit scenarios and exit throttling.
- Data availability challenges and operator censorship.
- Watchtower services monitoring commitments and initiating challenges.

## 4. Research Agenda
- Plasma with validity proofs to reduce exit latency.
- Hybrid Plasma-rollup architectures.
- User experience improvements for exit management.
