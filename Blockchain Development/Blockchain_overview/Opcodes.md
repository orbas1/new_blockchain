# Opcode Catalog

## Classification
- **Arithmetic & Logic**: ADD, SUB, MUL, DIV, MOD, bitwise operations.
- **Cryptographic**: HASH, KECCAK, BLAKE3, ECADD, ECPAIRING.
- **Control Flow**: JUMP, JUMPI, CALL, RETURN, REVERT.
- **Storage & Memory**: SLOAD, SSTORE, MLOAD, MSTORE.
- **Environment**: TIMESTAMP, BLOCKHASH, CALLER, ORIGIN.
- **System**: CREATE, CREATE2, SELFDESTRUCT (with deprecation policy), LOG opcodes.

## Versioning
- Maintain opcode tables per VM revision with deprecation timelines.
- Introduce feature flags for experimental opcodes gated by governance votes.

## Gas Schedule Considerations
- Benchmark cost on representative hardware.
- Adjust for precompile alternatives to prevent underpricing.
- Document DoS risk analysis for each opcode.

## Tooling
- Reference assembler/disassembler.
- Static analysis tools for opcode usage frequency and complexity.
