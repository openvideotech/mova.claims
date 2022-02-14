---
title: "Walkthru"
description: "How does <strong>mova</strong> work?"
lead: "How does <strong>mova</strong> work?"
date: 2022-02-02T13:26:54+01:00
lastmod: 2022-02-002T13:26:54+01:00
draft: false
images: []
menu:
  docs:
    parent: "help"
weight: 12
toc: true
---

## Onboarding
The first time you open **mova** it will talk you thru some of the new concepts in **mova**'s design (a [P2P database](/docs/concepts/peer-to-peer/), and [Public Private Keys](/docs/concepts/public-private-keys/)), then invite you to create a profile.

## Profile creation
After creating a profile you can register a default [Web Monetization](/docs/concepts/web-monetization/) wallet, aka a Payment Pointer for all your future claims. You can override this on each Claim, but this is your default.

## Domain verification
To help identify yourself you can go thru a process of domain verification to establish that you control a specific domain name, such as that of your production company or filmmaker web-page.

## Generate an ISCC & claim
Once you're profile is setup you can start to generate [ISCC](/docs/concepts/iscc) fingerprints for your videos and adding additional data about them such as cast, crew, license, terms of use and payment pointer/wallet. 

## Publish the claim
When you are happy with your film details you can publish it as a [Claim](/docs/helps/claims/) which will then appear on our [public API](/docs/help/api/[). We call public film listings Claims as it is not easy to prove that a film is controlled or owned by a specific person; but we can say that a person *claims* to have those right.

## Code lookup
In adition you can use **mova** to perform a 'Code Lookup' - where you generate an ISCC for a video file to see if - there's a matching film in the database. 

## Certifications
**mova** also allows for third party-certifications, such as of festival wins and age certification - but at present these are for demonstration purposes; there are no third party certifiers in place to verify the claims.
