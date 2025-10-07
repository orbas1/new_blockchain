# CLI Command Inventory (Expanded)

## Node Operations
- `node init` — bootstrap configuration from genesis manifest.
- `node join` — connect to mainnet/testnet with automatic peer discovery.
- `node upgrade` — orchestrate binary swaps with canary rollout and rollback.
- `node snapshot export/import` — manage state sync artifacts.

## Consensus & Validator Management
- `validator register` — submit staking collateral and metadata.
- `validator delegate` — manage delegation, commission rates, auto-compounding.
- `validator attest` — manual attestation commands for troubleshooting.
- `slashing appeals submit` — file on-chain appeals with supporting evidence.

## Governance
- `gov propose` — scaffold proposals (text, parameter change, software upgrade).
- `gov vote` — sign votes with hardware wallet integration.
- `gov tally` — retrieve live vote breakdown.
- `constitution diff` — compare governance charter revisions.

## Smart Contract Lifecycle
- `contract compile/deploy/call` with deterministic build caching.
- `contract trace` — generate execution traces and gas reports.
- `contract storage` — query state diffs and historical snapshots.

## Observability
- `metrics stream` — pipe Prometheus/OpenTelemetry data.
- `network map` — visualize peer graph and latency heatmap.
- `logs tail` — structured log streaming with filtering DSL.

## Security & Maintenance
- `keys rotate` — threshold key rotation workflow.
- `backup verify` — cryptographically verify backups and restore points.
- `incident report` — submit signed incident tickets to governance.
