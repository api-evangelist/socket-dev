---
title: "GitHub Actions Checkout Now Blocks Risky pull_request_target Checkouts"
url: "https://socket.dev/blog/github-actions-checkout-blocks-pull-request-target-checkouts"
date: "2026-06-20"
author: "Sarah Gooding"
feed_url: "https://socket.dev/api/blog/feed.atom"
---
GitHub released actions/checkout v7 with protections against "pwn request" attacks where privileged workflows check out untrusted pull request code. The update blocks unsafe fork checkouts by default and introduces an allow-unsafe-pr-checkout input for intentional exceptions. This addresses a long-standing supply chain risk that recent incidents like Nx, PostHog, and TanStack exploited.
