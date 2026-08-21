# Grokking Lab

Research environment for studying delayed generalization, phase transitions, and mechanistic changes in small neural networks.

## Research principle

Measured evidence is separated from interpretation:

1. a Python/PyTorch training core runs the experiment;
2. deterministic logging records losses, accuracies, norms, thresholds, and checkpoints;
3. mechanistic analysis can examine SVD, FFT, cosine similarity, norms, and related signals;
4. an LLM may interpret measured results but may not create experimental metrics;
5. claims are checked against recorded artifacts and replayable checkpoints.

## Current implementation

- task family: modular arithmetic, including `(a + b) mod p`;
- model family: compact transformer-style architectures;
- optimizer and training parameters are explicit and reproducible;
- provenance controls distinguish real PyTorch execution from simulated or generated metrics;
- checkpoint replay and frozen experiment artifacts are used to verify reported outcomes.

## Measured checkpoint

A controlled long run on modular addition with `p=113` and a compact one-layer transformer reached:

- training accuracy: **1.0000**;
- validation accuracy: **1.0000**;
- delayed generalization onset around **25.6k training steps**;
- stable high validation performance after the transition;
- final exact experiment artifacts preserved for replay and audit.

This is a reproducible experimental checkpoint, not a claim that grokking is universal across architectures, seeds, or datasets.

## Current status

Experimental R&D prototype with confirmed delayed-generalization behavior in a controlled PyTorch run. Ongoing work focuses on stronger multi-seed replication, mechanistic analysis around the transition, and cleaner public packaging of reproducible artifacts.
