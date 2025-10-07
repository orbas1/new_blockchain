# Cross-Chain Interoperability

## 1. Objectives
Enable asset and data mobility across heterogeneous chains with verifiable trust assumptions and automated risk management.

## 2. Components
- **Messaging protocols:** IBC, LayerZero, Axelar — deliver verifiable packets.
- **Bridges:** Lock-and-mint, burn-and-mint, liquidity networks.
- **Relayers:** Off-chain agents submitting proofs, incentivized via fees and slashing bonds.

## 3. Security Considerations
- Formal threat modelling (bridge hacks, replay attacks, relayer collusion).
- Cross-chain rate limits, timeouts, and telemetry for anomaly detection.
- Insurance mechanisms (slashing, collateral, mutualized funds).

## 4. UX & Developer Experience
- Unified APIs and SDKs for bridging and cross-chain contract calls.
- Transaction status tracking, user notifications, and fallback instructions.

## 5. Research Agenda
- ZK-based general message passing.
- Cross-chain MEV mitigation and fair ordering.
- Interoperability with off-chain systems (banking rails, CBDCs).
