# 20 — Architecture decision register

**Codename:** Caelvyr

Statuses: Open, Proposed, Accepted, Superseded, Rejected.

### C256-001 — Project independence
**Status:** Accepted. SAND-256 is an independent architecture in the SAND family. Shared principles do not imply shared ISA or ABI.

### C256-002 — Scalar width
**Status:** Proposed. General-purpose scalar target is 256 bits.

### C256-003 — Subfield model
**Status:** Open. Decide whether subfields are operands, views, or register groups; define widths, aliasing, lane order, and partial writes.

### C256-004 — Register inventory
**Status:** Open. Select count, names, special state, and reset behaviour.

### C256-005 — Address widths
**Status:** Open. Choose pointer, virtual, and physical address widths independently.

### C256-006 — Instruction encoding
**Status:** Open. Compare fixed, variable, and hybrid formats.

### C256-007 — Endianness and alignment
**Status:** Open. Specify byte order and all supported access alignment rules.

### C256-008 — Privilege and events
**Status:** Open. Define privilege domains, reset, traps, interrupts, and return semantics.

### C256-009 — ABI
**Status:** Open. Define calling convention, pointer representation, system-call ABI, and executable format.

Every accepted decision must include context, alternatives, rationale, consequences, affected specifications, and conformance tests.
