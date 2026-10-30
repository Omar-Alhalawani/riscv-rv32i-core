# RTL Interfaces — draft

Freeze interface definitions with **all four engineers** before implementation. The table below is a starting checklist, not an approved signal-level specification.

| Boundary | Agree on |
| --- | --- |
| Fetch ↔ instruction memory | address, request/response, valid/ready, response latency, faults |
| IF/ID | PC, instruction, valid, stall and flush behavior |
| ID/EX | decoded operands, immediates, register indices, controls and valid |
| EX/MEM | ALU result, branch outcome, store data, destination/control, valid |
| MEM/WB | load result, ALU result, destination/control, valid |
| Memory ↔ data memory | address, byte enables, data, read/write response timing |
| Writeback ↔ register file | destination, data, write enable, x0 suppression |
| Hazard/forwarding ↔ pipeline | operand selection, stall, bubble, redirect and flush priority |

## Questions before coding

- [ ] Reset/clock convention
- [ ] Consistent signal naming and width conventions
- [ ] Who owns pipeline registers and top-level integration?
- [ ] How do memory wait states propagate?
- [ ] How is an instruction's architectural retirement reported to verification?
