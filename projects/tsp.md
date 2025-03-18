---
layout: default
title: Traveling Salesman Solver
---

[← Back to Home](../index.html)

# Traveling Salesman Solver: MST, FASTTSP, and OPTTSP Algorithms  
*April 2023*

---

## Overview

This project implements an efficient C++ solution to the classic **Traveling Salesman Problem (TSP)**, offering three distinct solving modes:

1. **Minimum Spanning Tree (MST) Mode**  
2. **Heuristic TSP Solver (FASTTSP) Mode**  
3. **Optimal TSP Solver (OPTTSP) Mode**

The project is focused on both performance and accuracy, emphasizing efficient graph traversal, memory management, and advanced pruning techniques.

---

## Features
- **Command-line Interface:**  
  - Simple flag-based interface allowing users to select `MST`, `FASTTSP`, or `OPTTSP` modes.
  
- **MST Mode:**  
  - Implements **Prim's Algorithm** to compute the Minimum Spanning Tree for the input graph.
  
- **FASTTSP Mode:**  
  - Utilizes a **Greedy Nearest-Neighbor heuristic** to approximate the TSP tour quickly.
  
- **OPTTSP Mode:**  
  - Employs a **Branch & Bound algorithm** combined with:
    - Permutation generation
    - MST-based lower bounds for remaining vertices
    - Smart pruning of suboptimal paths

---

## How It Works

### Modes Breakdown:
| Mode      | Algorithm Implemented | Approach |
|----------|----------------------|---------|
| **MST**      | Prim’s Algorithm | Priority Queue & Edge Weights |
| **FASTTSP**  | Nearest-Neighbor Heuristic | Greedily selects closest unvisited vertex |
| **OPTTSP**   | Branch & Bound | MST lower bounds & pruning |

---

## Technologies
- C++
- Command-line Interface
- Dynamic Memory Management
- Automated testing with Bash scripting

---

## Repository
[View Code on GitHub](https://github.com/will51mps0n/tsp_solver)

---

[← Back to Home](../index.html)