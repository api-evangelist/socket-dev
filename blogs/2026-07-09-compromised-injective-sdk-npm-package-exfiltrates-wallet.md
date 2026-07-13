---
title: "Compromised Injective SDK npm Package Exfiltrates Wallet Keys and Mnemonics"
url: "https://socket.dev/blog/compromised-injective-sdk-npm-package?utm_medium=feed"
date: "2026-07-09"
author: "Karlo Zanki"
feed_url: "https://socket.dev/api/blog/feed.atom"
---
@injectivelabs/sdk-ts@1.20.21 records private keys and mnemonics, enabling wallet compromise via 17 scoped packages pinned to the malicious version. Socket detected a malicious @injectivelabs/sdk-ts@1.20.21 release published to npm with fake telemetry functionality that exfiltrates wallet private keys and mnemonic phrases. The affected package is part of the Injective Labs TypeScript SDK and receives roughly 50,000 weekly downloads, making the incident significant for developers and applications that handle Injective wallet workflows.
