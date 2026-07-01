# The Compute Allocation Scaling Law

The Compute Allocation Scaling Law (or Thinking Token Budgets) describes how test-time compute scales accuracy predictably during inference.

## How It Works
Similar to pre-training scaling laws, downstream reasoning accuracy scales as a power-law function of the absolute number of thinking tokens generated at inference time. By increasing the thinking token budget, performance on difficult tasks improves.

```mermaid
graph LR
    A[Low Difficulty Task] --> B[100 Thinking Tokens]
    C[High Difficulty Task] --> D[10,000+ Thinking Tokens]
    B --> E[High Accuracy]
    D --> F[High Accuracy]
```

## Significance
Allows models to solve highly complex problems (such as Math Olympiad questions) without modifying the base weights, simply by adjusting the inference runtime compute budget.

[← Back to README](../README.md)
