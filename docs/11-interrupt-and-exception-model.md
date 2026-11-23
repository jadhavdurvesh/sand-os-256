# 11 — Interrupt and exception model

**Status:** Research draft

## Event classes

- **Synchronous exception:** caused by the instruction being executed.
- **Asynchronous interrupt:** delivered independently of the current instruction.
- **Reset event:** establishes the initial machine state.

## Candidate exception causes

Invalid encoding, privilege violation, address translation fault, access violation, alignment fault, explicit software trap, and arithmetic fault where the ISA defines trapping arithmetic.

## Required specification

- Event identifiers and priority.
- Vector-table or dispatch mechanism.
- Saved instruction location.
- Saved status and privilege state.
- Fault address and cause reporting.
- Nesting and masking rules.
- Return-from-event semantics.
- Interrupt acknowledgement and pending state.

## Emulator plan

The reference emulator should inject asynchronous events as explicit inputs so tests remain deterministic. Event ordering must be specified.
