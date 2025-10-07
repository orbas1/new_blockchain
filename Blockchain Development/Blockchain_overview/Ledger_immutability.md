# Ledger Immutability

## Guarantees
- Achieved through cryptographic linkage of blocks (hash pointers) and consensus finality rules.
- Economic deterrence: slashing, energy costs, time-locked bonds discourage reorgs.
- Legal reinforcement: governance charters codify limits on rollback decisions.

## Threats to Immutability
- Majority attacks (51% hashpower or stake).
- Coordinated social consensus forks responding to critical bugs.
- Quantum adversaries breaking signature schemes.
- Long-range attacks exploiting weak checkpointing.

## Mitigations
- Frequent finality checkpoints anchored to external ledgers (Bitcoin, Ethereum).
- Diverse validator sets with geographic, jurisdictional spread.
- Quantum-safe cryptography roadmap (lattice-based signatures, hash-based signatures).
- Transparent incident response policy with rollback thresholds and stakeholder voting.

## Monitoring & Auditing
- Reorg depth dashboards and alerting on unusual fork rates.
- Immutable audit logs stored off-chain (WORM storage) for compliance.
- Third-party notarization via timestamping services.
