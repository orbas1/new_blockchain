# Sidechains

## Purpose
- Extend functionality and throughput by running independent chains pegged to the main network.
- Enable domain-specific optimization (privacy, compliance zones, specialized VM).

## Peg Mechanisms
- **Two-Way Peg**: Lock assets on main chain, mint representation on sidechain via federated or smart contract bridges.
- **Liquidity Providers**: Fast exits via bonded intermediaries.
- **Native Interop Protocols**: IBC-style light client verification across chains.

## Security Models
- Federated signers (Liquid), proof-of-authority validators, or independent proof-of-stake sets.
- Economic guarantees vary; require monitoring of collateralization and signer honesty.

## Operational Considerations
- Finality synchronization and withdrawal periods.
- Cross-chain slashing for validator misconduct.
- Upgrade pathways and fallback to main chain in event of catastrophic failure.

## Use Cases
- Compliance chains with KYC gating.
- High-frequency trading sidechains with deterministic finality.
- Confidential transaction zones using zero-knowledge proofs.
