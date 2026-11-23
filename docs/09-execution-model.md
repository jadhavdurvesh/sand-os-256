# 09 — Execution model

**Status:** Research draft

## Instruction boundary

The reference machine must define a deterministic state transition for each instruction:
1. Fetch bytes from the instruction location.
2. Validate access and encoding.
3. Decode the operation.
4. Validate operands and privilege.
5. Calculate effects.
6. Commit the specified state transition or take a defined exception.
7. Emit an optional deterministic trace record.

## Retirement and faults

The specification must state whether an instruction can partially update architectural state before a fault. The preferred initial rule is precise instruction retirement: no unintended partial architectural effects.

## Initial execution profile

Start with sequential, single-core execution. Parallel issue, speculation, out-of-order retirement, multicore consistency, and hardware scheduling are future research topics.

## Distinctive design constraint

The first profile investigates 256-bit scalar values with an explicit paired-field interpretation: arithmetic may operate on a full scalar or on architecturally specified subfields. The subfield model must be an ISA rule, not an accidental host-vector implementation.

## Reset and state

Reset must define the instruction location, privilege state, register reset behaviour, memory translation state, and interrupt state. Unspecified state must not be allowed to produce nondeterministic test results.
