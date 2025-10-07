# Rollups Strategy (Doctoral Expansion)

## 1. Taxonomy
- **Optimistic rollups:** Fraud proofs with challenge windows (Arbitrum, Optimism).
- **ZK-rollups:** Validity proofs (Groth16, Plonk, STARKs) ensuring immediate finality.
- **Sovereign rollups:** Manage own execution environment while inheriting data availability from L1.
- **Application-specific rollups:** Tailored constraints for gaming, payments, identity.

## 2. Architecture Components
1. **Sequencer layer:** Ordered batching, MEV neutralization, and cross-domain message routing.
2. **Prover system:** High-performance proof generation pipeline with GPU/ASIC acceleration and distributed prover markets.
3. **Bridge contracts:** Enforce verification logic, manage deposits/withdrawals, and expose governance hooks.
4. **Data availability:** On-chain calldata, blob space (EIP-4844), or external DA committees with KZG commitments.

## 3. Design Considerations
- **Security inheritance:** Formalize assumptions about L1 finality, censorship, and reorg handling.
- **Interoperability:** Shared bridge standards, message relayers, and canonical token mapping.
- **Economic model:** Fee allocation between L1, sequencers, and prover markets.
- **User experience:** Fast exits, bridging UX, and transparent status dashboards.

## 4. Operational Playbooks
- Sequencer decentralization roadmap: multi-operator, fault-tolerant consensus, fallback to L1 rollup contract.
- Proof generation SLAs with penalized delays and redundant prover networks.
- Incident response for invalid state roots, leveraging optimistic fraud proofs or emergency shutdown.

## 5. Research Directions
- Recursive proof composition for mass batching.
- Shared sequencing/ordering between multiple rollups (SUAVE, Espresso).
- Integration with privacy-preserving rollups (Aztec-style encrypted state).
- Tokenomic models for incentivizing data availability committees.
