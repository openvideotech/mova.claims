---
title: "Background"
description: "Why has mova been created? Why so many new ideas?"
lead: "Why did you make this and why is it so complex? What's the big idea?"
date: 2020-08-02T13:26:54+01:00
lastmod: 2020-08-002T13:26:54+01:00
draft: false
images: []
menu:
  docs:
    parent: "help"
weight: 20
toc: true
---

## What's the motivation for making this?

**mova** follows on from the arrival in the last few years of decentralized social media tech like [Activity Pub](https://www.w3.org/TR/activitypub/), [Matrix](https://matrix.org/) and [Secure Scuttlebut](https://scuttlebutt.nz/) – and micropayment and streaming payment systems like [Web Monetization]((/docs/concepts/web-monetization/)) and [Interledger](https://interledger.org/). Together these support a decentralized media ecosystem where the *discovery* and *production/hosting* layers for pay-per-view, subscription and donation-based are decoupled. This has long been discussed in the Open Video movement, but it's only now that there's payment technologies that coulld support it.

This decoupling is much like how offline film distribution works, with a separate producer, distributor and exhibitor/TV channel/video store. It's also similar to how most of the web works, separating server, search enginge/social network/email server and browser. But given the complexities around video - not only for copyright but legal and safeguarding issues, the web today has centralised both non advertising video hosting and discovery around a few services.

## How does mova fit in? 

Just as the decoupled web uses the [Domain Name System (DNS)](https://en.wikipedia.org/wiki/Domain_Name_System) to match a URL with the correct server – and lets anyone link to that, a decentralised video ecosystem needs some kind of a metadata registry. There are currently 
 - centralised metadata registries for video which give a [unique identifier](https://en.wikipedia.org/wiki/Unique_identifier) to every film like [ISAN](https://www.isan.org/) and [EIDR](https://www.eidr.org/); and 
 - embeded metadata registries, the biggest being Adobe's [Content Authenticity Initative (CAI)](https://contentauthenticity.org/). 

**mova** sits somewhere in between, in that it uses a unique identifier (like the ISAN or EIDR code) but that this is generated from the media itself (like CAI). Because **mova** uses as its identifer a new open source media fingerprinting protocol, the [International Standard Content Code](/docs/concepts/iscc/) or ISCC - anyone with a copy of the same video will generate the same ISCC identifier. Most signficiantly, similar video files (ie those which differ only by size, colour space, resolution or file format) will generate simiilar ISCC codes and be able to match up. So unlike CAI if someone transcodes a video file (ie from H264 to WebM), the link with the metadata needn't be lost. This is useful online because if you upload the same photo to three different websites, they will transcode/compress it differently so normal hashing (like that used by NFTs) would suggest there is a different file.

## So the ISCC is like a DNS nameserver?

On its own the ISCC is just a 52 character long string (or more accurately, four 13-character strings describing four different attributes of a file) – and any text, PDF, image or video file can produce one. But because all media files can produce an ISCC, and recognisie 'nearest neighbors', ie similar media files - the ISCC as an identifier can be used in a decentralised way to provide further information about that video. This could be copyright & license info, credits, subtitle files, legal notices, or a list of academic citations, etc. 

**We should also not be naive that repressive regimes and giant corporate legal departments can - and do - use fingerprints of media to create watchlists of activist or embarassing content to censor and block. The creators of mova strongly oppose such usage.**

## So Whois in control of video DNS then?

Very funny, like what you did there ([eh?](https://en.wikipedia.org/wiki/WHOIS)). 

Our position is that no single company or country should be in charge of it. However we anticipate a number of companies and blockchain projects could try to be, eith the emergence of two types of registries:
 - centralised media databases
 - large open decentralised blockchain databases

## So what kind of registry is mova?
 
In this too, **mova** tries to take the middle 'Goldilocks;' path. We use a private decentralised database shared between everyone who runs a copy of the **mova** app: it's neither sitting on one company's computer *or* left to run wild across the entire internet. 

 ## Sounds a lot like the Blockchain?

No - what's the same as the Blockchain is **mova** uses a 'distributed hash table' ([DHT](https://en.wikipedia.org/wiki/Distributed_hash_table)) or 'public ledger' – which is a shared public database. 

But unlike the Blockchain, this database is only writable to by the **mova** application and its protocols. It's a private database, which lets all of the app's users write to it. But you could also say it's a public database, closed to anyone not using the mova app. 

## What's this public ledger called?

[Holochain](/docs/concepts/holochain).

## I knew you were trying to sell me Blockchain!

It's a confusing name, but Holochain is NOT a Blockchain. A Blockchain like Bitcoin or Ethereum is writable to by every client and app using that system - it's one giant multi-terabyte database of all the diffeerent applications and services and transaction using that protocol. This not only makes transactions slow, because nodes have to process terabytes of data, it has a big environmental footprint. 

Holochain is a [peer-to-peer](/docs/concepts/peer-to-peer/) database, with a closed network of peers unique to each Holochain app, which is more energy and resource efficient. So if only 10 people donwload and use **mova** the data is shared only between 10 people. Furthermore, within each app, no single node loads the full database, but just a small segment - or shard - of it. 

The main challenge with distributed databases is establishing trust because any node or group of nodes has the potential to manipulate the data that they are hosting. Blockchains use either Proof-of-Work or Proof-of-Stake to establish trust (Proof of Work being the reason Bitcoin uses so much energy). Holochain uses a ['gossip protocol'](https://www.educative.io/edpresso/what-is-gossip-protocol) where shards of data are shared and verified with random peers on the network. This is a much lower energy form of validation.

## OK so it's not Blockchain, but why does mova use a decentralised database?

Quick answer: because we don't think any single one company or government should have that much power over the entire world's media. 

Long answer: because its generated from each video, the ISCC allows multiple authorities to add layers of meaning and provenange information to ISCC codes – and we think this is the best solution to the risk of a single chief censor for the world. Such a censor would adopt the political views of whichever country they're headquartered in, and whichever government is in power there at the time. It would end up in an eternal battle between the divides of the political spectrum; such an registry cannot work if it's only serving half of a population.

Some in the Web3 and Blockchain world see as an alternative to centralization an automated, leaderless structure in place of this, where digital authorities and [DAOs](https://en.wikipedia.org/wiki/Decentralized_autonomous_organization) folllowing [Smart Contracts](https://en.wikipedia.org/wiki/Smart_contract) decide everything, with power centred amongst those who've learnt how to best master the new tools, or even simply those who own the most tokens and are the richest. 

Others would say any potential for a censor - centralized or decentralized should be resisted at all cost - which is understandably worrying. Yet most people online spend most of their time between two or three companies web services; decentralisation depends on governance, and censorship is the ugle end-point of governance. The only way to avoid censorship is the darkweb, and most people don't want that, so return to a few powerful advertiser-funded services.

We picture something somewhat different, where existing authorities coulld play a role alongside user-led communities to create overlapping layers of meaning and metadata around media. For instance, the [BBFC](https://www.bbfc.co.uk/) or [MPAA](https://www.motionpictures.org/) might have a centralised registry of film age certification data; while a film journal might build a publicly generated and approved list of films that pass the [Bechdel test](https://bechdeltest.com/). The IMDB or [TMDB](https://www.themoviedb.org/) might offer comprehensive film metadata, while sales agents and film rights blockchains might aggregate license and payee info. Amazon Web Services or Google Cloud or Ben and Jerry's Bicycle Powered Server Farm might provide hosting and CDN, but none of those systems need sell your attention and private data to the highest paying advertiser.

## Sounds like utopia. 

You know utopia is a place that doesn't exist?

## Exactly - what's the catch?

We assume that all these overlapping datasets will end up being aggregated, with conflicts between them needing to be resolved. In this multi-meta-meaning future we would anticpate, initially, a rise in big centralised data stores competing on scale, price and speed (one company has already renamed themselves…). 

However, these would only be able to scale quickly by automating moderation and rights verification. But it seems that many of the problems we see around media online - be it around determining authorship, fair use, offensive or hateful speech, legal compliance or accurate classification need humans to make judgements in an accountable and transparent way, that can be appealed, questioned and discussed in a calm environment. 

So growing parallel to the 'fast registries', ie the automated centralised services who would compete through having superior AI and vast processing power, we anticipate a place for 'slow registries' that are more dependable, human-led, community-run and owned datasets. Just as Wikipedia couldn't be created by AI - we're trying to imagine what a shared human-built and -owned common media dataset looks like.

## Nothing too ambitious then?

We've planted some seeds for a new kind of metadata registry, but this will only grow into a healthy project with both demand and a community of support. The next step of development, however long it takes, is something we will want to do as part of a much broader community - we're too small (and English-speaking) as a team to take too many big decisions. Any system that wants to scale up for media governance, would need to be shaped by the community that needs and uses it. 

We not only need a community, there needs to be a model to support the time put into moderating, classifying, verifying and keeping the database in good shape - otherwise it would only be strong in areas with lots of volunteers available. We've an idea of how a payment model for moderation could work, but without media or a community - or proof of demands, it's just more big ideas to read.

 ## So what next?

**mova** is first step in a possibly long journey. It's a decentralised app for individual filmmakers to register and share their film's metadata with an ISCC code and payment wallet, but moderation is still centralised and very basic; while the Holochain architecture is so new (it's technically still pre-launch) we can't guarantee it won't break along the way. 

For that reason we're launching with a [closed beta programme](https//crm.openvideo.tech/founding-cohort) with a limited number of users.

We've built enough to explore the idea, but it's not yet enough to scale. It's a rowing boat with no rowers.

 ## How do I get involved?

 Apply to join our beta programme [here]. Say hello on our [Mattermost](https//matter.openvideo.tech/) forum. Check our community call calendar to see when we've next got a public meeting.

