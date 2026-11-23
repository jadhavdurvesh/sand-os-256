# 06 — Instruction-set architecture

**Status:** Research draft

## Instruction identity

A decoded operation is provisionally called **Keth**. The encoded instruction stream is provisionally called **Kethline**. These labels do not imply an encoding has been selected.

## Candidate operation groups

- Data movement and immediate construction.
- 256-bit integer arithmetic.
- Logical and bit-field operations.
- Signed and unsigned comparisons.
- Loads and stores of explicitly supported widths.
- Control transfer.
- System entry and privileged control.
- Atomic and memory-ordering operations, if included.
- Optional numeric extensions.

## Encoding decision

The project must compare fixed-width, variable-width, and structured hybrid encodings. Criteria include decode complexity, code density, immediate range, extension space, alignment, and toolchain effort.

No opcode values are assigned in this draft.

## Instruction specification template

Every accepted instruction must document:
1. Stable identifier and mnemonic.
2. Binary encoding and field layout.
3. Operand types and legal register forms.
4. Exact result calculation.
5. Architectural state read and written.
6. Overflow and status effects.
7. Faults and exception priority.
8. Privilege requirements.
9. Examples and boundary tests.

## Design-specific requirement

The first profile investigates 256-bit scalar values with an explicit paired-field interpretation: arithmetic may operate on a full scalar or on architecturally specified subfields. The subfield model must be an ISA rule, not an accidental host-vector implementation.

The final ISA must be original in its actual encodings and semantics, not merely in its instruction names.
