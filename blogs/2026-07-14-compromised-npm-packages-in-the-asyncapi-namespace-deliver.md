---
title: "Compromised npm Packages in the AsyncAPI Namespace Deliver Miasma Botnet Loader"
url: "https://socket.dev/blog/asyncapi-supply-chain-attack?utm_medium=feed"
date: "2026-07-14"
author: "Socket Research Team"
feed_url: "https://socket.dev/api/blog/feed.atom"
---
Socket's Threat Research Team identified four compromised npm packages in the @asyncapi namespace distributing a multi-stage botnet loader. The affected packages are @asyncapi/generator-helpers@1.1.1 , @asyncapi/generator-components@0.7.1 , @asyncapi/generator@3.3.1 , @asyncapi/specs ( v6.11.2, v6.11.2-alpha.1 ) Based on current analysis, the compromised packages deploy an obfuscated first-stage payload that downloads an encrypted second-stage payload, identified as Miasma, from IPFS. Users should avoid affected versions, upgrade to patched releases when available, and review developer and CI 
