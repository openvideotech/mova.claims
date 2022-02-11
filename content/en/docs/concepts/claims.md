---
title: "Adding a claim"
description: "Mova is built around the idea of Claims - which are public claims linking a specific ISCC code to a specific claim of some information."
lead: "Mova is built around the idea of Claims - which are public claims linking a specific ISCC code to a specific claim of some information."
date: 2022-02-02T13:26:54+01:00
lastmod: 2022-02-02T13:26:54+01:00
draft: false
images: []
menu:
  docs:
    parent: "concepts"
weight: 20
toc: true
---

Central to **mova** is linking the ISCC fingerprint of your work to further metadata, which is made public on our public database as a 'claim'. We use this language to make no judgement on the accuracy of the information. We want to provide tools to help people make informed decisions around mova's data - and ensure the best dataset possible - but as any philosopher will tell you, proving something is true is trickier than it seems, and people should use published data at their own risk. 

## Categorising metadata

Some claims can be verified technically, e.g. "this film is 81 minutes long" while others are completely subjective and have no absolute value of truth, e.g. "this film is amazing". We recognise media metadata falls into the following groups:

- **embedded**: data that could be verified technically from the film itself: running length, aspect ratio, file format, language, and the ISCC code (or parts of it).
- **objective**: data that can be verified externally from the film: cast and crew, locations, awards, festival selection, copyright holder, distributors, list of themes, Bechdel test, etc,
- **legal:** data that forms the basis of contractual and legal arrangements, such as copyright owner, data privacy flags, chain of title, age restrictions, payees. Like objective data, this has one version of what's true, but in the more extreme cases this 'truth' may need a court to establish or disprove it, and could lead to criminal charges if it's misrepresented or ignored. While it's not a big deal to spell an actor's name wrong, getting legal data wrong can have liabilities for those who depend on it.
- **subjective**: data where there can be no singular 'true' value. For instance, data relating to quality, popularity, funnyness, accuracy, offensiveness or trigger warnings. Subjective data has the ability to be aggregated to create collective subjective meaning (e.g. critics polls, audience ratings, etc) that can converge a common understanding.

In adition, this data can vary:

- **by region**: data that is specific to a country or region. For instance age certification, distributor, captions/subtitle files, legal status, box office information.
- **by time**: data that is specific to a period of time. For instance license, historic censorship, copyright/public domain status, changing distributors & rightsholders.

## Claims in mova

At this stage - **mova**'s primary focus is one area, whic is arguably the most challenging: that you own or control a film and can define its license, and earn money from it. **mova** lets you link your film's ISCC code to a Payment Pointer wallet address to allow you to start earning money. As legal data there is obviously a consequence in getting this wrong, which is why **mova**'s Terms of Services allow for the use **mova** only on condition of them only providinig accurate informaiton – especially in this. 

## Building trust around a claim

There is currently one method in **mova** to establish that you are who you say you are, which is to [verify your profile against a URL](/docs/help/verifying/). For instance if we know that www.msbigshotdirector.com is the homepage for the director of several films, anyone registering those films on our system who has verified that they control that domain name should either be Ms Bigshot Director, or her staff. But this wouldn't stop someone from registering and verifying MsBigshotDirector.co or .net – it's a not a fraud-proof verification system, but it offers some protection.
