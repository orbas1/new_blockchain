# Consensus Operational Flows (Graduate-Level Systems Analysis)

## Abstract
This document decomposes the consensus pipeline into formalized phases, annotating each with state transitions, failure domains, and observability markers. Flow diagrams are described textually to support verification and reproducibility.

## 1. Transaction Intake & Pre-Processing
- **Ingress control:** Transactions arrive via gossip; mempool admission applies stateless validation, signature verification, and anti-spam fee heuristics.
- **Ordering hints:** Access lists and intent metadata inform the scheduler about conflict domains; results fed into a weighted fair queuing model.
- **Privacy handling:** Optional threshold encryption encapsulates payloads until consensus commitments are achieved.

## 2. Proposal Construction
1. **Leader selection**
   - VRF output seeded from previous block certificate picks the provisional leader set (primary + backup).
   - Leader fetches highest-scoring transactions using multi-criteria ranking (fee density, age, QoS commitments).
2. **Block assembly**
   - Candidate block comprised of ordered transactions, state root, execution traces, and data availability commitments.
   - Proposer attaches proof-of-availability (erasure-coded chunk commitments) and randomness beacon attestation.

## 3. Voting Phases (HotStuff Fast Path)
- **Prepare phase:** Validators verify block proposal, run dry-run execution checks, and emit signed prepare votes aggregated via BLS.
- **Pre-commit phase:** Upon receiving 2f+1 prepare votes, leader issues pre-commit certificate; validators cross-validate dependencies.
- **Commit phase:** Commit certificate broadcast; validators lock on block and update local state machines.
- **Latency instrumentation:** Each phase annotated with microsecond timestamps exported for probabilistic latency modeling.

## 4. Fallback Invocation (HoneyBadger Module)
- Trigger condition: Timeout_i > μ + kσ, where μ and σ derived from recent latency distribution, k configurable by governance.
- **Batching:** Validators encrypt mempool transactions into batches, exchanging ciphertext via reliable broadcast.
- **Decryption:** After threshold of shares received, batches decrypted and deterministically ordered via hash sortition.
- **Commitment:** Asynchronous agreement finalizes batch; outputs mapped back to block format for execution.

## 5. Finalization & Checkpointing
- **Notarization cadence:** Every κ blocks, validators co-sign checkpoint containing block hash, state root, and cumulative slashing log.
- **Light client support:** Checkpoints inserted into Merkle Mountain Range to enable logarithmic synchronization.
- **Roll-back guarantees:** Safety proof ensures no conflicting checkpoint can be finalized without >1/3 equivocation.

## 6. Fault Handling Flow
- **Leader equivocation:** Evidence propagated, slashing transaction auto-generated, backup leader resumes with locked view number.
- **Network partition:** Dual-committee monitoring compares vote participation; fallback triggered when divergence > δ.
- **Validator recovery:** Stalled validators request state sync via state proofs; trust-on-first-use anchored in last checkpoint.

## 7. Observability & Feedback Loops
- Telemetry service collects per-phase success probabilities, vote latency histograms, and committee health metrics.
- Machine learning agents (reinforcement learning) tune timeout parameters by minimizing cost function combining latency and fork probability.
- Incident retrospectives captured as structured knowledge base feeding simulation parameter updates.
