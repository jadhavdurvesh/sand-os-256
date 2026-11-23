# 02 — Architecture overview

**Architecture:** Caelvyr  
**Status:** Proposed

## Architectural layers

Caelvyr is divided into independently specified layers:

1. Value and scalar model.
2. Register inventory and state visibility.
3. Instruction encoding and semantics.
4. Execution and retirement model.
5. Address formation and memory translation.
6. Privilege, traps, and interrupts.
7. Platform reset and boot contract.
8. Executable format and software ABI.

## Distinctive research direction

The first profile investigates 256-bit scalar values with an explicit paired-field interpretation: arithmetic may operate on a full scalar or on architecturally specified subfields. The subfield model must be an ISA rule, not an accidental host-vector implementation.

## Architectural state

The specification must enumerate all state visible at an instruction boundary: general registers, instruction location, status state, control registers, translation context, privilege state, and extension state. It must define reset values and which state is accessible at each privilege level.

## Execution profile

The first reference profile should be deterministic and single-core. Superscalar, speculative, out-of-order, multicore, and cache-coherence behaviour are deferred until the sequential architectural contract is stable.

## Width is not capacity

A 256-bit register stores a 256-bit value. It does not prove that the machine can address or physically install 2^256 bytes of RAM. The architecture must separately define implemented address bits and platform limits.

## Open areas

The initial unresolved questions are recorded in [the decision register](20-decision-register.md). No instruction encoding or address width is considered stable until accepted.
