---
title: "RubyGems Adds Cooldown Feature to Bundler for Newly Published Gems"
url: "https://socket.dev/blog/rubygems-adds-bundler-cooldown"
date: "2026-06-05"
author: "Sarah Gooding"
feed_url: "https://socket.dev/blog"
---
RubyGems and Bundler 4.0.13 introduced an opt-in cooldown feature that delays newly published gems during dependency resolution, allowing developers to configure Bundler to skip gem versions published within a specified number of days. This time-based security control reduces exposure to rapidly deployed supply chain attacks. The feature reflects a broader industry trend toward install-time controls that protect developers against newly released malicious packages.
