# 15 — ABI specification

**Status:** Not yet specified

The ABI is the software contract between compiled programs, runtime libraries, and the operating system. It is independent of the register-width headline.

## Required decisions

- Pointer width and representation.
- Argument and return-value locations.
- Register preservation rules.
- Stack layout and alignment.
- Structure layout and padding.
- System-call entry and return.
- Error representation.
- Object format and relocation types.
- Symbol conventions.
- Unwind and exception conventions, if supported.
- Versioning and feature discovery.

## Wide values

The ABI must define whether a 256-bit value is passed in one scalar register, multiple registers, or memory. It must specify alignment and aggregate layout. No convention should be inferred from another SAND architecture.

## Compatibility

ABI compatibility requires stable documented rules and tests. Similar register widths do not imply binary compatibility.
