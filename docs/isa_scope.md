# Instruction Set Scope — draft

Target ISA: **RV32I**. Agree on an explicit supported instruction and architectural-behavior checklist before claiming full compliance.

## RV32I instruction families to track

- [ ] Integer register-register arithmetic / logic / shifts
- [ ] Integer immediate arithmetic / logic / shifts
- [ ] Branches and jumps (conditional branches, JAL, JALR)
- [ ] Loads and stores (byte, halfword, word; signed/unsigned loads)
- [ ] Upper immediates and PC-relative operations (LUI, AUIPC)
- [ ] FENCE, ECALL, EBREAK and relevant architectural behavior: **policy TBD**

## Decisions to document

- Alignment and misalignment behavior
- Illegal or unsupported instruction handling
- Exceptions/traps, CSR and privileged support boundaries
- Memory ordering requirements relevant to the implemented scope
- Exact compiler flags and supported bare-metal test setup

**Note:** Partial instruction support is an initial milestone, not full RV32I compliance. Record intentional exclusions and test gaps.
