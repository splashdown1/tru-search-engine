# TRU Sovereign Search Engine v2.0

**Air-gapped • Zero external dependencies • IndexedDB persistent**

Local-first structured knowledge search for the TRU core.

## What’s in v2.0

### 1. Structured KJV core
- ~119 high-value verses with full metadata: `book`, `chapter`, `verse`, `reference`, `text`, `tags`
- Books covered: Genesis, Exodus, Deuteronomy, Joshua, Psalms, Proverbs, Isaiah, Jeremiah, Micah, Matthew, John, Romans, 1–2 Corinthians, Galatians, Ephesians, Philippians, Colossians, 2 Timothy, Hebrews, James, 1 Peter, 1 John, Revelation
- Book and tag filters in the UI
- Full KJV (or any corpus) can still be brought in via **IMPORT** — stays local

### 2. Persistent annotations
- Add / edit / delete personal notes on any node
- Notes live only in IndexedDB on the device
- **MY NOTES** panel lists everything you’ve written
- Notes travel with **EXPORT** / **IMPORT**

### 3. Lightweight relationship graph
- Directed edges with optional labels (seed cross-references included)
- Related nodes shown under each result
- Click a related reference to jump
- **GRAPH** panel: view, add, or delete edges locally

### 4. Ranking & search
- BM25-lite + field boost (reference/title) + tag tokens + phrase/order bonus
- Debounced input, clear button, `/` focuses search, Escape clears
- One-tap COPY on every result

### 5. Import / Export
- Export full working set: docs + edges + notes
- Import accepts either a plain document array or a full export object
- Everything remains air-gapped

## Design constraints (unchanged)

- Zero network calls  
- Zero remote assets / CDNs  
- Pure vanilla JavaScript, single-file HTML  
- A gap stays a gap — no invention, no remote fallback  

## How to use

1. Open `index.html` in any modern browser.
2. Index builds or loads from IndexedDB automatically.
3. Search, filter by book/tag, add notes, explore related nodes.
4. **REBUILD** forces a fresh index from seed + imports.
5. **EXPORT** / **IMPORT** move knowledge between devices offline.

## Next natural expansions

- Larger structured KJV packs (importable JSON bundles by book)
- Optional local vector / embedding layer if a tiny offline path is proven
- GitHub Pages preview + one-file distribution packaging
- Deeper TRU lane integration (Shelf, Door, Rules, etc.)

---

**TRU** — Clarity toward salvation. Sovereign. Offline. Free.
