# 07 — Memory architecture

**Status:** Research draft

## Fundamental separation

Register width, load/store width, pointer width, virtual-address width, and physical-address width are separate architectural parameters.

A 256-bit scalar can hold a number much larger than the implemented physical address space. An address formed from a register must be validated against the active address-space rules.

## Required memory specification

- Supported load/store sizes.
- Alignment and misalignment behaviour.
- Byte ordering.
- Sign and zero extension.
- Address translation and permissions.
- Page sizes and page-table layout.
- Fault causes and fault-address reporting.
- Atomicity guarantees.
- Memory ordering model.
- I/O and device-memory rules.

## Translation

The first profile may use a deliberately small translation model, but it must define valid virtual ranges, physical limits, page permissions, privilege checks, and translation invalidation behaviour.

## Protection

Instruction fetch, data reads, and data writes should have separately defined permission checks. The kernel must be able to isolate address spaces before process isolation can be claimed.

## Implementation realism

A theoretical address space is not installed RAM. Actual capacity is limited by physical memory devices, buses, controllers, translation hardware, platform design, and implementation cost.
