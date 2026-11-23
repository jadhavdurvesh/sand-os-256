# 16 — Kernel architecture

**Status:** Planned  
**Working identity:** Orrenfold

## Purpose

Orrenfold is the proposed privileged operating-system environment for SAND-256. It is downstream of the ISA and platform contract.

## First kernel responsibilities

- Boot handoff and CPU initialisation.
- Exception and interrupt handling.
- Physical-memory inventory.
- Memory allocation and virtual-memory setup.
- Basic task isolation.
- Minimal system-call interface.
- Emulator console output.

## Wide-state considerations

A 256-bit register model can increase context-save and task-switch costs. The kernel specification must define which architectural state is mandatory to preserve, how extension state is managed, and whether lazy preservation is safe.

## Non-goals for first boot

No initial commitment to a graphical desktop, networking, storage stack, SMP, or broad physical-device support. A small protected kernel is the first meaningful proof.
