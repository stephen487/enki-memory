# Enki Memory

**A memory your AI agents share, kept on your own computer.**

Tell Claude Code something on Monday; Cursor knows it on Tuesday. Enki Memory gives every AI agent you use one
shared, persistent memory. It runs locally, works offline, and your memories never leave your machine.

- **Works with** Claude Code, Claude Desktop, Cursor and Windsurf (connected automatically on install), and any
  other MCP agent by hand.
- **Your agent gets six tools:** `store`, `retrieve`, `update`, `discard`, `stats`, `export`.
- **Local and offline.** Everything runs on your PC, including the search model. No Python or other install needed.
- **Yours to keep.** Memories live in `%USERPROFILE%\.enki-memory`. Uninstalling removes the program and leaves
  your memories alone. Recall, forget and export keep working on every plan, even if Pro lapses.
- **Leaner memory.** In our June 2026 LongMemEval research runs, Enki's memory engine stored about half as
  much as mem0. Our full 500-question run is under way; results will be published, wins and losses.

### Install (Windows 11, 64-bit; Windows 10 should work but is not tested yet)
1. Download `EnkiMemory-Windows-*.zip` from **Releases** and unzip it.
2. Double-click **Install Enki Memory.cmd**. It finds your AI apps and asks before connecting each one.
3. Restart your AI app. Enki Memory appears in its tools.

> **Windows may warn you** the first time, because this preview is not code-signed yet. Signing is on its way.

Full guide: `README.md` inside the download.

### Plans
- **Free:** up to 500 facts. No account, no sign-up, no network.
- **Pro:** unlimited facts, £3.99/month or £39/year. Buy and manage it at https://enkilabs.co.uk/memory/

### Privacy
Your memories never leave your computer. A free install makes **no network connections at all**. With a Pro
licence, Enki Memory checks the date and renews the licence with our licence service, sending only the licence
and a random number, never your memories.

### Honest limits
- When you change a fact, have your agent use `update`. A reworded new fact does not always replace the old one
  on its own.
- `discard` hides a fact from recall and keeps an audit record; it does not scrub it from disk.

### Status
UK patent application filed (patent pending). The Enki engine is proprietary and closed-source: this repository
holds documentation and releases only.

Made by Enki Labs UK Ltd · https://enkilabs.co.uk
