# podme

Makes spoken-word video searchable and verifiable. Every claim it shows links to the exact second it was spoken.

> **Status:** personal project and the technical base of my master's thesis at TU Wien. The source code is private. This repository contains the README and the architecture write-up only.

## What it does

- A **library** of saved transcripts and an **editor** that shows one transcript with annotations in the margin.
- A **Chrome extension** that adds a small corner panel to any page with a video it can read a transcript for: YouTube, Vimeo, embedded players, HTML5 tracks, Opencast (for example university lecture portals) and captured captions.
- Four actions: add a transcript, ask a question, add context, fact-check a claim.
- Answers are summaries with quotes, and each quote is linked to the exact timestamp.
- Fact checks run through the same four-level cascade as Unbias (separate repository), and every verdict carries its sources.

Target users: journalists and analysts who need to verify what a specific person said.

## Research angle

The thesis asks whether the quotes in a retrieval-augmented answer really support its claims:

*Beyond Chunk-Level Citations: Temporal Span Grounding and Cross-Source Consistency in Spoken-Word RAG* (TU Wien, in progress).

## Stack

Python, FastAPI, PostgreSQL with pgvector, Sentence Transformers, Claude API, React, Chrome extension.

## Documentation

- [ARCHITECTURE.md](ARCHITECTURE.md): ingestion, retrieval, quote anchoring, clients.

## License

All rights reserved. No source code is published here.
