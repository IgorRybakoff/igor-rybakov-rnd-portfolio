# AI Clean Layer

AI Clean Layer explores safer interaction between language models and external memory.

## Core idea

Knowledge should move through explicit states rather than entering trusted memory immediately:

1. raw input;
2. working knowledge;
3. validated knowledge.

A Knowledge Contract records provenance, validation status, uncertainty, and permitted use.

## Architecture direction

- separate working and validated vector collections;
- ingestion gates and provenance metadata;
- contradiction detection;
- controlled promotion of knowledge;
- auditable retrieval;
- local-model compatibility.

## Current status

Python-oriented architecture prototype. Future publication will include a minimal reproducible implementation, test fixtures, and measurable acceptance criteria.
