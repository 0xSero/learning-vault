---
title: Red Letter Bible
date: 2026-08-19
layer: primitives
tags:
  - layer/primitives
  - corpus
aliases:
  - Red-letter
  - Red letter corpus
---

# Red Letter Bible

> [!abstract] TL;DR
> A red-letter Bible prints every word spoken by Jesus in red ink. The corpus of those words — **2,029 verses** across Matthew, Mark, Luke, John, Acts, 1 Corinthians, 2 Corinthians, and Revelation — is the authoritative data layer of the God research. It is the only part of the corpus that requires no interpretation to identify: the edition's editors already made the speaker attribution.

## What it is

Standard Bibles print all text in the same color. Red-letter editions (popularized in the 19th century; e.g., the 1876 *The Holy Bible in the Words of Christ*, and the modern KJV red-letter editions) mark the direct words of Jesus Christ in red. The practice is a devotional convention, not a critical one — but it is a *stable, widely agreed* convention, which is exactly what makes it useful as data.

The corpus used in the God research comes from [NolanLT/kjv-bible](https://github.com/NolanLT/kjv-bible), a machine-readable KJV where every red-letter verse is wrapped in braces:

```
{ And Jesus said unto them, Suffer the little children to come unto me... }
```

## Why it matters for the corpus

The God research has two data layers with different epistemic status, and the distinction is load-bearing:

| Layer | Verses | Status |
|---|---|---|
| Jesus (NT) | 2,029 | **Authoritative.** The red-letter marking is the standard corpus; nothing is guessed. |
| God (OT) | 5,393 | **Heuristic.** The KJV has no red-letter markup for divine speech, so verses were identified by speaker-attribution frames ("God said", "Thus saith the LORD", introducer frames with continuation rules). |

Every page of the wiki states which layer it is sitting on. This is the single most important methodological decision in the project: **label authoritative and inferred separately, or the whole corpus becomes an uncheckable blob.**

## Coverage and limits

Red-letter editions cover the *spoken words* of Jesus. What that means in practice:

- **Gospels:** full coverage of direct speech.
- **Acts:** the post-resurrection appearances to Saul (9, 22, 26) are red-letter; narrative voice is not.
- **Epistles:** only the handful of verses quoting Jesus directly (1 Cor 11:24–25, 2 Cor 12:9).
- **Revelation:** the voice of the risen Christ in the letters to the seven churches and the opening/closing self-declarations.
- **Not included:** words *about* Jesus (Pilate in John 18:34, the guards in John 7:45), the narrator's voice (John 3:16), and the Holy Spirit's speech. This last exclusion is why [[The Sacrifice Thread]] cites John 3:16 as *narrator's voice* even though it is the theological center of the gospel.

## Go deeper

- [[Corpus Anatomy]] — the full numbers, distributions, and curation rules
- [[The Corpus Method]] — how the heuristic layer was built, including the bug that was caught
- [[Self Reference Catalog]] — the 604-saying curated layer built on top of the 2,029

## Sources

- [Red letter Bible — Wikipedia](https://en.wikipedia.org/wiki/Red_letter_Bible)
- [NolanLT/kjv-bible](https://github.com/NolanLT/kjv-bible) (KJV with red-letter markup, public domain)
- [The Holy Bible in the Words of Christ (1876) — Wikipedia](https://en.wikipedia.org/wiki/The_Holy_Bible_in_the_Words_of_Christ)
