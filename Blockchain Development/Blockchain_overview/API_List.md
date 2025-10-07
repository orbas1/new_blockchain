# API Endpoint Catalogue

## Consensus & Node Health
- `/health` — Node diagnostics.
- `/consensus/status` — Current epoch, view, validator set.
- `/metrics` — Prometheus-formatted metrics.

## Ledger & State
- `/block/{height}` — Block details with proofs.
- `/state/{address}` — Account/state query with Merkle proof.
- `/transactions/pending` — Mempool snapshot.

## Governance
- `/governance/proposals` — Proposal list, status, metadata.
- `/governance/votes` — Vote breakdown by delegations.

## Ecosystem
- `/tokens/{id}` — Token metadata, supply, holders.
- `/nfts/{collection}` — NFT attributes and provenance.
- `/marketplace/orders` — Order book snapshots.

## Tooling
- `/telemetry/stream` — Websocket telemetry.
- `/analytics/reports` — Generated insights, risk reports.
