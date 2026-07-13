---
title: "Fake Braintree NuGet Package Skims Credit Cards and Harvests Merchant Credentials"
url: "https://socket.dev/blog/braintree-nuget-typosquat-skims-credit-cards?utm_medium=feed"
date: "2026-07-09"
author: "Joseph Edwards"
feed_url: "https://socket.dev/api/blog/feed.atom"
---
Socket’s AI scanner flagged a suspicious NuGet package masquerading as the official Braintree payment gateway client, with the first malicious version published on July 3, 2026. It was detected by Socket as potential malware 10 minutes after publication. Follow-on analysis by the Socket Threat Research team revealed a multi-stage .NET implant that intercepts live payment card data, exfiltrates Braintree merchant API keys and harvests host environment secrets upon assembly load.
