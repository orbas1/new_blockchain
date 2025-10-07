# Virtual Machine Types Catalog (Advanced Enumeration)

## Abstract
This catalog enumerates virtual machine (VM) paradigms relevant to blockchain execution environments, summarizing properties, strengths, and use cases.

| VM Type | Execution Model | Determinism | Strengths | Considerations |
|---------|-----------------|-------------|-----------|----------------|
| Ethereum Virtual Machine (EVM) | Stack-based, 256-bit words | Deterministic | Mature tooling, broad ecosystem, Solidity compatibility | Limited instruction set, gas inefficiencies, lacks formal semantics. |
| WebAssembly (WASM) VM | Stack-based, linear memory | Deterministic with restrictions | Multi-language support, fast performance, sandboxing | Requires determinism guards (no floating point nondeterminism). |
| MoveVM | Resource-oriented, register-based | Deterministic | Strong asset safety via linear types, formal verification friendly | Smaller ecosystem, specialized language. |
| eBPF-based VM | Register-based | Deterministic (with constraints) | High performance, direct syscalls, mature tooling from kernel space | Requires stringent sandboxing to prevent host compromise. |
| zkVM (e.g., Risc0, zkSync VM) | Arithmetic circuit execution | Deterministic | Generates zero-knowledge proofs of execution, ideal for zk-rollups | High prover costs, complex tooling. |
| LLVM IR JIT VM | SSA-based intermediate | Requires determinization | Rich optimization pipeline, language flexibility | Hard to guarantee determinism without heavy constraints. |
| Custom DSL VM | Domain-specific instructions | Deterministic by design | Tailored for protocol needs, potentially minimal footprint | Requires bespoke tooling and adoption incentives. |

## Research Directions
- Evaluate hybrid VM stacks enabling fallback from high-level DSL to WASM for compatibility.
- Investigate zk-friendly instruction sets to reduce proving costs.
- Collaborate with academia to formalize semantics for custom VMs using proof assistants.
