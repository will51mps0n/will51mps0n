---
layout: default
title: Pipeline Simulator & Assembler
github_url: https://github.com/will51mps0n/Assembler-and-Simulator
---

[← Back to Home](../index.html)

# Pipeline Simulator & Assembler  
[View Code on GitHub](https://github.com/will51mps0n/Assembler-and-Simulator)

---

## Overview

This project implements both an **Assembler** and a **5-Stage Pipeline Simulator** for the LC-2K instruction set architecture (ISA), fully written in C. It provides low-level insight into how a processor parses assembly instructions, manages control flow, detects hazards, and simulates pipeline stages like modern CPUs.

The project is divided into two components:

1. **Assembler:**
   - Converts LC-2K assembly code into 32-bit machine code.
   - Handles labels, opcode translation, offset calculations, and error checking.

2. **Pipeline Simulator:**
   - Simulates a 5-stage pipeline: IF, ID, EX, MEM, WB.
   - Implements data hazard detection, stalling, and forwarding to ensure correctness.
   - Prints state of memory, registers, and pipeline registers after each cycle.

---

## Features

### Assembler:
- **Label Management:**
  - Parses up to 1000 assembly lines.
  - Detects duplicate labels and invalid labels.
  - Calculates relative addresses for branch instructions.

- **Opcode Translation:**
  - Supports LC-2K instructions: `add`, `nor`, `lw`, `sw`, `beq`, `jalr`, `halt`, `noop`, `.fill`.
  - Converts instructions into 32-bit machine code with proper register and offset encoding.

- **Error Handling:**
  - Checks register bounds (0–7).
  - Ensures valid label usage.
  - Detects invalid opcodes and out-of-range offsets.

---

### Pipeline Simulator:
- **Instruction Memory & Data Memory:**
  - Supports up to 65,536 memory locations.
  - Initializes program memory from machine code file.

- **Pipeline Stages:**

| Stage | Description |
|-------|-------------|
| **IF**  | Instruction Fetch: loads instruction and increments PC |
| **ID**  | Instruction Decode: reads registers, detects hazards, stalls if necessary |
| **EX**  | Execute: ALU operations, calculates branches, sets branch target |
| **MEM** | Memory: executes load/store instructions, resolves branches |
| **WB**  | Write Back: writes results to registers |

- **Hazard Detection & Handling:**
  - **Data Hazards:**
    - Implements stalling when a `lw` instruction is followed by a dependent instruction.
  - **Forwarding:**
    - Forwards values from EX/MEM and MEM/WB stages to avoid stalls.
  - **Branch Handling:**
    - Clears pipeline with no-ops when branch is taken to ensure correctness.

- **Verbose Output:**
  - Displays the state of the pipeline, memory, and registers after every clock cycle.
  - Provides detailed visualization of each pipeline register, including instruction values, ALU results, and branch decisions.

---

## Technologies
- C
- Assembly Parsing & Translation
- Pipelining
- Version Control
- Automated Testing with Bash

---

[← Back to Home](../index.html)