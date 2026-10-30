# riscv-rv32i-core
Design and independent verification of a five-stage pipelined RISC-V RV32I processor in SystemVerilog.

## Team ownership

| Engineer | RTL design responsibility | Independent verification responsibility |
| --- | --- | --- |
| **[Adam](https://github.com/AdamAIbrahim)** | Instruction fetch (IF), PC and redirects | Zayd's instruction decode and register file |
| **[Zayd](https://github.com/zaydb-dev)** | Instruction decode (ID), immediates and register file | Omar's execute, forwarding and hazards |
| **[Omar](https://github.com/Omar-Alhalawani)** | Execute (EX), ALU, branch logic and hazards | Suhaib's memory access and writeback |
| **[Suhaib](https://github.com/Suhaib-Ben-Zreiba)** | Memory access (MEM), load/store and writeback (WB) | Adam's instruction fetch and PC control |

All four engineers share responsibility for architecture, integration, processor-level verification, synthesis and documentation.

See [architecture](docs/architecture.md), [verification plan](docs/verification_plan.md), and [contributing guidelines](CONTRIBUTING.md). This repository currently contains project scaffolding and draft specifications, not a completed processor.
