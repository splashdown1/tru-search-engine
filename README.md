# TRU Sovereign Search Engine v1.3

**Air-gapped • Zero external dependencies • IndexedDB persistent**

Local-first hybrid search engine for the TRU knowledge core.

## What changed in v1.3

- **Field boosting** — reference/title terms count double in the index
- **Phrase / order bonus** — consecutive query terms and full ordered coverage lift rank
- **Expanded seed** — ~45 core KJV verses + richer TRU architecture nodes
- **Local import / export** — paste JSON documents; export the working set; everything stays offline
- **Better UX** — clear button, result count, one-tap COPY, `/` focuses search, Escape clears
- **Stronger stats** — nodes, term count, build time, import delta
- **Safer rendering** — HTML escaping on all user-facing text
- **Dataset versioning** still forces rebuild on mismatch

## Features

- Fully self-contained single-file HTML
- Pure vanilla JavaScript (no frameworks, no CDNs)
- Real IndexedDB persistence of the inverted index + user imports
- BM25-lite scoring with length normalization, IDF, field boost, phrase bonus
- Debounced input for mobile smoothness
- Clear air-gapped status indicators
- Force-rebuild control

## How to use

1. Open `index.html` in any modern browser (or iOS HTML viewer).
2. The index builds (or loads from IndexedDB) automatically.
3. Type to search. Results rank by local BM25-lite + phrase score.
4. **REBUILD** forces a fresh index from seed + any stored imports.
5. **EXPORT** downloads the current working dataset as JSON.
6. **IMPORT** accepts a JSON array of `{ id, reference, text }` objects (local only).

## Design Constraints

- Zero network calls
- Zero remote assets
- Works offline after first load
- A gap stays a gap — no invention, no remote fallback

## Status

Hardened foundation layer. Natural next expansions:

- Full structured KJV injection (book/chapter aware)
- Persistent annotations / personal notes per node
- Lightweight relationship graph between verses and TRU nodes
- Optional local vector layer if a tiny embedding path is ever added offline

---

**TRU** — Clarity toward salvation. Sovereign. Offline. Free.
