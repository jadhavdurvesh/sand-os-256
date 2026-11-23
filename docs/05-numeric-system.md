# 05 — Numeric system

**Status:** Research draft

## 256-bit scalar range

A 256-bit unsigned scalar spans 0 through 2^256−1 and requires up to 78 decimal digits or 64 hexadecimal digits.

For unsigned interpretation:

\[
0 \leq x \leq 2^{256}-1
\]

For signed two's-complement interpretation:

\[
-2^{255} \leq x \leq 2^{255}-1
\]

A 256-bit value contains 32 octets. These are value-representation facts, not memory-capacity claims.

## Numeric formats to evaluate

- Unsigned binary integers.
- Signed two's-complement integers.
- Saturating and wrapping arithmetic, if specified as distinct operations.
- Fixed-point formats.
- Floating-point formats as a separately specified extension.
- Multi-register and arbitrary-precision arithmetic.
- Packed and subfield representations, where justified by the architecture's research direction.

## Arithmetic contract

Every operation must specify operand interpretation, result width, overflow behaviour, division by zero, signed division edge cases, shift-count rules, carry/borrow semantics, and exception behaviour.

## Number bases

Binary is the underlying bit representation. Decimal, hexadecimal, and octal are human-readable notations. A wider architecture does not require a new positional number base.

## Emulator requirements

Arithmetic helpers must have explicit wrap, sign-extension, comparison, division, and shift behaviour. Use a tested multi-limb implementation if the host language cannot directly represent the full scalar width.
