# SRX — Semantic Reconstructive eXchange

SRX is an experimental open-source reconstructive engine for evolving structured data.

It explores whether some version transitions can be represented as compact, reversible structural explanations while preserving exact target bytes and falling back to conventional representations when structural encoding is not cheaper.

> **Ask the history. Prove the answer.**

## Research focus

- deterministic structural reconstruction;
- exact byte-level recovery with SHA-256 verification;
- adaptive structural-vs-conventional representation selection;
- temporal indexing and version intelligence;
- file-level selective historical reconstruction;
- verified evidence resolution from exact historical sources.

## Public v0.1 status

SRX has a public experimental release with:

- Python core and CLI;
- Temporal / Evidence Python layer;
- local-folder and local-Git connectors;
- reproducible frozen benchmarks;
- documented trust model and known limitations;
- GitHub Actions CI on Python 3.10 and 3.13.

Release gate:

- 55 unit/integration tests — PASS;
- frozen corpus SHA-256 verification — PASS;
- frozen benchmark regression — PASS;
- exact reconstruction — PASS.

Measured frozen benchmark results:

| Corpus | Conventional | SRX adaptive | Structural selected | Exact restore |
|---|---:|---:|---:|---|
| DevInit | 1638 B | 1638 B | 0/5 | PASS |
| Vite | 2952 B | 2919 B | 4/9 | PASS |

These results are compatibility measurements, not a claim of universal superiority.

## Links

- [Public repository](https://github.com/IgorRybakoff/srx)
- [Release v0.1.0](https://github.com/IgorRybakoff/srx/releases/tag/v0.1.0)
- [Trust model](https://github.com/IgorRybakoff/srx/blob/main/TRUST_MODEL.md)
- [Known limitations](https://github.com/IgorRybakoff/srx/blob/main/KNOWN_LIMITATIONS.md)

## Current status

**Public experimental release.** The deterministic core, Temporal/Evidence layer, benchmark gate, and CI are published. Persistent Temporal CLI, stronger rename identity, repeated-array optimization, and stronger authenticity mechanisms remain future work.
