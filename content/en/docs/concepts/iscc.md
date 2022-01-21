---
title: "ISCC"
description: "a 'multi-faceted lightweight fingerprint' standardised and used as an identifier"
lead: "the International Standard Content Code"
date: 2022-01-11T03:30:30+01:00
lastmod: 2022-01-11T03:30:30+01:00
draft: false
images: []
menu: 
  docs:
    parent: "concepts"
weight: 10
toc: true
---

{{< alert text="\"It might look complex but I have coded this in 500 lines of Python code. It's just functions, no classes\" <a href=\"https://www.youtube.com/watch?v=4OCvPrDhGuQ\" target=\"_blank\">Titusz Pan</a>" />}}

Coming out of the [Google News Initiative](https://newsinitiative.withgoogle.com/)-funded [Content Blockchain](https://content-blockchain.org/) project, the International Standard Content Code (ISCC)'s goal is to "establish content as the subject of transactions in decentralized and networked environments." In other words to use a 'multi-faceted lightweight fingerprint' standardised and used as an identifier. It is developed by [Titusz Pan](https://craft.de/),  with [Sebastian Posth](https://posth.me/).

## Background

ISCC has some similarities with hashing - a deterministic (always produces the same value), one-way, natural identifier for data of fixed length. Hashing can be:

 - **cryptographic:** verifying the integrity of files or messages, password protection, comparing files without having to access the full file, git, IPFS. They are correlation resistence (when the source data changes it doesn't change in a visible way)
 - **non-cryptographic:** checksums and error correction codes, data deduplication, similarity measurement

## Layers of Content Identification

Titusz Pan identified *6 Layers* of content identification from abstract to concrete commonly used and discussed:

1. Abstract creation / collection (ie a Journal & all its issues, a TV show & its episodes)
2. Meaning - Semantic Field (e.g. RDF tripples -`photo <contains> windmill`, windmill ≠ coal mine)
3. Generic Manifestation (ie the inherent content, file2.jpg ≠ file1.jpg)
4. Media specific Manifestation (ie file.jpg ≠ file.png)
5. Exact Representation (ie file.jpg = file.jpg)
6. Individual Copy (ie print 27 of 100 ≠ print 28 of 100)

## Structure 

 ISCC handles *Syntactical similarity*, ie structural similarity. *Semantic similarity* (level 2, above) – ie meaning – isn't implemented. An ISCC is made up of four 13 character codes, ranging from abstract to concrete:

| **Meta-ID** | **Content-ID** | **Data-ID** | **Instance-ID** |
|---|---|---|---|
| CC7YpFEVFZm8K | CYLXYDN5KREJi | CDUVSFKUtkrv5 | CR1RWa4MVvKvQ |

they can be separasted with hyphens (55chars) or as one long string (52chars). 

**Meta-ID (Layer 1)** 

Abstract creation Metadata is a Title - max 128 bytes; and an extra info field - max 800 bytes. Seed Metadata is metadata that stays froxzen and immutable thru its existence. Floating metadata is mutable metadata that is managed in context with an ISCC.

**Content-ID (Layer 3)** 

Generic manifestation Recognises the inherent qualities of the media, separate from its encoding. There will be some variation in the content with transcoding - but a threshold of up to 10 bits in 64 is suggested as safely indicating the same file after transcoding. Conversely the divergence begins when a threshold of difference is passed - for e.g. changing one paragraph in a document with five paragraphs will appear very different to changing one document in a doc with 100,000 paragraphs, which might appear largely similar or even the same. "The senesitivity is in relation to the whole data". For images - the image is reduced to a fixed size, made black and white and then given a pixel by pixel analysis.

**Data-ID (Layer 4)** 

Media Specific Manifestation Uses content defined chunking, or shift resistence chunking to recognise the same file, used in de-duplication systems. (guess - when media is transferred it's broken up and repackaged, and this overlooks changes from that process?)

**Instance-ID (Layer 5)** 

Exact Representation A cryptographic hash of the file; the root of a Merkle Tree from the media object's raw data. Verifies data integrity. Is published as a 13 char code - but the metadata includes the full 256bit hash.




When a files metadata changes - all the other identifiers stay the same.

'short, globally unique, persistent, resolvable, owned, verifiable, authenticated IDs' - pointing to an ISCC ID.

## Links

- [Public specification](https://iscc.codes/)
- [Governance body](https://iscc.foundation/)
- [Github](https://github.com/iscc/)
- [Demo](https://iscc.coblo.net/)
- [Nearest Neighbor Search demo](https://nns.iscc.in/), 
- [API](https://api11.iscc.in/)
