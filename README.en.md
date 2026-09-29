**繁體中文** ([README.md](README.md)) | **English** | [简体中文](README.zh-CN.md)

# Klingon

**A single-file cognition & output system.** One `index.html`, your browser, your data — no build step, no framework, no backend, no account.

## Screenshots

| Morning Notebook | Night Notebook |
|:---:|:---:|
| ![Morning notebook](docs/morning.png) | ![Night notebook](docs/night.png) |

*Monthly notebooks: a 30-day life grid, per-day ledgers, and print-ready A4 PDF output.*

## Background

Klingon is built around the **D1 → D3 → D7 output method** (inspired by Shion Kabasawa's memory books): an idea is captured as a one-line intuition on **Day 1**, transformed into written reflection on **Day 3**, and distilled into practice on **Day 7**. A gentle 7-day loop, morning dopamine focus, and a night review close the circle; at each month's end everything settles into a printed notebook.

It is also an experiment in **"less is more" software**: no colors louder than one teal accent, no emoji, no modals stacked on modals — just warm paper, serif type, and small sounds. It was designed to be the kind of tool a person can actually use every day, which means it never scolds you for missing a day (the "grace period" rule).

## Features

- **Morning Focus** — up to 3 tasks with a rising-sun badge that fills as you check them off; drag & drop ordering; last night's "one small step" appears as a ghost placeholder you can adopt with Tab.
- **Output Tracker** — magazine-style cards with punched-ticket stubs (STUB 01 → STUB 02 → STUB 03), red PUNCHED stamps on each completed stage, and a frameless writing drawer that preserves every line break.
- **Night Review** — today's traces aggregated into a light accordion, three-line micro reflection with instant autosave, 4-7-8 breathing rhythm, and a synthesized singing bowl when you turn off the light.
- **Monthly Notebooks** — a 30-day life grid with a rhythm-completion rate; morning & night ledgers; print-ready A4 PDF with a binding margin, where a day's content never splits across pages.
- **Spotlight** — `Ctrl / ⌘ + K` to search everything you've ever written.
- **Multi-window safe storage** — merge-on-save across windows; deletion tombstones so deleted items never resurrect; order-is-data semantics; rotating timestamped backups (up to 20 restore points); snapshot rescue plus a history panel to browse and restore any past state.
- **Local file persistence** — optionally grant access to a folder and every save also writes a plain `klingon-data.json` you can see in Explorer; if browser storage is ever cleared, the app restores itself from that file on next launch.
- **Export** — share cards in Paper White / Obsidian Dark (copy or download as PNG), plus whole-archive JSON backup / restore.

## Design rules

- Zero colored emoji — every icon is a 1.5px monochrome geometric SVG.
- English-only category labels: **All · Book · Movie · Show · Podcast · Life**.
- Long-form text always preserves paragraph structure: `pre-wrap`, Georgia serif, 1.8 line height.
- No closed focus frames on writing surfaces — underline only.
- Warm paper palette: `#FBFAF4` paper · `#F8F7F0` sidebar · `#E6E2D4` ecru · `#20808D` teal accent.

## Run

1. Download `index.html`
2. Double-click it (Chrome or Edge recommended)
3. That's it.

Optional: click 啟用本地存檔 in the sidebar to mirror every save to a folder of your choice.

## Data & privacy

Everything lives in your browser's localStorage (key `klingon.v1`) plus, optionally, a JSON file in a folder you choose. **Nothing is ever uploaded anywhere.** The only network request the page makes is loading the optional html2canvas library from a CDN — every feature, including image export, works offline with the built-in canvas engine.

## License

[MIT](LICENSE) © suzie — free to use, modify, and build upon. Attribution appreciated.
