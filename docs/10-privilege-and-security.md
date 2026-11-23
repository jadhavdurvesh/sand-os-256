# 10 — Privilege and security

**Status:** Research draft

## Minimum protection domains

A practical OS experiment needs at least:
- An unprivileged application domain.
- A privileged kernel domain.

The final architecture may use a different number or naming of privilege levels, but transitions must be explicit and validated.

## Required rules

- Which instructions are privileged.
- Which control registers are readable or writable at each level.
- How software enters the kernel.
- How return to an unprivileged context is validated.
- How memory permissions are enforced.
- How interrupts and exceptions preserve state.
- How address spaces are isolated.
- How debug facilities are controlled.

## Threat model

The initial kernel should assume applications can provide malformed pointers, invalid system-call arguments, and hostile executable images. The architecture must support the kernel in validating these inputs.

## Security claims

A privilege model alone does not prove the system secure. Security requires implementation, testing, and review of the complete kernel, toolchain, boot path, and platform.
