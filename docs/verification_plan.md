# Verification Plan — draft

**Principle:** Every engineer designs one subsystem and independently verifies someone else's design. Designers may run local smoke tests but cannot be sole sign-off for their own RTL.

| DUT owned by | Verification led by | Scope |
| --- | --- | --- |
| E1 | E4 | Fetch/PC, redirects, stalls, flush behavior |
| E2 | E1 | Decode, immediates, register-file behavior |
| E3 | E2 | ALU, branches, forwarding and hazards |
| E4 | E3 | Load/store access sizing, alignment policy and writeback |

## Required evidence for each subsystem

- [ ] Verification plan derived from its interface/specification
- [ ] Directed boundary and corner-case tests
- [ ] Self-checking tests with independent expected results
- [ ] Relevant assertions and functional coverage (as tooling permits)
- [ ] Reproducible regression commands / recorded seeds
- [ ] Failure logs and waveforms for unresolved bugs
- [ ] Independent verification owner signs off the issue

## Full-core verification

- [ ] Directed RV32I assembly programs and test runner
- [ ] Independent architectural reference comparison (e.g. Spike)
- [ ] Instruction-retirement trace design
- [ ] Randomized instruction regressions and test-result summaries
- [ ] Measured functional coverage; document exclusions and gaps
- [ ] Synthesis sanity check and final integrated demonstration

**Do not equate passing a small directed test suite with comprehensive RV32I compliance.**
