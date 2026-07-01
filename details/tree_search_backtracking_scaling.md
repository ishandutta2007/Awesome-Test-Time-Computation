# Tree-Search & Backtracking Scaling

Tree-Search and Backtracking Scaling models text generation explicitly as a tree-traversal problem during decoding.

## How It Works
At each step, a generator model proposes multiple token pathways. A process-supervised value model (PRM) scores the viability of each branch. If a branch score drops below a threshold, the decoder backtracks to a previous checkpoint and explores an alternate branch.

```mermaid
graph TD
    A[Root Node] --> B[Branch 1: Score 0.9]
    A --> C[Branch 2: Score 0.3]
    B --> D[Branch 1.1: Score 0.8]
    B --> E[Branch 1.2: Score 0.2]
    E -->|Dead End| F[Backtrack to Branch 1]
    F --> D
```

## Key Algorithms
- Depth-First Search (DFS)
- Monte Carlo Tree Search (MCTS)
- A* Search

[← Back to README](../README.md)
