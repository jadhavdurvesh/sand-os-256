# Contributing to SAND-256

SAND-256 is an experimental architecture research project. Work specification-first.

1. Read the project charter and relevant architecture documents.
2. Check the decision register before introducing a new architectural rule.
3. Record alternatives and trade-offs.
4. Update the specification before relying on behaviour in code.
5. Add positive, negative, and boundary tests.
6. Mark work accurately as proposed, accepted, implemented, or verified.

Do not copy another ISA's encodings, ABI, or exception rules and merely rename them. Existing designs may be studied and cited. Keep this repository independent from other SAND architecture repositories.

The reference emulator must be deterministic and must not depend on host-language overflow or undefined behaviour. A feature is not verified until tests demonstrate its specified behaviour.

Coined names are provisional until checked for collisions. Technical precision takes priority over decorative terminology.
