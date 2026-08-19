---
title: Progressive Disclosure
date: 2026-08-19
tags:
  - layer/primitives
  - meta
  - vault
---

# Progressive Disclosure

> [!abstract] TL;DR
> This vault is organized so that any topic can be read at the depth you need *right now*, without forcing you through everything. Every note is a disclosure level: TL;DR first, working body second, deeper links third, sources fourth. You research by following links one layer at a time — never skipping two. The whole structure is the method: **primitives → research → applied → sources.**

## The four layers

| Layer | Folder | Question it answers | Example |
|---|---|---|---|
| 1. Primitives | `01-primitives/` | What do the words mean? | [[Son of Man]], [[I Am Formula]], [[Typology]] |
| 2. Research | `02-research/` | What is the deep claim, and where is it weak? | [[Thread of God]], [[The Sacrifice Thread]], [[Corpus Anatomy]] |
| 3. Applied | `03-applied/` | What do I *do* with this? | [[Study Plan]], [[The Corpus Method]], [[The Adversary Method]] |
| 4. Sources | `04-sources/` | Where is the raw material to verify? | [[Self Reference Catalog]], [[Source Index]] |

## The disclosure protocol (per note)

1. **TL;DR** — one paragraph. If you stop here, you should be able to use the idea at 80%.
2. **Body** — the working level: claims, data, tables, the argument itself.
3. **Go deeper** — wikilinks to the next layer down. Each link says *why* to follow it.
4. **Sources** — external anchors: Wikipedia, the data repos, books. These are for verification, not for first reading.

> [!warning] The rule
> Never skip two layers. If a research note uses a word you don't know, drop to the primitive first. Skipping is how you get confident in a definition you never actually read.

## How to deep-research a topic (the loop)

1. Start at the **research** note for the topic (e.g. [[The Sacrifice Thread]]).
2. Read the TL;DR. If it matches your question, read the body.
3. Every word you don't know → follow to the **primitive**. Read it. Come back.
4. Every claim you want to verify → follow to the **source** (the catalog, the live site, the Wikipedia article).
5. Every "I want to *use* this" → follow to the **applied** note.
6. When you find something the vault doesn't cover, that gap is your next research target — note it in the relevant note's "Go deeper" section as an open link.

## Obsidian mechanics that make this work

- **Wikilinks** (`[[Note]]`) — internal links; Obsidian tracks renames automatically, so the web stays intact as the vault grows.
- **Unresolved links** — a `[[note that doesn't exist yet]]` is a *research TODO*. The graph view shows the gaps as orphan nodes.
- **Graph view** — the whole vault as a network. The primitives cluster on one side, research in the middle, applied and sources on the other. If the graph looks like a ball, the layers are leaking.
- **Search** (`Ctrl/Cmd+Shift+F`) — search the vault for a term (e.g. "substitute") to find every note that touches it, across layers.
- **Embeds** — `![[Note#Heading]]` pulls a section of another note inline, so a page can carry its own definitions without duplicating them.
- **Callouts** — `> [!abstract]`, `> [!warning]`, `> [!tip]` mark the disclosure levels visually.
- **Frontmatter tags** — every note carries `layer/...` tags, so you can filter the whole vault by layer.

## Why this shape

Deep research fails in two ways: it either stays shallow (you read summaries and stop) or it drowns (you read everything at once and retain nothing). Progressive disclosure is the middle path: **each layer is complete on its own, and each layer is a door to the next.** You are always at a level you can act on, and the depth is one click away.

## Go deeper

- [[The Corpus Method]] — the same principle applied to the data itself (authoritative layer vs heuristic layer vs curated layer)
- [[LEARNING|Home]] — the map

## Sources

- [Progressive disclosure — Wikipedia](https://en.wikipedia.org/wiki/Progressive_disclosure)
- [Obsidian: Links](https://help.obsidian.md/links)
- [Obsidian: Callouts](https://help.obsidian.md/callouts)
