# 19 — Research roadmap

**Status:** Initial roadmap; no dates promised.

## Stage A — Charter
Complete scope, terminology, and decision register.
**Exit:** clear non-goals and open questions.

## Stage B — Machine specification
Select register inventory and subfield semantics; specify instruction encoding, arithmetic, execution, address model, reset, privilege, and traps.
**Exit:** versioned base ISA with precise instruction semantics.

## Stage C — Reference emulator
Implement Latticefire with explicit 256-bit arithmetic, deterministic state transitions, memory, exceptions, and traces.
**Exit:** accepted instructions pass boundary and negative tests.

## Stage D — Toolchain
Implement assembler, disassembler, executable format, and linker.
**Exit:** a small assembled program runs in the emulator.

## Stage E — Kernel
Implement Orrenfold for a documented virtual platform.
**Exit:** kernel boots, reports status, and handles a controlled exception.

## Stage F — Evaluation
Measure state-save size, arithmetic cost, code density, and memory behaviour before considering extensions or hardware.
