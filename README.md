# TRU Sovereign Search Engine v1.2

**Air-gapped • Zero external dependencies • IndexedDB persistent**

Local-first hybrid search engine for the TRU knowledge core.

## Features

- Fully self-contained single-file HTML
- Pure vanilla JavaScript (no frameworks, no CDNs)
- Real IndexedDB persistence of the inverted index
- Dataset versioning with automatic rebuild on mismatch
- BM25-lite scoring (length-normalized, IDF-weighted)
- Debounced input for mobile smoothness
- Expanded seed: core KJV verses + TRU architecture nodes
- Clear air-gapped status indicators
- Force-rebuild control for development

## How to use

1. Open `index.html` in any modern browser (or iOS HTML viewer).
2. The index builds (or loads from IndexedDB) automatically.
3. Type to search. Results rank by local BM25-lite score.
4. Use **REBUILD** to force a fresh index build.

## Design Constraints

- Zero network calls
- Zero remote assets
- Works offline after first load
- Designed for progressive expansion of the local dataset

## Status

This is a hardened foundation layer. Next natural expansions:

- Full KJV structured injection
- Persistent conversational / annotation memory
- Lightweight relationship graph
- Export / import of the entire local knowledge base

---

**TRU** — Clarity toward salvation. Sovereign. Offline. Free.
