---
layout: default
title: AlphaZero-Based Othello AI
github_url: https://github.com/will51mps0n/tsp

---

[← Back to Home](../index.html)

# AlphaZero-Based Othello AI  
*December 2024*

---

## Overview

This project implements an **AlphaZero-inspired Othello agent** using **Monte Carlo Tree Search (MCTS)** guided by a deep neural network, written entirely in Python with PyTorch.

Key highlights of the implementation include:

1. **Monte Carlo Tree Search (MCTS):**
   - Implements all core phases of MCTS:
     - **Selection:** Chooses actions based on Upper Confidence Bound (UCB) criteria.
     - **Expansion:** Adds new states to the tree.
     - **Simulation:** Uses the neural network to predict game outcomes instead of rollouts.
     - **Backpropagation:** Updates Q-values, visit counts, and propagates rewards up the tree.
   - Handles terminal game states and reward flipping logic as per AlphaZero principles.

2. **Neural Network Integration:**
   - Uses a convolutional neural network to predict move policies and board evaluations.
   - Trained iteratively using self-play data generated from MCTS.

3. **Self-Play and Learning Loop:**
   - Employs a Coach class to manage training iterations, self-play episodes, model evaluation, and updating policies.
   - Compares new models against older versions to retain only stronger agents.

---

## Features

- **AlphaZero Framework for Othello:**
  - Custom implementation of MCTS tightly integrated with a neural network evaluator.
  - Focuses on efficient exploration, data efficiency, and deep reinforcement learning strategies.

- **Detailed MCTS Components:**

  | Phase           | Description                                                                 |
  |----------------|-----------------------------------------------------------------------------|
  | **Selection**    | Traverses the game tree, selecting actions based on UCB formula.            |
  | **Expansion**    | Adds new unexplored states to the tree.                                     |
  | **Simulation**   | Uses neural network predictions for state evaluation instead of rollouts.   |
  | **Backpropagation** | Updates action values and visit counts, propagating rewards upwards.     |

- **Training Loop:**
  - Runs multiple self-play episodes to gather data.
  - Trains the neural network based on gameplay history.
  - Evaluates and updates models based on performance against prior versions.

- **Hyperparameter Customization:**
  - Adjustable values for number of MCTS simulations, training episodes, and comparison games to experiment with training efficiency and model performance.

- **Visualization:**
  - Displays Othello board states and tracks actions taken by the agent during MCTS for debugging and analysis.

---

## Technologies

- python
- pytorch
- CNNs
- Deep Reinforcement Learning

---

## Repository
[View Code on GitHub]()

---

[← Back to Home](../index.html)