# 18 — Testing and verification

**Status:** Planned

## Verification levels

1. Arithmetic helper unit tests.
2. Register-state and reset tests.
3. Decoder positive and negative tests.
4. Per-instruction semantic tests.
5. Memory translation and permission tests.
6. Trap and privilege tests.
7. Assembler/disassembler round trips.
8. ABI conformance programs.
9. Kernel boot integration tests.
10. Deterministic replay and differential testing.

## Wide arithmetic edge cases

Tests must exercise carry and borrow across all 4 64-bit limbs, signed boundaries, maximum unsigned values, division corner cases, shifts around the scalar width, and serialization round trips.

## Status labels

- Proposed: design candidate.
- Accepted: decision approved for current revision.
- Implemented: code exists.
- Verified: tests demonstrate specified behaviour.
- Deferred: intentionally postponed.

A feature must not be called verified merely because it compiles.
