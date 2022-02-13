---
title: "mova API"
description: "Information about mova's Application Programming Interface, or API"
lead: "There is a prototype basic public API providing access to claims registered on the <strong>mova</strong> app."
date: 2022-02-02T13:26:54+01:00
lastmod: 2022-02-02T13:26:54+01:00
draft: false
images: []
menu:
  docs:
    parent: "help"
weight: 200
toc: true
---

All Claims registered publicly on **mova** will be made available via a public API, unless they have been hidden for breaching our Terms of Service.

## Searches

The API will allow developers to query the MOVA registry and return different types of data:

### ISCC Codes

These should be accessible straight after submission. You can search for:
 - the listing(s) for a specific **full ISCC code** with `/api/claims/:iscc_code=12344-123AF-8ASF32-HGAS9`
 - the listings for a **partial ISCC code**, by adding `?match=meta,content,data,instance` to an ISCC search, and deleting the types of query not needed to search on. For instance to only look for content matches, not data matches (which could recognise different file formats/resolutions) you would append `?match=content`.

### Database searches

These are revised every hour. To search for claims in the registry that match some metadata:
 - start with `api/query`,
 - add `?value=[something]`
 - add `?number=[integer]` (default is 10) to define how many results to return
 
 To query a **specific field**, add `?field_def=[entryHash]` where '[entryHash]' is the ID for whatever field you want to search on (e.g. `?field_def=uhCkklhPcwiI7BvIKfBVi7GalKpR785wGDiNICl8XNqrplsSCRGjF?value=`)
 
 NB - You can wrap your query in quotes, but you do, remember to backslash quote marks inside, for e.g. `api/query?value="don\'t look up"?`.

 ## How does it work?
 
The **mova** API bases its data from the distributed database that powers *mova* stored in parts on every user's computer. For speed, the full database is crawled and indexed once an hour so there's a maximum delay of an hour between adding a claim and it appearing in the database. ISCC codes can be search on immediately however.

The API endpoint has four-parts:
 - **h-app node.** An always-on **mova** instance (which also ensures the database is always accessible during low-usage), which supports a…
 - **crawler.** A runner which looks thru the published Claims and tracks new and updated listings, writing these to an…
 - **index.** For speedy search and access by the…
 - **API**. Allows for searches by partial and whole ISCC codes, and terms from any published string.
