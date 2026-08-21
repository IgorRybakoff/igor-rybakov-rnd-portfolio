# AI Clean Layer — Validated Memory Boundary

AI Clean Layer explores a safer boundary between language models and persistent external memory. The central idea is simple: information should not become trusted memory merely because a model produced or retrieved it.

## Knowledge lifecycle

```text
Raw input
   ↓
Working knowledge
   ↓
Validation / contradiction checks
   ↓
Garbage Gate
   ↓
Validated knowledge
   ↓
Controlled retrieval into model context
```

Knowledge therefore moves through explicit states rather than entering persistent trusted memory immediately.

## Knowledge Contract

A knowledge item can carry structured metadata such as:

- source / provenance;
- validation status;
- confidence;
- freshness;
- FACT vs HYPOTHESIS distinction;
- permitted use and escalation requirements.

The contract is intended to make retrieval policy inspectable rather than implicit.

## Prototype direction

- Python / FastAPI-oriented pipeline;
- separation of working and validated vector collections;
- validated-only retrieval for trusted context;
- prototype use of a dedicated validated store (`kb_validated`);
- ingestion gates and provenance metadata;
- contradiction detection before promotion;
- a **Garbage Gate** that blocks unverified information from trusted persistent memory;
- controlled promotion from working to validated knowledge;
- structured outputs such as Verdict / Source / Confidence / Next Step;
- compatibility with local-model workflows.

## Research principle

Retrieval quality is not only a search problem; it is also a trust-state problem.

AI Clean Layer therefore separates:

**what the system has seen** from **what the system is allowed to treat as validated knowledge**.

## Current status

Validated-memory architecture prototype. A local Python-oriented implementation direction has explored gated ingestion and validated-only retrieval, but the project is not presented as a production security boundary or independently validated safety system.

Future public work should focus on a minimal reproducible implementation, adversarial test fixtures, measurable promotion/rejection criteria, and explicit provenance guarantees.
