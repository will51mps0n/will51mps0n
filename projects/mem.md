---
layout: default
title: Memory Manager and Pager
---

[← Back to Home](../index.html)

## EECS 482 Memory Manager: Virtual Memory Pager
**March 2025**

This project was the culmination of Michigan’s advanced Operating Systems course, where I built a complete **memory pager** to manage virtual memory for multiple processes. The system mimicked an OS kernel module, complete with simulated MMU, swap space, file mapping, page tables, and physical memory.

---

## Overview

The pager implements:
- **Swap-backed and File-backed Pages**
- **On-demand Page Allocation** using `vm_map()`
- **Page Fault Handling** via `vm_fault()`
- **Copy-On-Write Sharing** for forked address spaces
- **Clock Algorithm for Page Replacement**
- **Dirty and Referenced Bit Tracking**
- **Zero Page Pinning Optimization**

All system calls and faults are handled via trap-based interfaces defined in the simulated infrastructure, adhering to strict performance, correctness, and memory safety guarantees.

---

## Key Design Decisions

- **Deferred Work Optimization:** Pages are only loaded and written when strictly necessary, minimizing I/O and CPU overhead.
- **Clock Algorithm Implementation:** Resident pages are evicted with second-chance logic for fairness and efficiency.
- **Copy-on-Write Logic:** Deferred page copying until a write occurs, saving memory and compute for child processes.
- **Shared File-Backed Pages:** Multiple processes can map the same file block, ensuring real OS-like consistency.

---

## Technologies & Concepts

- C++17  
- Page Tables, MMU Simulation  
- Swap File & File I/O  
- Arena-based Virtual Addressing  
- System Call Traps  
- RAII & Smart Pointers  
- Clock (Second-Chance) Eviction

---

## Testing

Wrote 25+ custom test cases that validated:
- Multi-process arena duplication
- Concurrent faults and zero-page reuse
- File mapping corner cases
- Page replacement under memory pressure

---


<p align="center">
  <a href="mailto:adwisi@umich.edu" style="font-size: 20px;">Request Access to Code</a>
</p>
