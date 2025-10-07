# Storage Architecture (Doctoral Expansion)

## 1. Multi-Tier Design
- **Hot storage:** SSD-backed databases (RocksDB, TiKV) for active state.
- **Warm storage:** Object stores (S3-compatible) for recent history.
- **Cold archival:** Tape, glacier storage, or decentralized storage (Arweave, Filecoin) for compliance retention.

## 2. Data Layout
- Columnar encoding for analytics.
- Versioned key-value stores with snapshot isolation.
- Content-addressable chunking with deduplication.

## 3. Reliability & Durability
- 3-2-1 backup strategy with geographic dispersion.
- Regular integrity checks (Merkle proofs, checksums).
- Disaster recovery drills with restore time objectives (RTO/RPO).

## 4. Performance Tuning
- Prefetch caches for trie nodes.
- Write-ahead logging and batching.
- Compression/compaction schedules aligned with consensus cadence.

## 5. Research Agenda
- Verifiable storage outsourcing with proofs-of-retrievability.
- Differential privacy for data analytics exports.
- Green storage metrics incorporating energy per byte.
