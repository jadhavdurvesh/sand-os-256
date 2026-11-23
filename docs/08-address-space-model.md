# 08 — Address-space model

**Status:** Open research area

## Address concepts

- **Pointer representation:** how software encodes references.
- **Virtual address width:** implemented virtual address bits.
- **Physical address width:** implemented physical address bits.
- **Register width:** 256 bits in the initial scalar target.
- **Addressable unit:** the smallest independently addressable unit, normally an octet but not assumed until accepted.

## Address formation

The ISA must specify effective-address calculation, permitted arithmetic, wrap detection, canonical or valid ranges, alignment, and invalid-address faults.

## Virtual-memory questions

- Number of address-space contexts.
- Translation-table format.
- Page sizes and large-page rules.
- Permission bits.
- User/supervisor separation.
- Translation cache behaviour.
- Invalidation and synchronisation.
- Fault classification.

## Do not assume full-width addressing

Using all 256 register bits as a virtual address would create a theoretical 2^256-byte byte-addressed space. This is not required and is unlikely to be a useful initial implementation target. The first profile should choose an implementable address width based on explicit trade-offs.

## Decision gate

No pointer ABI or page-table structure should be frozen until the address-width and translation decisions have been accepted.
