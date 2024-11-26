
markdown
Copy code
# IITB-RISC-23: 6-Stage Pipelined Processor Design

## Overview

The IITB-RISC-23 is a simple 16-bit RISC-based processor developed for teaching purposes. It uses a 6-stage pipeline architecture, implementing a variety of instructions to demonstrate fundamental computer architecture concepts. The processor is optimized for performance with mechanisms such as forwarding to mitigate data hazards.

## Processor Features

- **16-bit word length**
- **8 General-purpose registers** (R0 to R7), where:
  - **R0** always holds the Program Counter (PC).
- **2 Flags**:
  - **Carry (C)**
  - **Zero (Z)**
- **6-stage pipeline**: 
  1. **Instruction Fetch (IF)**
  2. **Instruction Decode (ID)**
  3. **Register Read (RR)**
  4. **Execute (EX)**
  5. **Memory Access (MEM)**
  6. **Write Back (WB)**

### Pipeline Hazard Mitigation

- **Forwarding**: Data forwarding paths are implemented to handle data hazards, allowing results to be used in subsequent stages without waiting for the data to be written back to the register file.
- **Stall Mechanisms**: A simple stall mechanism may be included for certain data hazards, although forwarding is the primary strategy for performance optimization.
- **Branch Prediction (optional)**: While not required, a branch prediction mechanism may be added to improve branch handling efficiency.

---

## Instruction Set Architecture (ISA)

The IITB-RISC-23 follows the Little Computer Architecture (LCA), and its instruction set consists of three types:

1. **R-Type**: Register-based instructions (e.g., ADD, NAND)
2. **I-Type**: Immediate-based instructions (e.g., Load, Store)
3. **J-Type**: Jump-based instructions (e.g., Jump and Link)
