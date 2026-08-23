# Grokking Lab

> This page is the stable portfolio entry point. The complete public v0.1.0 package now lives in the standalone repository.

[Open the Grokking Lab repository →](https://github.com/IgorRybakoff/grokking-lab)

## Research question

Can a compact Transformer first memorize a modular-addition training subset and only much later generalize to held-out examples?

## Public experimental release

The standalone repository provides:

- executable PyTorch training code for `(a + b) mod 113`;
- a deterministic smoke test suitable for CI;
- tests for configuration, data splitting, model behavior, artifact integrity, and checkpoint replay;
- a frozen 40,000-step experimental record with checksums and five replayable checkpoints;
- the measured training curve, event-detection output, diagnostics, and experiment report;
- explicit reproducibility guidance and known limitations.

## Measured checkpoint

| Field | Recorded value |
|---|---:|
| Model | Compact 1-layer Transformer |
| Seed | 42 |
| Training split | 0.3 |
| Training steps | 40,000 |
| Memorization | approximately step 200 |
| Delayed-generalization candidate | approximately step 25,600 |
| Stable plateau | approximately step 26,500 |
| Final train accuracy | 1.0000 |
| Final validation accuracy | 1.0000 |

This is one controlled experimental checkpoint. It is not evidence that grokking occurs for every seed, model, optimizer, or task.

## Research principle

**LLM never creates metrics; LLM only interprets measured evidence.**

The long run is published as frozen evidence. CI verifies the public code, deterministic setup, smoke training, checksums, and checkpoint replay; it does not pretend to reproduce the full 40,000-step run.

[Inspect the code, CI, evidence, and limitations →](https://github.com/IgorRybakoff/grokking-lab)
