# Peer Topology

## Peer Discovery
- Bootnodes with static addresses.
- mDNS and DNS-based discovery for local/regional peers.
- Peer exchange protocols (gossip-based sampling).

## Connection Management
- Maintain target peer count with inbound/outbound balance.
- Reputation scoring to avoid eclipse attacks.
- Encryption via TLS/Noise protocol for privacy and integrity.

## Monitoring
- Track peer churn, latency, bandwidth usage.
- Detect anomalous behavior (spam, invalid blocks, fork attempts).
- Provide dashboards for network operations center.
