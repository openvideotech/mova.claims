---
title: "Peer-to-Peer"
description: "Instead of your data being stored in the Cloud, mova uses a Peer-to-Peer (P2P) data infrastructure."
lead: "Instead of your data being stored in the Cloud (aka big companies' data centres), we use a Peer-to-Peer (P2P) data infrastructure."
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

Communications before the 21st century was mostly Peer-to-Peer: sending letters, or making phonecalls from one person to another. While data might pass through junctions like a mail-box or phone exchange it wasn't stored there.

## What is Peer-to-Peer (P2P) technology?

Communications before the 21st century was mostly Peer-to-Peer: sending letters, or making phonecalls from one person to another. While data might pass through a mail-box or phone exchange it wasn't stored there.

P2P is an application architecture that shares tasks, data or work between Peers. Peers are equally privileged users of the application, sharing and using resources and information across the network of other Peers.

Peer-to-Peer (P2P) on the Internet became famous with piracy battles around Napster and BitTorrent – but these apps also used P2P to lower the costs and improve the speed of media streaming by sharing people's bandwidth. P2P remains popular with the rise of Signal messenger, with 40 million users communicating end-to-end, and blockchain.

## How is it different from cloud-based technology?
The client-server model of 'the Cloud' centralizes processing power or disk storage on servers. With P2P, Peers are both suppliers and consumers of resources, and make a portion of their own resources – such as processing, storage or network bandwidth – directly available to other network participants, without the need for central coordination

## Why does MOVA use peer-to-peer technology?
There's two reasons:
 - Generating ISCC fingerprints for large video files is time- and processor- intensive, and uploading videos to a central server to generate an ISCC fingerprint would cost a lot in storage and bandwidth, while potentially creating a legal liability for the owner of the server. MOVA, as a desktop application, instead generates the ISCC fingerprints locally, with users' own processors and local storage – saving energy costs and time.
 - While MOVA's database of video fingerprints linked to license and payment claims could be hosted by one company on one database; that would centralizes a lot of monopoly power, inevitably enforcing the worldview of a single CEO/board and a single country's legal system. Inspired by the approach of the DNS system, which connects the URLs of the Worldwide Web to the correct server in a decentralized way; MOVA connects a video fingerprint to claims of ownership and payment information, and verified third party certifications of those claims. Each user - and any index or API of the database - is responsible for complying with the laws in the country where they are based, and the terms of service for the application, but this should't stop the database from operating globally.

## What is Holochain?
[Holochain](https://www.holochain.org) is an open-source framework for creating Peer-to-Peer applications. Instead of depending on central servers and processing power, Holochain applications connect user devices directly to each other in secure Peer-to-Peer networks, with all users of an application sharing a distributed database (or ledger) exclusively for that application. 

Online safety is ensured by mutual accountability. Each piece of data has a cryptographic audit trail connected to its author\'s public key, and every user's system helps enforce shared application rules and identify 'bad actors'. [Introductory video](https://www.youtube.com/watch?v=EUfyHNGvnDo).

## What are the advantages?
P2P technology reduces the costs of creating ISCC codes and running a central database.

It avoids monopolization by a single legal entity, instead distributing co-ownership of the database amongst its users. 

As a community-owned dataset, the quality and usefulness of the database is a shared responsibility and priority of its users. 

## What are the risks?
Firstly, this is new, emerging technology and so can have more bugs than normal software.

It's also more complicated than centralized services, so requires people to invest enough time to understand it well enough to use it safely.

While moderators can block the accounts of Bad Actors and flag their false claims, that data will have been published and stored in the distributed hash table that underpins the shared database. It won't be easy to find or read, but it will be there - just like a server log, except that it's distributed in small chunks across many machines.

Finally - as the history of the web has shown - bad actors exist and invent new ways to do bad things.. centralized systems potentially make it easier, or at least quicker to deal with them, given that the definition of 'bad' can be subjective.