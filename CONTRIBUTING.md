# Contributing

This is a four-engineer RV32I processor design and **independent verification** project.

## Ownership

| Engineer | RTL ownership | Independent verification ownership |
| --- | --- | --- |
| E1 | Instruction fetch / PC | Decode + register file (E2 RTL) |
| E2 | Decode + register file | Execute + hazards (E3 RTL) |
| E3 | Execute + hazards | Memory + writeback (E4 RTL) |
| E4 | Memory + writeback | Fetch / PC (E1 RTL) |

Roles are provisional until the team assigns members.

## Working agreement

1. Agree on the architecture, scope, and module interfaces before significant implementation work.
2. Use a focused branch and pull request for each change. Link the related GitHub issue.
3. RTL owners may write smoke tests and debug their code, but **the independent verification owner creates the authoritative verification plan/checks and signs off** their subsystem.
4. Verification expected behavior must come from the specification or an independent model, not a copy of the RTL logic.
5. Include relevant test results and documentation changes in the pull request.
6. Require independent review before merging. Never claim a unit, ISA subset, or core is verified until its defined criteria have been met.
7. Keep generated binaries, waveforms and build artifacts out of version control.

## Suggested branch names

- `rtl/fetch`, `rtl/decode`, `rtl/execute`, `rtl/memory`
- `dv/fetch`, `dv/decode`, `dv/execute`, `dv/memory`
- `infra/toolchain`, `docs/architecture`, `integration/core`

## Pull request checklist

- [ ] Linked issue and explained the design or test changes
- [ ] Agreed module interfaces followed (or interface changes reviewed)
- [ ] Relevant checks run and results supplied
- [ ] Independent subsystem verifier reviewed/signs off when applicable
- [ ] Documentation updated for architecture or behavior changes
