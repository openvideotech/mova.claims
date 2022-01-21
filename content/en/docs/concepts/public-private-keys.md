---
title: "Public Key Pairs"
description: "Instead of choosing you a username and password, mova uses the more secure approach of Public Key Pairs to know who you are, and log you in quickly and safely."
lead: "Goodbye username-password, welcome Public Key Pairs."
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

Instead of choosing you a username and password, our system uses the more secure approach of Public Key Pairs to know who you are, and log you in quickly and safely. Public key cryptography underpins many of the most secure systems on the Internet.

## What are Public Key Pairs?
Keys are long strings of random characters used widely in modern secure systems to identify people and protect data. Two analogies can be helpful to understand them. 

 - **HOSUE:** Your home has a *public address*, which anyone can visit, and you have a *private door-key* to let only you inside. In Key Pairs, the public key can be viewed by anyone; while the private key is kept secret to yourself.
 - **SEAL:** For thousands of years before computers people wanting to send a message securely could seal an envelope with melted wax and press into this their own exclusive seal or crest. The seal could be viewed by anyone carrying the message, identifying the sender; but only the owner of the private seal could re-create the imprint, preventing people from opening the message and then resealing it. When you sign a message with your private key, it verifies the public key accompanying the message as coming from the only person with that private key.

## How do Public Key Pairs differ from username-passwords?
Your Key Pair is stored on your computer as a tiny text file. When you open MOVA rather than ask you for a password, it will automatically find this text file, and know who you are. No more remembering your password. But if you try to access MOVA from another computer, it won't let you in, and you'll need to copy your keys across.

## Why MOVA uses Public Key Pairs?
Public Key Pairs are widely used in systems requiring secure, private and trustworthy identification and data transmission. They let the application know that you are you, without having to store a copy of your password, which can be a security risk. It's both more secure, and quicker to use.

## Where are Public Key Pairs stored?
This varies depending on your Operating System – the profile page should show you the path to your Private Key. On a Mac they will be inside the Mova-App folder, in the Application Support folder in your Library.

## What are the advantages?
It's quicker to launch an app as you don't need to enter a username and password to login. It's harder for someone pretend to be someone they're not because the public key needs to be backed up with a private key. Without private login credentials stored on a central server, this makes Public Key Pairs more secure, provided you have exclusive access to your computer.

## What are the risks?
Someone with access to your computer or your Private Key could pretend to be you.  In cryptography it's assumed that anyone with access to your computer can do anything (send emails, reset passwords, install malware) so this is seen as a smaller risk within a bigger problem. If you want to access the application from another computer - you will need to copy your private key across – but of course this means someone else could have access to your private key in the process. Finally, if you lose your Private key, perhaps because you lose your computer or there's a hardware failure, you will lose your account. Therefore you should keep a copy of your Public Key Pairs securely in your password manager and encrypted backups.