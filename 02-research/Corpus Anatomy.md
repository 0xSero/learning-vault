---
title: Corpus Anatomy
date: 2026-08-19
tags:
  - layer/research
  - corpus
  - data
aliases:
  - God research
  - The corpus
---

# Corpus Anatomy

> [!abstract] TL;DR
> The God research is three data layers with three different epistemic statuses: **5,393** Old-Testament sayings of God (heuristic), **2,029** red-letter sayings of Jesus (authoritative), and **604** sayings in which Jesus speaks about himself (curated judgment). This note is the port: every number, how it was made, the curation rules, and the known tensions. The raw data lives in [[Self Reference Catalog]] (the 604, full text) and in the live site / repo.

## Where it lives

| Artifact | Location |
|---|---|
| Live site | https://0xsero.github.io/bible-quotes-wiki/ |
| Repo | https://github.com/0xSero/bible-quotes-wiki |
| Local copy | `~/.local-studio/bible-quotes-wiki/` |
| Ported 604 | [[Self Reference Catalog]] |

## The three layers

| Layer | Count | Method | Status |
|---|---|---|---|
| God (OT) | 5,393 | Speaker-attribution heuristics on KJV | **Heuristic** — explicit frames, stated rules |
| Jesus (NT) | 2,029 | Red-letter KJV markup (NolanLT/kjv-bible) | **Authoritative** — standard corpus |
| Jesus about himself | 604 | Hand curation over the 2,029 | **Judgment** — rules stated, exclusions listed |

### The heuristic layer (OT)
The KJV carries no red-letter markup for divine speech, so a verse is included when the text explicitly attributes speech to God — frames like "God said," "the LORD spake … saying," "Thus saith the LORD," "saith the LORD," "Then answered the LORD." When an introducer frame opens a block of law or prophecy, the following verses are included as continued divine speech *until* a narrative break (a human actor speaking, or narration resuming); continued-speech verses carry a trailing arrow in the UI. This captures whole discourses: the Ten Commandments (Ex 20), the holiness code (Lev 19), God's two speeches to Job (Job 38–41).

Known limits (stated on the live page): in narrative-dialogue chapters (e.g. 1 Sam 3, the calling of Samuel) the line between the divine call and the human reply is thin, and a few reply clauses may be retained with the call; in Deuteronomy, where Moses retells the law, the boundary between Moses's mediation and God's direct word is deliberately left conservative.

### The authoritative layer (NT)
Every verse spoken by Jesus in the red-letter edition, across Matthew, Mark, Luke, John, Acts, 1 Corinthians, 2 Corinthians, Revelation. Nothing guessed. Excluded by construction: words *about* Jesus (Pilate, the guards), the narrator (John 3:16), the Spirit's speech. See [[Red Letter Bible]].

### The curated layer (604)
The selection rule: **Jesus is the speaker, and the content of the saying is about himself** — his person, identity, origin, nature, works, words, will, cup, hour, glory, kingdom, throne, body, blood, flesh, name, voice, coming, going, return, presence, and his relationship with the Father and the Spirit.

Included:
- First-person sayings whose subject is himself ("I am the way…"; "my words shall not pass away")
- Third-person self-reference — the ~69 "Son of man" sayings (see [[Son of Man]])
- Parabolic speeches where the first person is Jesus himself (the King of the final judgment who identifies with "the least of these," Matt 25:35–40; the returning Lord of the talents; "occupy till I come," Luke 19:13)
- Post-resurrection appearances (Acts 9, 22, 26) and the risen Christ's letters (Revelation)

