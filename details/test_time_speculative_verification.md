# Test-Time Speculative Verification

Test-Time Speculative Verification optimizes the computational overhead associated with running massive reasoning models.

## How It Works
A lightweight, fast draft model generates candidate thinking traces, and a larger, highly accurate target model evaluates and verifies the entire block of tokens in a single parallelized forward pass.

```mermaid
graph TD
    A[Input Query] --> B[Draft Model generates speculative thoughts]
    B --> C[Target Model evaluates entire block in one pass]
    C --> D{Validate?}
    D -->|Accepted| E[Commit Tokens & Continue]
    D -->|Rejected| F[Target Model overrides & regenerates]
```

## Benefits
Significantly reduces serving latency and VRAM usage without sacrificing the quality of the final output.

[← Back to README](../README.md)
