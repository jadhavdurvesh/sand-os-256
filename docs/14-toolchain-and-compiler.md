# 14 — Toolchain and compiler

**Status:** Planned  
**Toolchain codename:** Veyrforge

## Components

- Assembler.
- Disassembler.
- Object format.
- Linker and relocation model.
- Executable-image builder.
- Compiler backend.
- Runtime support.
- Emulator integration.

## Development order

1. Freeze the first instruction subset.
2. Build assembler and disassembler.
3. Define object and executable formats.
4. Implement a linker or image builder.
5. Add a compiler backend after register allocation and ABI decisions are stable.

## Compiler requirements

The compiler must model 256-bit values accurately. It must not assume pointer width equals scalar width. Register classes, calling conventions, alignment, and extension state must be represented explicitly.

## Verification

Round-trip assembler/disassembler tests, relocation tests, malformed-object rejection, ABI conformance, and emulator integration are required.
