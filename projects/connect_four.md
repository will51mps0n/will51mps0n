---
layout: default
title: Connect Four AI
github_url: https://github.com/will51mps0n/connect_four_ai
---

[← Back to Home](../index.html)

# Connect Four AI: Minimax with Alpha-Beta Pruning
*November 2024*

---
# Overview

This project implements an intelligent AI agent that plays **Connect Four** using the Minimax algorithm enhanced with **Alpha-Beta Pruning**. The AI evaluates the board state and makes optimal moves to maximize its chance of winning while minimizing the human player's chances.

## Features
- Minimax search algorithm with depth control
- Alpha-Beta pruning for efficiency
- Heuristic evaluation function considering:
  - Center column advantage
  - Horizontal, vertical, and diagonal scoring windows
- Pygame-based UI for interactive gameplay
- Test cases demonstrating AI wins in specific scenarios

## How It Works
The AI agent simulates future moves using a recursive minimax approach:
- Maximizes its score when it's the AI's turn.
- Minimizes the score when it's the opponent's turn.
- Uses Alpha-Beta pruning to cut unnecessary branches, improving performance.

### Example Tests:
| Test # | Human Moves (Columns) | AI Move to Win | Winning Combo |
|-------|----------------------|--------------|----------------------------|
| 0     | 4, 3, 4, 2            | 4            | Positive diagonal (cols 1–4) |
| 1     | 6, 1                  | 2            | Negative diagonal (cols 1–4) |
| 2     | 4, 4, 1, 0            | 4            | Positive diagonal (cols 1–4) |
| 3     | 5, 6                  | 2            | Negative diagonal (cols 3–6) |

## Technologies
- Python
- NumPy
- Pygame

---

## Repository
[View Code on GitHub](https://github.com/will51mps0n/connect_four_ai)

---

[← Back to Home](../index.html)