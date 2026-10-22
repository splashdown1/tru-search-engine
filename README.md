# TRU Sovereign Search Engine v2.0

**Air-gapped • Zero external dependencies • IndexedDB persistent**

Local **knowledge index** for the TRU offline network. It indexes what you load into it. It does not replace the domain lanes.

## What this is

- A single-file BM25 search UI over a **local** document set
- Structured seed: ~48 core KJV verses + TRU architecture cards
- Optional **packs** under `packs/` (network map, signal, water, storm bridges)
- Persistent notes and a lightweight relationship graph (IndexedDB)
- Import / export so the working set can move by hand between devices

## What this is not

| Need | Use instead |
|------|-------------|
| Full KJV + lexicon / cross-refs | [Canonbound](https://github.com/splashdown1/tru-canonbound) |
| FM 21-76 / FM 21-11 survival & first aid | [Lifeline](https://github.com/splashdown1/tru-lifeline) |
| Full distress / Morse / panel engine | [Signal](https://github.com/splashdown1/tru-signal) |
| EPA dose UI as its own card | [Water](https://github.com/splashdown1/tru-water) |
| Routing “which ship holds this ask?” | [Door](https://github.com/splashdown1/tru-door) |
| Catalog of all lanes | [Shelf](https://github.com/splashdown1/tru-shelf) |

Packs may **point at** those lanes or carry short sourced cards. They are not the full engines.

## Role in the fleet

| Layer | Job |
|-------|-----|
| **Shelf** | Catalog of lanes |
| **Door** | Routes the ask to the right ship |
| **Search** | Indexes what *you* hold locally |
| **Lanes** | Domain cards (Canonbound, Lifeline, …) |
| **Rules** | One file. A gap stays a gap. No call out. |

Live: https://splashdown1.github.io/tru-search-engine/

## How to use

1. Open `index.html` or the Pages URL.
2. Search the embedded seed; filter by book/tag; add notes; follow related edges.
3. **IMPORT** a pack from `packs/` (paste JSON) to expand the local index.
4. **EXPORT** to move docs + edges + notes offline.

## Packs

| Pack | Contents |
|------|----------|
| `tru-network-pack.json` | Rules + Shelf/Door/Search map |
| `tru-signal-pack.json` | Sourced distress/panel cards (full engine remains Signal) |
| `tru-water-pack.json` | EPA-aligned disinfection notes (full engine remains Water) |
| `tru-storm-pack.json` | Bridges to Lifeline and storm lanes — not medical advice |
| `tru-seed-full.json` | Larger structured seed for import |

## GitHub Pages

**Live source today:** branch **`gh-pages`**, root (`/`).  
URL: https://splashdown1.github.io/tru-search-engine/

`.nojekyll` is on the repo. A workflow at `.github/workflows/pages.yml` can deploy from `main` if you switch Pages → **GitHub Actions** and re-run the workflow; until then, keep **`gh-pages`** in sync when content changes.

## Design constraints

- Zero network calls after the file is saved
- Pure vanilla JS, single-file HTML
- A gap stays a gap — no invention, no remote fallback

---

**TRU** — Clarity toward salvation. Sovereign. Offline. Free.
