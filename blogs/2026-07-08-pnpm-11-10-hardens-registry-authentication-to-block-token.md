---
title: "pnpm 11.10 Hardens Registry Authentication to Block Token Redirection"
url: "https://socket.dev/blog/pnpm-11-1-hardens-registry-authentication?utm_medium=feed"
date: "2026-07-08"
author: "Sarah Gooding"
feed_url: "https://socket.dev/api/blog/feed.atom"
---
pnpm 11.10 was released over the weekend as a small update that includes several supply chain hardening changes. The main change is a new way to configure registry authentication that keeps a repository's own files from redirecting your registry token to a different host. The release also tightens a few build and packaging commands and adds an install path for pnpm v12, the Rust rewrite.
