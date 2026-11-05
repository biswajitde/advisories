# advisories — CleanStart advisory pipeline EMULATION

**EMULATION DATA. These are NOT CleanStart security advisories.** Nothing here is a
statement to customers, and nothing here is consumed by osv.dev or any scanner.

This repository emulates the layout of CleanStart's published advisory repository so
the advisory pipeline (`advisory-platform`, `advisory/lib/advisory-gen.py`) can be
exercised end to end: `advisories/<year>/<CLEANSTART-ID>.json`, one OSV record per file.

- Every record is generated, never hand-written, and carries its own
  `database_specific` provenance (generator, scan, instrument identity).
- Records are produced from scans of **emulation** images built in a test environment.
- ⚠️ Known limitation: the records' `references[type=ADVISORY]` self-link points at the
  production repository path (the generator's repository URL is not yet configurable).
  Treat those links as placeholders.

Seed (2026-11-05): 9 records from the S2 chain hop 4 run on
`ct2-s2-rebuild@sha256:40aee754…`, carried over unchanged from the earlier private
staging repository.
