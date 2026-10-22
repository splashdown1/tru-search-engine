# TRU Sovereign Search Engine v2.0

**Air-gapped • Zero external dependencies • IndexedDB persistent**

Local knowledge index for the TRU offline network — the internet without internet.

## Role in the fleet

| Layer | Job |
|-------|-----|
| **Shelf** | Catalog of lanes |
| **Door** | Routes the ask to the right ship |
| **Search** | Indexes what you already hold |
| **Lanes** | Domain cards (Canonbound, Lifeline, …) |
| **Rules** | One file. A gap stays a gap. No call out. |

Search is listed on the [Shelf](https://github.com/splashdown1/tru-shelf) and routed by the [Door](https://github.com/splashdown1/tru-door).

## What’s in v2.0

- Structured seed (KJV core + TRU architecture) with book / tags
- BM25-lite + field boost + phrase bonus
- Persistent annotations (MY NOTES)
- Relationship graph (seed + user edges)
- Book and tag filters
- Import / export of docs + edges + notes
- Packs under `packs/` for offline expansion

## How to use

1. Open `index.html` (or the Pages URL once enabled).
2. Search, filter, add notes, follow related links.
3. **IMPORT** a pack (e.g. `packs/tru-network-pack.json` or `tru-seed-full.json`).
4. **EXPORT** moves the full working set between devices offline.

## GitHub Pages

Settings → Pages → Deploy from branch → `main` / root.  
`.nojekyll` is present. Target URL: https://splashdown1.github.io/tru-search-engine/

## Design constraints

- Zero network calls after the file is saved  
- Pure vanilla JS, single-file HTML  
- A gap stays a gap — no invention, no remote fallback  

---

**TRU** — Clarity toward salvation. Sovereign. Offline. Free.
