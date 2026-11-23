# 17 — Memory and numerical capabilities

**Status:** Theoretical reference; not a hardware claim

## Scalar value capacity

A 256-bit scalar contains 256 bits, or 32 octets.

- Number of bit patterns: 2^256.
- Unsigned range: 0 through 2^256−1.
- Signed two's-complement range: −2^255 through 2^255−1.
- Maximum unsigned decimal representation: approximately 78 digits.
- Hexadecimal representation: 64 digits.

## Theoretical byte-address space

If every bit of a 256-bit address were used for byte addressing, the mathematical space would be 2^256 bytes. This is a theoretical upper bound, not an implementation target.

| Concept | Meaning |
|---|---|
| Register capacity | Values a scalar register can represent |
| Virtual address space | Addresses a process may form and translate |
| Physical address space | Locations the platform can identify |
| Installed RAM | Actual memory devices present |
| Memory bandwidth | Rate of data transfer |
| Storage capacity | Persistent storage available |

These quantities are not interchangeable.

## Practical constraints

Actual memory capacity depends on memory devices, buses, controllers, physical address implementation, translation structures, platform design, and cost. A wider pointer can increase memory use without increasing installed RAM.

## Required future measurements

Any emulator or hardware prototype must report implemented virtual and physical address widths, memory limits, transfer widths, alignment rules, and measured performance. Theoretical bit counts must never be presented as measured capacity.
