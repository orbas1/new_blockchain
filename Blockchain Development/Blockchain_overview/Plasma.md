# Plasma Framework

## Concept
- Hierarchical chain structure where child chains commit Merkle roots to root chain.

## Mechanics
- Operators aggregate transactions, submit commitments, and provide fraud proofs when challenged.
- Users exit by presenting inclusion proofs and waiting through challenge period.

## Variants
- Plasma Cash for non-fungible coins.
- Plasma Debit enabling shared slots and micropayments.
- Plasma Prime integrating zero-knowledge proofs.

## Limitations
- Data availability reliance on operators.
- Complex exit games leading to UX friction.
- Incompatible with general smart contract execution without extensions.

## Future Work
- Combine with rollup data availability to reduce exit complexity.
- Improve mass exit handling via liquidity providers and insurance pools.
