---
title: "Introduction"
description: "What is mova? What is the ISCC and Holochain? Why has this been created?"
lead: "<b>mova</b> is a desktop app that lets you register films you've nade on a decentralised database along with license info and payment wallet. This can then be used by platforms looking to show, share and help monetize work."
date: 2020-08-02T13:26:54+01:00
lastmod: 2020-08-002T13:26:54+01:00
draft: false
images: []
menu:
  docs:
    parent: "help"
weight: 10
toc: true
---

## What can mova do? 

**mova** At present Mova alpha can:
 - lets you generate fingerprints for the videos you made or control the copyright of;
 - add metadata such as license & payee info;
 - verify that you are associated with / have access to a specific domain name;
 - publish this on a public shared distributed database as a 'Claim' 
 - index this database and make it public at an API endpoint
 - implement very basic moderation of videos there that break our community [Code of Conduct](/code-of-conduct/) and [Terms of Service](/terms-of-service) (such as are infringing, misleading or illegal).
 We haven't built moderation tools and don't have a community, let alone governance

## lower case?

**mova** can be written in all lower case or all upper case —MOVA— but we try to avoid a mix. It originally stood for Monetizing Open Video Assets or Making Open Video Awesome/Amazing/Accessible, depending who you ask.

## What technologies does mova use?

**mova** is:
- an [electron.js](https://www.electronjs.org/) app
- wrapping a [Holochain](https://holochain.org) app (HApp)
- for Mac, Windows and Linux
- written in [Rust](https://www.rust-lang.org/) and [ReactJS](https://reactjs.org/)
- including the [ISCC library](https://iscc.codes/)
- which runs in [Python](https://www.python.org/), and includes [FFMPEG](https://www.ffmpeg.org/).

## Who made this?

mova was built by Connor Thurland and Pegah Vaezi of [Sprilllow](https://sprillow.com) with [Nicol Wistreich](https://helloideas.com), with funding by Grant for the Web. It's a hosted project of [openvideo.tech](https://openvideo.tech).