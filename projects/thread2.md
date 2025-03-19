---
layout: default
title: Custom C++ Thread Library
github_url: https://github.com/eecs482/adwisi.ecomini.skis.2

---

[← Back to Home](../index.html)

---

# C++ Thread Library: Cooperative Threads & Monitors  
*February 2025*

---

## Overview

This project implements a custom **C++ Thread Library** that simulates cooperative multithreading and synchronization primitives such as **mutexes** and **condition variables**. It demonstrates how operating systems manage context switching, thread lifetimes, and interrupt handling, offering a hands-on perspective on low-level threading concepts.

---

## Features

- **Custom Thread Scheduling**
  - FIFO ready queue ensuring predictable scheduling behavior.
  - Voluntary context switches via `thread::yield()`.

- **Thread Context Switching**
  - Built from scratch using `ucontext_t` structures.
  - Implemented `makecontext`, `swapcontext`, and `setcontext` logic.

- **Mutexes & Condition Variables**
  - Mutexes ensure mutual exclusion with FIFO queueing.
  - Condition Variables allow threads to wait and signal efficiently.
  - Correct handling of edge cases like signaling without lock.

- **Interrupt Handling**
  - Timer interrupt and IPI (inter-processor interrupt) support.
  - Atomic interrupt disable/enable wrapped in guard structures.

- **CPU Management**
  - Multi-CPU support with a global ready queue (advanced setup ready).
  - CPU suspension when no runnable threads are available.

- **Error Detection & Robustness**
  - Exception handling for illegal mutex unlocks and bad thread usage.
  - Resource deallocation on thread completion.
  - Smart pointers and RAII patterns used throughout to avoid memory leaks.

---

### Key Components:
| Component            | Functionality                                                                                      |
|---------------------|---------------------------------------------------------------------------------------------------|
| **cpu class**        | Bootstraps CPUs, sets up interrupt handlers, manages thread execution, and handles CPU suspension. |
| **thread class**     | Manages thread creation, voluntary yielding, joining, and context switching.                      |
| **mutex & cv classes** | Provides mutual exclusion and thread synchronization mechanisms (FIFO order).                    |
| **ucontext API**     | Low-level context switching primitives (`makecontext`, `swapcontext`, `setcontext`).               |

---

## Technologies
- C++ (C++17/20)
- Low-level Systems Programming
- `ucontext` API
- Smart Pointers & RAII
- Manual Memory Management
- Exception Handling

---

## Access
Message me for access to this repo due to the EECS 482 Umich Honor Code :c
[View Code on GitHub](https://github.com/eecs482/adwisi.ecomini.skis.2)

---

[← Back to Home](../index.html)