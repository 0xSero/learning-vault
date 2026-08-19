---
title: The Corpus Method
date: 2026-08-19
tags:
  - layer/applied
  - method
  - data
---

# The Corpus Method

> [!abstract] TL;DR
> The reusable method behind the God research: **define the claim → find the data → separate authoritative from heuristic → extract with stated rules → curate with stated exclusions → verify → publish with per-item context links.** The method's core discipline is epistemic layering: every number in the output carries a label for how it was made, and no layer's status is allowed to bleed into another.

## The six steps

### 1. Define the claim precisely
"Not quotes from the Bible" but: *every verse in which the KJV attributes direct speech to God (OT) or to Jesus (NT).* The claim's precision determines everything downstream. A vague claim produces a blob; a precise claim produces a corpus.

### 2. Find the data with the right status
- **Jesus (NT):** a red-letter KJV edition (NolanLT/kjv-bible) — the speaker attribution is already made by the edition's editors. **Authoritative.** Nothing is guessed.
- **God (OT):** the KJV has no red-letter markup for divine speech. There is no authoritative source, so the option is a **heuristic with explicit rules** — and the rules are printed on the page, not hidden in the code.

> [!warning] The discipline
> If a layer has no authoritative source, the heuristic's rules must be as visible as the data. A hidden heuristic is an uncheckable number.

### 3. Extract with stated rules
OT extraction rules (as printed on the live page):
- Include a verse when the text explicitly attributes speech to God: "God said," "the LORD spake … saying," "Thus saith the LORD," "saith the LORD," "Then answered the LORD."
- When an introducer frame ("…saying," "…and said,") opens a block of law or prophecy, continue including until a **narrative break** (a human actor speaking, or narration resuming).
- Mark continued-speech verses with a trailing arrow so the reader sees which verses are the frame and which are the continuation.

### 4. Curate with stated exclusions
The 604 self-reference layer is a curation judgment. The rule is printed; the exclusions are printed; the known tensions (John 15:13, parable boundaries) are printed too. A curated layer that hides its exclusions is an argument without its counter-arguments.

### 5. Verify
- The curation list is an explicit (book, chapter, verse) allowlist; every reference is checked against the source data at build time; a missing reference **fails the build**.
- The data files are parse-validated in a clean runtime; counts are cross-checked against the source.
- **Audit the fall-throughs, not just the hits.** The real bug of the session: the first-pass classifier lowercased text before checking for the word "I", so pure first-person sayings fell through to the wrong bucket and had to be re-scanned. The lesson generalizes: when a classifier's output is a curation decision, the things it *missed* are as important as the things it caught.

### 6. Publish with per-item context links
Every saying links to its verse in context (Bible Gateway, KJV). A quote without its context is a slogan; the link is what makes the corpus *readable* rather than just *countable*. The site is pure static (no build, no dependencies) so it works from a file URL, a repo, or a Pages deployment identically.

## The epistemic layering, as a rule

| Layer | Status | What it may be used for |
|---|---|---|
| Red-letter corpus (2,029) | Authoritative | Anything: counts, curation, claims |
| Heuristic OT (5,393) | High-coverage catalogue | Distributions, phase-shape — **not** "God said exactly N things" |
| Curation (604) | Judgment | Thematic reading, devotional use — **not** "these are the only self-references" |

Every page of the wiki states which layer it is sitting on. That one habit is what keeps the whole project checkable.

## Go deeper

- [[Corpus Anatomy]] — the method applied: all the numbers and their status
- [[The Adversary Method]] — the second half: how the *interpretation* on top of the data gets stress-tested
- [[The 23-Second Probe]] — the failure mode the method guards against (fabricating a fixed symbol)
