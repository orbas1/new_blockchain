# Finalization Time Analysis

## Target KPIs
- Mean time to finality (MTF) under normal conditions: ≤ 12 seconds.
- Tail latency (p95, p99) tracked for stress scenarios.

## Influencing Factors
- Network latency and gossip efficiency.
- Validator participation rate and timeout configuration.
- Block size and execution time.
- Fork-choice rules and view synchronization.

## Measurement Strategy
- Instrument nodes to log propose, pre-vote, pre-commit timestamps.
- Correlate with telemetry dashboards (Prometheus/Grafana).
- Simulate adversarial scenarios (network partitions, offline validators) in testnet.

## Optimization Roadmap
- Adaptive timeouts responsive to observed network delay.
- Aggregated BLS signatures to reduce message size.
- Employ pipelined consensus (HotStuff) to overlap rounds.
