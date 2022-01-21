---
title: "Distributed database"
description: "Objective data (e.g. running length, year of release) can easily be centralised; subjective data is by its nature decentralised"
lead: "A distributed database (Holochain) to handle subjectivity and co-ownership around a cultural dataset."
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

{{< alert icon="👉" text="\"Holochain starts with a fundamentally different perspective from either blockchain or client/server architectures: an acknowledgement that all information has its origin in the subjective experience of the agent (usually a person) producing it, and <strong>the argument that data separated from its provenance has lost a critical part of its meaning</strong>.\" <br /> <a href=\"https://dialnet.unirioja.es/servlet/articulo?codigo=8036267\" target=\"_blank\">Exploring Co-Design Considerations for Embedding Privacy in Holochain Apps</a> A Value Sensitive Design Perspective (Harris-Braun, <a href=\"https://dialnet.unirioja.es/servlet/autor?codigo=5372969\" target=\"_blank\">Paul d’Aoust</a>, <a href=\"https://dialnet.unirioja.es/servlet/autor?codigo=5372970\" target=\"_blank\">Anisha Fernando</a>, <a href=\"https://dialnet.unirioja.es/servlet/autor?codigo=5099109\" target=\"_blank\">Kirsten Wahlstrom</a>)" />}}

## What does this really mean?

Let's take a film like Alfred Hitchcock's *Vertigo*. We know for sure objective data such as when it was made (1958), and who was in it (Kim Novak and James Stewart) and its running length (128mins). 

But there's also a lot of subjective data: 
- 191 journalists in the Sight and Sound poll [voted Vertigo the greatest film of all time](https://www.bfi.org.uk/sight-and-sound/greatest-films-all-time). 
- a [tweet that went viral](https://twitter.com/louisvirtel/status/1002264089563840512/retweets/with_comments) however said it's 'unberably boring', 
- numerous feminist critics and writers have called the film [blatantly misogynistic](https://thefword.org.uk/2012/08/vertigo/). 
- [some feminists](https://www.theguardian.com/film/2018/jun/28/vertigo-is-not-the-last-word-in-misogyny-but-a-feminist-deconstruction-of-it) have defended it. 

What does this tell us? Can we reliably say that the film is either the greatest ever, or deeply sexist? We can only really say with references that "a lot of critics have said the film is great", or "many feminists have said the film is sexist" or "a Tweet saying the film is boring was popular". 

[Holochain](https://www.holochain.org), the distributed database (not blockchain) technology MOVA is built on, matches this philosophy in its architecture by trying to centre the subjective experience in relation to the data set. Holochain's founders created the [Cryptographic Autonomy License](https://opensource.org/licenses/CAL-1.0), a new, [somewhat controversial](https://opensource.org/LicenseReview042019#cal) Open Source Initiative verified license that gives the user of an open source decentralised database full agency and control over their own data – while enabling anyone to fork the codebase but not the dataset.

Put another way, objective data (running length, year of release) can easily be centralised; subjective data is by its nature decentralised. But just as publications can aggregate subjective data to produce collective meaning – e.g. Sight and Sound's famous critics poll, or a peer-review academic journal publishing [a paper on the film](https://www.grin.com/document/346603), MOVA's use of certifying organisations with verified credentials offers a path to create new aggregated forms of meaning. And unlike, say, an IMDB score, which is tied deeply to IMDB's records and its community of users – we're not trying to define the nature of that aggregated meaning, but instead creating the data infrastructure for producers of meaning to create that.