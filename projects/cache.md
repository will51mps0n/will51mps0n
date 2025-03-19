---
layout: default
title: LC-2K Cache Simulator
---

[← Back to Home](../index.html)

# LC-2K Cache Simulator  
*March 2025*

---

## Overview

This project involves developing a **Cache Simulator** for the LC-2K instruction set architecture (ISA), implemented in C. The simulator integrates with an existing LC-2K processor simulator to model the behavior of a CPU cache, providing insights into memory access patterns, cache hits and misses, and the impact of cache configurations on performance.

---

## Features

- **Configurable Cache Parameters:**
  - **Block Size:** Adjustable number of words per cache block.
  - **Number of Sets:** Defines the number of sets in the cache.
  - **Blocks Per Set:** Determines the associativity of the cache, ranging from direct-mapped to fully associative configurations.

- **Write Policy:**
  - Implements a **write-back** policy with **allocate-on-write**, meaning data is written to the cache and marked dirty; the main memory is updated only upon eviction.

- **Replacement Policy:**
  - Utilizes the **Least Recently Used (LRU)** algorithm to decide which cache block to evict upon a cache miss when the set is full.

- **Cache Operations:**
  - **Read (Fetch/lw):** Retrieves data from the cache; if absent, loads it from memory into the cache.
  - **Write (sw):** Writes data to the cache and marks the block as dirty; updates main memory upon eviction.

- **Statistics Tracking:**
  - Monitors cache hits, misses, memory accesses, and write-backs to evaluate cache performance.

---

## How It Works

### Cache Structure:

The cache is organized into multiple sets, each containing a fixed number of blocks. Each block comprises:

- **Data Array:** Stores the actual data words.
- **Metadata:**
  - **Valid Bit:** Indicates if the block contains valid data.
  - **Dirty Bit:** Shows if the block has been modified (write-back required upon eviction).
  - **Tag:** Identifies the memory address associated with the block.
  - **LRU Label:** Used to track the usage for implementing the LRU replacement policy.

### Address Breakdown:

An LC-2K memory address is divided into:

- **Tag:** Identifies the specific block within the cache.
- **Set Index:** Determines which set the block belongs to.
- **Block Offset:** Specifies the exact word within the block.

### Cache Initialization (`cache_init`):

Sets up the cache based on user-defined parameters:

- **Block Size:** Number of words per block.
- **Number of Sets:** Total sets in the cache.
- **Blocks Per Set:** Associativity level.

Validates input parameters, initializes cache structures, and sets all blocks as invalid initially.

### Cache Access (`cache_access`):

Handles memory read and write operations:

- **Read Operation:**
  - Checks if the data is in the cache (cache hit); if so, returns the data.
  - On a cache miss, loads the block from memory into the cache, possibly evicting an existing block based on the LRU policy.

- **Write Operation:**
  - Writes data to the cache and marks the block as dirty.
  - If the block is not present, loads it into the cache (write-allocate) and then performs the write.

### Replacement Policy:

Implements the LRU strategy:

- Each block in a set has an LRU label indicating its usage recency.
- Upon accessing a block, updates LRU labels to reflect the most recent access.
- On eviction, selects the block with the highest LRU label (least recently used).

---

## Technologies

- C
- Bit Manipulation
- Cache and Memory Management

---

## Repository
Add LATER
[View Code on GitHub](https://github.com/will51mps0n/Cache)

---

[← Back to Home](../index.html)