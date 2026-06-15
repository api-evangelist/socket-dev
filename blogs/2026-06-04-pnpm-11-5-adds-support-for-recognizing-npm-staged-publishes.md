---
title: "pnpm 11.5 Adds Support for Recognizing npm Staged Publishes"
url: "https://socket.dev/blog/pnpm-11-5-adds-support-for-recognizing-npm-staged-publishes"
date: "2026-06-04"
author: "Sarah Gooding"
feed_url: "https://socket.dev/blog"
---
pnpm 11.5 now properly recognizes npm's staged publishing approvals as a strong security signal in release metadata, preventing packages using npm's newer 2FA-backed release workflow from triggering false downgrade warnings. This fix addresses a broader need for clearer publishing signals in package registry metadata as npm adds more secure release mechanisms.
