---
title: Source Index
date: 2026-08-19
layer: sources
tags:
  - layer/sources
  - references
---

# Source Index

> [!abstract] TL;DR
> Every external anchor this vault leans on, annotated with what it's for. The rule of the vault: a claim is only as good as the anchor you can follow in thirty seconds. These are the anchors. Grouped: **data** (the corpus itself), **Wikipedia** (the padding layer), **books** (the scholarly depth), and **tools** (the infrastructure).

## Data (the corpus)

| Source | What it is | Used by |
|---|---|---|
| [The God Research, live site](https://0xsero.github.io/bible-quotes-wiki/) | The full wiki: 5,393 God sayings + 2,029 Jesus sayings + the 604 self-reference page, with filters | Everything |
| [The God Research, repo](https://github.com/0xSero/bible-quotes-wiki) | The static site + data files + build script | [[Corpus Anatomy]] |
| [[Self Reference Catalog]] | The 604 sayings, ported into this vault, full text | [[Study Plan]], [[Devotional Threads]] |
| [NolanLT/kjv-bible](https://github.com/NolanLT/kjv-bible) | KJV (public domain) with red-letter markup — the upstream data source | [[Red Letter Bible]] |
| [Bible Gateway (KJV)](https://www.biblegateway.com) | Per-verse context links (every catalog entry links here) | All notes |

## Wikipedia (the padding layer)

Annotated by which note uses them:

**Identity and the thread**
- [Son of man](https://en.wikipedia.org/wiki/Son_of_man) — [[Son of Man]]
- [Son of God](https://en.wikipedia.org/wiki/Son_of_God) — [[Son of Man]]
- [I AM (theology)](https://en.wikipedia.org/wiki/I_AM_(theology)) — [[I Am Formula]]
- [I am the LORD](https://en.wikipedia.org/wiki/I_am_the_LORD) — [[I Am Formula]], [[Corpus Anatomy]]
- [Progressive revelation](https://en.wikipedia.org/wiki/Progressive_revelation) — [[Thread of God]]
- [Theophany](https://en.wikipedia.org/wiki/Theophany) · [Christophany](https://en.wikipedia.org/wiki/Christophany) · [Shekhinah](https://en.wikipedia.org/wiki/Shekhinah) — [[Theophany]]
- [Interbiblical period](https://en.wikipedia.org/wiki/Interbiblical_period) — [[Thread of God]] (phase 4, the silence)
- [Incarnation (Christianity)](https://en.wikipedia.org/wiki/Incarnation_(Christianity)) — [[Thread of God]] (phase 5)
- [Consummation](https://en.wikipedia.org/wiki/Consummation) — [[Thread of God]] (phase 8)
- [Red letter Bible](https://en.wikipedia.org/wiki/Red_letter_Bible) · [The Holy Bible in the Words of Christ](https://en.wikipedia.org/wiki/The_Holy_Bible_in_the_Words_of_Christ) — [[Red Letter Bible]]

**The sacrifice thread**
- [Binding of Isaac](https://en.wikipedia.org/wiki/Binding_of_Isaac) — [[The Sacrifice Thread]]
- [Passover](https://en.wikipedia.org/wiki/Passover) — [[The Sacrifice Thread]]
- [Sacrifice (Christianity)](https://en.wikipedia.org/wiki/Sacrifice_(Christianity)) · [Atonement](https://en.wikipedia.org/wiki/Atonement) — [[The Sacrifice Thread]]
- [Typology (theology)](https://en.wikipedia.org/wiki/Typology_(theology)) · [Typology in early Christianity](https://en.wikipedia.org/wiki/Typology_in_early_Christianity) — [[Typology]]
- [Eucharist](https://en.wikipedia.org/wiki/Eucharist) — [[The Sacrifice Thread]]

**Methodism**
- [Methodism](https://en.wikipedia.org/wiki/Methodism) · [John Wesley](https://en.wikipedia.org/wiki/John_Wesley) · [Aldersgate](https://en.wikipedia.org/wiki/Aldersgate) — [[Methodism]]
- [Prevenient grace](https://en.wikipedia.org/wiki/Prevenient_grace) · [Entire sanctification](https://en.wikipedia.org/wiki/Entire_sanctification) — [[Methodism]]
- [United Methodist Church](https://en.wikipedia.org/wiki/United_Methodist_Church) · [World Methodist Council](https://en.wikipedia.org/wiki/World_Methodist_Council) — [[Methodism]]

**Method and numbers**
- [Kairos](https://en.wikipedia.org/wiki/Kairos) · [Chronos](https://en.wikipedia.org/wiki/Chronos) · [Second (time)](https://en.wikipedia.org/wiki/Second) — [[Two Times]]
- [Gematria](https://en.wikipedia.org/wiki/Gematria) · [Numerology](https://en.wikipedia.org/wiki/Numerology) — [[The 23-Second Probe]]
- [Progressive disclosure](https://en.wikipedia.org/wiki/Progressive_disclosure) — [[Progressive Disclosure]]
- [Daniel 7](https://en.wikipedia.org/wiki/Daniel_7) · [Targum](https://en.wikipedia.org/wiki/Targum) — [[Son of Man]]

## Books (the scholarly depth)

Not linked (no stable free URL), cited for verification:

- **John P. Meier, *A Marginal Jew* vol. I** — the standard scholarly treatment of the son-of-man sayings. For the authenticity claim in [[Son of Man]].
- **E. P. Sanders, *Jesus and Judaism*** — the historical Jesus in his Jewish context; the Deut 18 "prophet like Moses" material in [[John 8:40]].
- **Craig S. Keener, *The Gospel of John: A Commentary*** — verse-by-verse on John; the bread discourse and the High Priestly Prayer.
- **Walter Kaiser, *The Progress of Redemption*** — the classic treatment of the thread-of-revelation arc; the backbone of [[Thread of God]].
- **Hebrews 11:19** — "in a figure" (*en typos*); the typology term of art. See [[Typology]].

## Tools (the infrastructure)

| Tool | What it is |
|---|---|
| [Obsidian](https://obsidian.md) | The app this vault runs in |
| [kepano/obsidian-skills](https://github.com/kepano/obsidian-skills) | The skills set in `skills/` — the markdown conventions (wikilinks, callouts, properties, embeds) this vault follows |
| [Obsidian Flavored Markdown docs](https://help.obsidian.md/obsidian-flavored-markdown) | The syntax reference |
| [JSON Canvas](https://jsoncanvas.org/) | For future map-of-content canvases if the vault outgrows the list-based [[Progressive Disclosure]] |

> [!tip] The anchor rule
> If a note in this vault cites a claim that isn't in the data layer ([[Corpus Anatomy]], [[Self Reference Catalog]]) and isn't in the Wikipedia layer above, the claim is a float. Add the anchor or mark the claim as unverified.
