---
title: "npm Tooling Bug Incorrectly Marks One-Character Packages as Security Holders"
url: "https://socket.dev/blog/npm-tooling-single-character-bug?utm_medium=feed"
date: "2026-06-09"
author: "Sarah Gooding"
feed_url: "https://socket.dev/api/blog/feed.atom"
---
npm incorrectly applied security-holder metadata to multiple one-character packages, including letters, numbers, and the - package. Socket reviewed public npm registry metadata and found several affected packages had been assigned 0.0.1-security or 0.0.1-security.0 versions, with the latest dist-tag moved to the security placeholder. Older package versions remained available.
