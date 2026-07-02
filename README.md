# Enki — selective memory for AI agents

**Your AI forgets everything between chats. Enki remembers what matters — and forgets what's stale.**

Enki is a memory layer for LLM agents. It keeps the *current* answer and retires outdated values
**at write time, deterministically, on your machine** — no LLM in the loop deciding what to forget, so
no per-write cost or latency, and your data never leaves the box. Your agent recalls today's answer, not
every value ever mentioned, at about **half the storage**.

## ▶️ Try it live — no signup, runs local
### → **https://try.enkilabs.co.uk**
Type a fact, come back "the next day," and watch a standard AI forget while Enki remembers — then see the
same conversation stored at ~**0.49×** the footprint of keeping everything.

## Why it's different
Most agent memory either grows forever, or calls an LLM/graph on **every write** to decide what to update
or invalidate (mem0, Zep, Cognee, and Letta each do a version of this). Enki forgets **deterministically**
and **locally**:
- **Write-time supersede** — a newer value for the same thing retires the stale one automatically.
- **No per-write LLM tax** — no model call to forget: lower cost, lower latency.
- **Sovereign** — local embeddings, no API key, £0/call; the store is a plain file you can inspect.
- **Tunable footprint** — dial storage toward ~half.

Honest scope: recall is **comparable at full retrieval** — the edge is the *mechanism* (local +
deterministic + cheap) and the *efficiency*, not an accuracy-lead claim.
**[See the head-to-head LongMemEval results →](https://github.com/stephen487/enki-benchmarks)**

## Memory as agent tools (MCP)
Enki exposes a framework-agnostic memory surface over the Model Context Protocol — for Claude
Desktop/Code, Cursor, Windsurf, or any custom agent:

| Tool | What it does |
|------|--------------|
| `store` | Save a fact; a newer value auto-retires the stale one; exact duplicates ignored. |
| `retrieve` | Recall the current, relevant facts (superseded/discarded excluded). |
| `update` | Explicitly replace a fact (non-numeric changes). |
| `discard` | Forget a fact (mark-not-delete; retained for audit). |
| `stats` | Active vs superseded vs total. |

The MCP server is in **closed beta** while we package the engine as a closed distribution.
**Want early access?** Join the waitlist at **[try.enkilabs.co.uk](https://try.enkilabs.co.uk)** or open an issue here.

## Status
UK patent application filed (**patent pending**). The Enki engine is **proprietary and closed-source** —
this repository is documentation and links only; no engine source, configuration, or internals are published here.

---
*Enki Labs (UK) · 2026 · [try.enkilabs.co.uk](https://try.enkilabs.co.uk)*
