# Architecture — draft

**Status:** To be defined and approved by the team. No processor implementation is present yet.

## Proposed baseline

- ISA target: RV32I (specific instruction and exception scope to be documented in [ISA scope](isa_scope.md)).
- Five-stage in-order, single-issue pipeline: IF → ID → EX → MEM → WB.
- Separate instruction and data interfaces for the initial educational implementation.
- Four pipeline-register boundaries: IF/ID, ID/EX, EX/MEM, MEM/WB.

## Subsystem ownership (proposed)

| Subsystem | RTL owner | Independent verification owner |
| --- | --- | --- |
| Instruction fetch + PC control | E1 | E4 |
| Decode, immediate generator + register file | E2 | E1 |
| Execute, branch, forwarding + hazards | E3 | E2 |
| Load/store + writeback | E4 | E3 |

## Architecture decisions required

- [ ] Reset value, reset semantics and clocking
- [ ] Memory protocol, latency, alignment and errors
- [ ] Pipeline valid, stall and flush semantics
- [ ] Forwarding, load-use stalls, branch resolution/redirect handling
- [ ] Exceptions, traps, CSRs and privileged-mode scope
- [ ] Architectural retirement trace / reference comparison interface
- [ ] Performance and synthesis goals

Add detailed block diagrams under `docs/diagrams/` when the interfaces are approved.
