---
title: "jscrambler npm Package Compromised in Supply Chain Attack"
url: "https://socket.dev/blog/jscrambler-supply-chain-attack?utm_medium=feed"
date: "2026-07-11"
author: "Socket Research Team"
feed_url: "https://socket.dev/api/blog/feed.atom"
---
A compromised release of the popular jscrambler npm package introduced hidden native binaries that execute automatically during npm install , exposing users to a supply chain attack before any application code runs. The malicious 8.14.0 release, published on July 11 , adds an undocumented preinstall hook that invokes dist/setup.js . It also introduces new files, including dist/setup.js and dist/intro.js , along with platform-specific binaries for Linux, macOS, and Windows embedded in an obfuscated CSI container.
