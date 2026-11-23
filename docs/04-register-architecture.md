# 04 — Register architecture

**Status:** Research draft

## Scalar target

The initial design target is a 256-bit general-purpose scalar register, provisionally called a **Aru**. The full visible register organisation is provisionally called the **Aruvane**.

## Design-specific investigation

The first profile investigates 256-bit scalar values with an explicit paired-field interpretation: arithmetic may operate on a full scalar or on architecturally specified subfields. The subfield model must be an ISA rule, not an accidental host-vector implementation.

The architecture must decide whether scalar values are independent registers, structured groups, or a combination. It must define aliasing, partial writes, read-after-write behaviour, and whether sub-register views exist.

## Required specification

- Number and names of general-purpose registers.
- Special-purpose architectural state.
- Register zero or constant-register policy, if any.
- Instruction-location register semantics.
- Stack and frame conventions, if architectural.
- Register access by privilege level.
- Reset values.
- Context-save and restore rules.
- Extension-state discovery and preservation.

## State-size accounting

If the architecture exposes N general-purpose registers of 256 bits each, their raw scalar storage is N × 256 bits, before special registers, privilege state, vector extensions, or implementation overhead. The register count N is not yet selected.

## Arithmetic interpretation

Register bits are bit-vectors. Instructions must explicitly define unsigned, signed two's-complement, logical, or other interpretations. Host-language integer behaviour must never define guest semantics accidentally.

## Open questions

whether subfield operations belong in the base ISA; register count; instruction encoding; address width; condition-state design; endianness; memory ordering.
