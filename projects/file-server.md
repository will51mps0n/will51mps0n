---
layout: default
title: Multithreaded File Server
---

[← Back to Home](../index.html)

# Multithreaded File Server
[View Code on GitHub](https://github.com/will51mps0n/Networked-Fs-Cpp)

## Overview

This project simulates a multithreaded network file server with a Unix-style hierarchical file system. It supports directory traversal, file creation, deletion, reading, and writing across concurrent client requests using Boost threads and RAII locking.

Each path is parsed and locked step-by-step, with strict permission enforcement and deep integration into a simulated disk subsystem.

## Features

- Hierarchical directory and file structure
- Boost `shared_mutex` read/write lock guards
- RAII-style concurrency control
- Socket-based communication and custom request parsing
- Safe deletion and cleanup of blocks and inodes
- Block reuse and free list management
- Hand-over-hand locking for safe traversal

## Key Design Decisions

- **RAII Locks:** Used scoped guards for thread-safe disk operations.
- **Deferred Deletion:** Safely cleans up data blocks and metadata for both files and directories.
- **Deadlock-Free Traversal:** Locks are acquired in strict order with read/write granularity.
- **Dynamic Allocation:** Blocks are dynamically allocated and recycled via a custom `DiskManager`.

## Technologies & Concepts

**C++17**, **Boost Threads**, **RAII**, **Sockets**, **Custom File System**, **Concurrency**, **Inodes**, **Block Reuse**, **Thread-safe Memory Management**

## Testing & Validation

Wrote 30+ edge case tests validating:

- Concurrent client operations
- Nested path traversal
- Directory shrinkage after deletion
- Reuse of freed blocks
- Proper lock acquisition and release

[← Back to Home](../index.html)
---

