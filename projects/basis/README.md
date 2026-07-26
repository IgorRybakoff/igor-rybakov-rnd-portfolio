# BASIS — Verified Intelligence

BASIS is a proposed consensus and verification layer for multi-model reasoning.

## Purpose

Instead of hiding disagreement between models, BASIS records it explicitly and separates supported conclusions from unresolved uncertainty.

## Decision states

- `AGREED`
- `PARTIAL`
- `SPLIT`
- `REJECTED`
- `HUMAN_REVIEW`

## Architecture direction

- parallel or role-based model responses;
- evidence and contradiction extraction;
- structured uncertainty;
- confidence calibration;
- optional stability validation by SEACS;
- auditable final synthesis.

## Current status

Architecture and prototype direction. BASIS is not presented as an oracle or a guarantee of truth; its value depends on evidence quality, model diversity, calibration, and transparent escalation to human review.
