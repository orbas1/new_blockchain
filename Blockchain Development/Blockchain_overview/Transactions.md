# Transaction Lifecycle

## Phases
1. Creation by user or smart contract.
2. Signing with private key or delegated authority.
3. Submission to mempool via RPC or gossip.
4. Prioritization by fee market and inclusion into block.
5. Execution in VM, state transition recorded.
6. Finalization and archival.

## Transaction Types
- Simple transfers.
- Contract deployment and calls.
- Batch transactions and meta-transactions.
- Cross-chain messages and rollup proofs.

## Mempool Design
- Priority queue by effective gas price.
- Spam prevention via base fee and minimum gas price.
- Privacy enhancements (encrypted mempools, private orderflow).

## Observability
- APIs for pending transactions, confirmation tracking.
- Alerts for stuck transactions and gas spikes.