Excluded (the judgment calls, stated):
- Speech of parable characters (the wicked tenants' lord, the father of the prodigal, the unjust steward, the friend at midnight, the servants, the two sons' father, the master of the feast)
- Quoted OT where the speaker of the quotation is God or David — e.g. "I am the God of Abraham…" (Matt 22:32), "The LORD said unto my Lord, sit thou on my right hand" (Matt 22:44), "I send my messenger" (Matt 11:10)
- Plain speech-act sentences whose subject is other people ("I tell you, you must be born again")
- Sayings *about* Jesus by other speakers — e.g. the guards in John 7:45 ("No man spake as this man spaketh") — this page is restricted to Jesus's own voice
- Non-Jesus speakers that the red-letter corpus includes (e.g. Pilate in John 18:34)

## The numbers, distributed

**OT divine speech (5,393) by section:**

| Section | Count | Share |
|---|---|---|
| Torah | 1,109 | 21% |
| History | 318 | 6% |
| Wisdom / Poetry | 742 | 14% |
| Major prophets | 2,611 | 48% |
| Minor prophets | 613 | 11% |

**Top OT books:** Jeremiah 1,030 · Ezekiel 792 · Isaiah 789 · Psalms 612 · Leviticus 387 · Numbers 381 · Exodus 158 · Zechariah 154.

> [!note] The prophetic dominance
> 60% of all divine speech in the corpus is prophetic. The thread is densest at the phase where God speaks *through* a human, stamped with the "I am the LORD" formula of the [[I Am Formula]] — 101 occurrences, 70 in the major prophets, **58 in Ezekiel alone**. This is the data skeleton of [[Thread of God]] phase 3.

**The 604 self-referencing sayings by book:**

| Book | Count | Share |
|---|---|---|
| Matthew | 122 | 20% |
| Mark | 60 | 10% |
| Luke | 108 | 18% |
| John | 263 | 44% |
| Acts | 17 | 3% |
| 1 Corinthians | 2 | — |
| 2 Corinthians | 1 | — |
| Revelation | 31 | 5% |

Of the 604, **82 contain "I am"** (the identity declarations, isolatable in the UI).

> [!note] The John dominance
> 44% of the self-referencing corpus is one gospel. The data confirms what scholarship says about John's high Christology: John is the book where the thread (phase 5) speaks most about itself.

## The verification story (why the numbers are trustworthy)

- The curation list is an explicit (book, chapter, verse) allowlist — 604 references, each checked against the source data at build time; a missing reference fails the build.
- The data files are parse-validated (the `.js` loads in a clean JS runtime; counts cross-checked against the source JSON).
- One real bug was caught during curation: the first-pass classifier lowercased text before checking for the word "I", so pure first-person sayings ("Verily I say unto you…") fell through to the wrong bucket and had to be re-scanned. The fix: run the "I" check on the original casing. Lesson: **when a classifier's output is a curation decision, audit the fall-throughs, not just the hits.**

## Known tensions (stated, not smoothed over)

1. **John 15:13** ("no man hath greater love than this, that a man lay down his life for his friends") is *off* the self-reference page (it's a general saying, not about himself) yet it is central to [[The Sacrifice Thread]]. The page's rule and the thread's logic don't perfectly align — the pages are *arguments*, and the exclusions should be read with the same care as the inclusions.
2. **Parable boundaries are judgment calls.** The master of the talents = the returning King (included); the master of the weeds = the owner of the world (excluded); the fig-tree owner (excluded as ambiguous). A different exegete could draw these lines differently, and the corpus would be a different ~50 verses.
3. **The heuristic layer is a high-coverage catalogue, not a theologically red-letter OT.** The live page says so in its methodology box; this note inherits the same limit.

## Go deeper

- [[Self Reference Catalog]] — the 604, full text, grouped by book (the ported data)
- [[The Corpus Method]] — the reusable method behind all three layers
- [[Thread of God]] — what the distribution *means*
- [[Source Index]] — the upstream repos and the KJV source

## Sources

- [NolanLT/kjv-bible](https://github.com/NolanLT/kjv-bible) (KJV with red-letter markup, public domain)
- [The God Research, live](https://0xsero.github.io/bible-quotes-wiki/)
- [The God Research, repo](https://github.com/0xSero/bible-quotes-wiki)
