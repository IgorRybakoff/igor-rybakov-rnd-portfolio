# Grokking Lab

Research environment for studying delayed generalization and phase transitions in small neural networks.

## Research principle

Metric generation is separated from interpretation:

1. a Python/PyTorch training core runs real experiments;
2. a deterministic phase watcher records thresholds and checkpoints;
3. a mechanistic analyzer computes SVD, FFT, cosine similarity, norms, and related measurements;
4. an LLM may interpret measured results but may not invent them;
5. a verifier checks claims against analyzer output.

## Current experiment

- task: modular arithmetic, such as `(a + b) mod p`;
- model: small embedding-based MLP;
- logged evidence: epoch, train/validation accuracy, loss, and weight norm;
- reproducibility: explicit seeds and checkpoint hashes.

## Current status

Experimental prototype. A smoke test reached full training accuracy but zero validation accuracy, correctly identifying memorization rather than grokking. Longer controlled runs and seed comparisons remain in progress.

Source code will be published after dependency, secret, and reproducibility checks.
