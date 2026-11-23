# 12 — Boot architecture

**Status:** Planned

## Boot philosophy

The first target is a virtual platform implemented by the reference emulator. Physical hardware is not required for the initial project.

## Boot contract

Specify:
- Reset instruction location and privilege state.
- Memory map and reserved regions.
- Firmware or loader responsibilities.
- Kernel image format.
- Entry-point and relocation rules.
- Device discovery.
- Handoff arguments and boot information.
- How the kernel establishes memory protection.

## Boot stages

A future minimal sequence may be:
1. Emulator reset.
2. Platform state initialisation.
3. Loader validates the kernel image.
4. Loader transfers control with a documented handoff structure.
5. Kernel establishes its own execution and memory state.

Exact stage names and binary formats remain open.
