---
layout: default
title: Adam Simpson
---


<p style="text-align: center; font-weight: bold;">
  <span style="
      color:rgb(0, 0, 0); 
      font-size: 28px;">B.S. in Electrical Engineering & Computer Science</span><br>
  
  <span style="
      color:rgb(12, 51, 86); 
      font-size: 26px; 
      text-shadow: 
        -1px -1px 0 #FFCB05, 
        1px -1px 0 #FFCB05, 
        -1px 1px 0 #FFCB05, 
        1px 1px 0 #FFCB05;">University of Michigan, Class of 2025</span>
</p>

## About Me

I’m a recent graduate from the University of Michigan with a B.S. in Electrical Engineering and Computer Science, focused on systems engineering and infrastructure, software development, and data science and machine learning.

My work spans low-level systems projects — including a virtual memory pager, a multithreaded file server, and custom threading libraries in C and C++ — as well as applied machine learning and full-stack development. I’ve built end-to-end applications like WaitFast, a mobile app with a live Flask/AWS backend, and explored deep learning through computer vision and reinforcement learning projects using PyTorch.

This portfolio highlights a selection of these projects, with technical breakdowns, source code, and reflections on the challenges tackled and lessons learned.

Click on the blue titles below to be redirected to the dedicated project pages.

---

## My Projects

### Systems & Infrastructure 

- [**Multithreaded File Server – C++**](./projects/file-server.html)  
  Designed and implemented a networked file server supporting concurrent client requests and hierarchical path traversal. The server communicates over TCP sockets and ensures crash consistency and correctness through atomic disk writes and thread-safe I/O using RAII and Boost locks.   
  **Skills:** Multithreading, RAII, Boost Locks, Socket Programming, File Systems

- [**Virtual Memory Pager – C++**](./projects/mem.html)  
  Built a virtual memory subsystem that handles page faults, copy-on-write behavior, and page eviction using the clock algorithm. The pager simulates real-world memory management logic, including read/write protections and shared memory scenarios across processes.  
  **Skills:** Virtual Memory, Page Tables, MMU Simulation, Copy-on-Write, Clock Algorithm

- [**Custom Thread Library – C++**](./projects/thread2.html)  
  Developed a cooperative user-level threading library using ucontext.h, supporting thread scheduling, context switching, and synchronization primitives like mutexes and condition variables.  
  **Skills:** Thread Scheduling, ucontext, Mutexes, Condition Variables

- [**LC-2K Assembler & Pipeline Simulator – C**](./projects/assembler.html)  
  Wrote a full assembler and 5-stage pipelined simulator for the LC-2K instruction set, with support for label resolution, instruction decoding, and pipeline hazard mitigation. 
  **Skills:** Systems Programming, Assembly, Pipeline Simulation

- [**LC-2K Cache Simulator – C**](./projects/cache.html)  
  Simulated a parameterized LRU cache system with support for configurable block and set sizes. Logged memory operations to validate eviction policy and cache performance under various workloads.  
  **Skills:** Memory Management, Cache Simulation, LRU Policy

- [**Traveling Salesman Solver – C++**](./projects/tsp.html)  
  Implemented a TSP solver combining minimum spanning tree heuristics, nearest insertion, and optimized branch & bound search to compute near-optimal tour paths.    
  **Skills:** Algorithm Design, MST, Heuristics, Bash Scripting

---

### Data Science, Artificial Intelligence, & Machine Learning

- [**Power Outage Analysis – Python & ML**](./projects/power-outage.html)  
  Built a regression pipeline to estimate the financial cost of power outages using Random Forests. Focused on extensive feature engineering and hyperparameter optimization on real utility data.  
  **Skills:** Scikit-learn, Pandas, Data Cleaning, Feature Engineering, Regression, Hyperparameter Tuning

- [**Stock Prediction Pipeline – Python**](./projects/stock.html)  
  Developed an end-to-end forecasting system for stock prices, integrating live data scraping, technical indicators, and models like LSTM and Random Forests to predict future price movements.   
  **Skills:** Time Series Forecasting, API Integration, Linear Regression, Random Forest, LSTM

- [**AlphaZero Othello – Python & AI**](./projects/alz.html)  
  Trained an AlphaZero-inspired agent using Monte Carlo Tree Search and a deep neural network for board evaluation and policy guidance. Self-play loop built for continuous model improvement.  
  **Skills:** PyTorch, Reinforcement Learning, MCTS, Neural Networks

- [**CIFAR-10 Classifier – Python & AI**](./projects/img.html)  
  Built image classification models on CIFAR-10 using CNNs and fully connected networks. Ran grid search over architectures and training hyperparameters to compare accuracy and convergence.  
  **Skills:** PyTorch, CNNs, Hyperparameter Tuning

- [**Connect Four AI – Python**](./projects/connect_four.html)  
  Engineered a perfect-play Connect Four AI using the Minimax algorithm with alpha-beta pruning and a hand-crafted evaluation function. Includes an interactive UI with Pygame.  
  **Skills:** AI Search Algorithms, Game Theory, Pygame

---

### Mobile & Full-Stack Development

- [**WaitFast – Python, Swift, SQL**](./projects/wait_fast.html)  
  Built an IOS mobile app that crowdsources and displays real-time wait times at local venues. Backend includes a live Flask API, PostgreSQL database, and AWS-hosted infrastructure.  
  **Skills:** iOS UI/UX, Flask, AWS, PostgreSQL, Google & Apple APIs, Version Control

---


<p align="center" style="font-family: 'Lato', sans-serif;">
  <span style="font-size: 30px; color:rgb(26, 188, 93); font-weight: normal;">Connect with Me</span><br>
  <span style="font-size: 15px;">Feel free to explore my work and reach out!</span><br><br>
  <a href="https://github.com/will51mps0n" style="font-size: 20px;">GitHub</a> •
  <a href="https://www.linkedin.com/in/adam-simpson-b6a3201a7/" style="font-size: 20px;">LinkedIn</a> •
  <a href="mailto:adwisi@umich.edu" style="font-size: 20px;">Email</a>
</p>



