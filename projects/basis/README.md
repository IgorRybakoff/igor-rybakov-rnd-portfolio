# BASIS — Verified Intelligence & Multi-Model Arbitration

BASIS is an experimental verification and arbitration layer for multi-model reasoning. Its purpose is not to force consensus, but to preserve disagreement, connect conclusions to evidence, and make uncertainty explicit before a final answer is accepted.

## Core flow

```text
Question
  ↓
Independent / role-based model responses
  ↓
Claims + evidence extraction
  ↓
Agreement / contradiction analysis
  ↓
Structured decision state
  ↓
Optional HUMAN_REVIEW
  ↓
Auditable synthesis
```

## Decision states

- `AGREED` — material agreement on the supported conclusion;
- `PARTIAL` — only part of the conclusion is sufficiently supported;
- `SPLIT` — meaningful unresolved disagreement remains;
- `REJECTED` — the proposed conclusion is not adequately supported;
- `HUMAN_REVIEW` — uncertainty or risk requires explicit human judgment.

These states are decision metadata, not claims that a majority vote establishes truth.

## Prototype direction

- parallel or role-based model evaluation;
- normalization of claims, evidence, confidence, and rationale;
- contradiction and unsupported-claim detection;
- explicit preservation of model disagreement;
- structured confidence and evidence tracking;
- auditable final synthesis;
- optional stability validation by SEACS;
- prototype consensus API surface centered on `/consensus/ask`.

## Research principle

Model agreement and evidence quality are separate variables. BASIS is designed to expose both rather than collapse them into a single confidence score.

A useful result may therefore be an explicit `SPLIT` or `HUMAN_REVIEW`, rather than a superficially confident synthetic answer.

## Current status

R&D architecture and prototype. Structured consensus states and a verification-oriented API direction have been developed, but BASIS is not presented as an oracle, production truth engine, or independently validated safety system.

Its reliability depends on source quality, model diversity, calibration, task design, and transparent escalation when evidence is insufficient.
