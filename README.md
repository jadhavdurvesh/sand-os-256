# SAND-256

**Caelvyr — Experimental 256-bit computing architecture research**

SAND-256 is an independent clean-sheet architecture experiment within the SAND Architecture Research Family. It shares family principles while defining its own register organisation, instruction set, execution model, memory contract, toolchain, and ABI.

> **Research status:** This repository contains design proposals and documentation. It does not claim a working processor, emulator, kernel, physical 256-bit address space, or performance advantage.

## Research direction

The first profile investigates 256-bit scalar values with an explicit paired-field interpretation: arithmetic may operate on a full scalar or on architecturally specified subfields. The subfield model must be an ISA rule, not an accidental host-vector implementation.

## Architecture identity

| Concept | Provisional name |
|---|---|
| Architecture | Caelvyr |
| 256-bit scalar register | Aru |
| Register organisation | Aruvane |
| Decoded instruction | Keth |
| Encoded instruction sequence | Kethline |
| Kernel environment | Orrenfold |
| Reference emulator | Latticefire |
| Toolchain | Veyrforge |

Names are provisional project vocabulary, not claims of trademark uniqueness.

## Important width distinction

The initial scalar register target is 256 bits. Pointer width, virtual address width, physical address width, load/store width, and instruction encoding width are independent design decisions. A 256-bit register does not imply that the machine can address or physically contain 2^256 bytes of memory.

## SAND Universal Architecture Foundation

All architectures in the SAND family follow the shared [SAND Universal Architecture Foundation (SUAF)](docs/00-sand-universal-architecture-foundation.md). It establishes common engineering principles and terminology while preserving independent instruction sets, register models, memory contracts, execution semantics, and ABIs.


## Numerical Systems Research

The shared [SAND Numerical Systems Research (SNSR)](docs/22-sand-numerical-systems-research.md) programme investigates alternative radices and numeric representations, including **sexagesimal (base-60)**, balanced ternary, decimal/BCD, fixed- and floating-point, and residue number systems. These are research topics, not claims that every format is implemented in the ISA.

## Documentation

The [docs directory](docs/) contains the architecture specification roadmap, including register design, numeric formats, ISA, memory, addressing, execution, privilege, boot, emulator, toolchain, ABI, kernel, capabilities, verification, and decisions.

## Repository structure

```text
.
├── README.md
├── CONTRIBUTING.md
├── docs/
│   └── architecture specifications and decision records
├── specifications/     Machine-readable ISA definitions (future)
├── emulator/           Latticefire (future)
├── assembler/          Assembler and disassembler (future)
├── compiler/           Compiler backend (future)
├── bootloader/         Virtual platform loader (future)
├── kernel/             Orrenfold (future)
└── tests/              Conformance tests (future)
```

Implementation directories will be created when meaningful code is ready rather than filled with empty placeholders.

## Current status

| Area | Status |
|---|---|
| Project charter | Drafted |
| Architecture terminology | Proposed |
| Register architecture | Proposed / open |
| Instruction set | Not frozen |
| Address and memory model | Open |
| Emulator | Not implemented |
| Toolchain | Not implemented |
| Kernel | Not implemented |
| Hardware | Not implemented |

## Development order

1. Review the design decisions.
2. Freeze a minimal machine specification.
3. Build the reference emulator.
4. Add assembler and executable-image support.
5. Boot a minimal experimental kernel.
6. Measure and evaluate before adding extensions.

See [CONTRIBUTING.md](CONTRIBUTING.md) and [the decision register](docs/20-decision-register.md).

## License

No license has been selected. All rights are reserved unless and until a license is added. Do not assume permission to reuse, redistribute, or modify this repository's contents.
