# 01 — Vision and scope

**Architecture:** Caelvyr  
**Target scalar width:** 256 bits  
**Status:** Research proposal

## Purpose

SAND-256 is an independent experimental architecture within the SAND Architecture Research Family. It shares the family's design discipline, documentation conventions, and emulator-first philosophy, but it is not an extension mode of SAND-128 and does not inherit another repository's ISA or ABI.

The Caelvyr project investigates paired-field scalar design. Its goal is to produce a precise machine specification, a reference emulator, a minimal toolchain, and eventually a small experimental operating-system kernel.

## Design objectives

- Define a genuinely independent instruction set and machine contract.
- Investigate 256-bit general-purpose scalar values.
- Specify register, arithmetic, pointer, virtual-address, physical-address, and instruction widths separately.
- Make every observable behaviour deterministic and testable.
- Record design alternatives before freezing decisions.
- Distinguish theoretical capacity from practical hardware capability.

## Non-goals

- Commercial processor development.
- Claims that a wider register automatically makes a computer faster.
- Claims of compatibility with x86-64, AArch64, RISC-V, or another ISA.
- Assuming 256-bit pointers or 256-bit physical addressing merely because scalar registers are 256 bits.
- Reusing another SAND architecture's instruction encoding or ABI by default.

## Initial research direction

The first profile investigates 256-bit scalar values with an explicit paired-field interpretation: arithmetic may operate on a full scalar or on architecturally specified subfields. The subfield model must be an ISA rule, not an accidental host-vector implementation.

This is a research direction, not a frozen design. The exact register inventory, encodings, privilege model, address translation, and platform contract remain open until accepted through decision records.

## Width separation

| Property | Initial direction |
|---|---|
| General-purpose scalar register | 256 bits, proposed |
| Native integer arithmetic | At least 256 bits, proposed |
| Pointer width | Open |
| Virtual address width | Open; independent of scalar width |
| Physical address width | Platform-defined; open |
| Instruction encoding width | Open |
| Vector or packed-data width | Open |

## Relationship to the SAND family

The family shares engineering principles, not binary compatibility. Each architecture must have independent register semantics, instruction definitions, exception rules, memory model, executable format, and ABI. Shared tooling may be developed later only where it does not compromise architectural independence.

## Success criteria

The first success is a reviewed specification and a reference emulator that passes a small, rigorous conformance suite. A bootable kernel comes later.
