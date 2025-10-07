# Block Structure

## Components
- Header: parent hash, state root, transaction root, receipt root, timestamp, difficulty/validator info.
- Body: ordered list of transactions, uncle/ommer references, metadata (e.g., attestations).
- Signatures: proposer signatures, aggregate BLS signatures for votes.

## Validation Steps
1. Verify header fields and consensus-specific requirements.
2. Validate proposer identity and signatures.
3. Execute transactions in order, updating state transitions.
4. Confirm resulting state root matches header commitment.

## Optimization Considerations
- Include metadata for MEV transparency (bundle commitments, fee recipients).
- Support variable block sizes with gas limits tuned to hardware capabilities.
- Provide additional channels for blob data (EIP-4844 style) to separate execution and DA.
