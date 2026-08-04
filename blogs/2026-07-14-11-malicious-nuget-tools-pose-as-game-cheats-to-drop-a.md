---
title: "11 Malicious NuGet Tools Pose as Game Cheats to Drop a Windows Host-Surveillance Payload"
url: "https://socket.dev/blog/11-malicious-nuget-tools-pose-as-game-cheats?utm_medium=feed"
date: "2026-07-14"
author: "Kush Pandya"
feed_url: "https://socket.dev/api/blog/feed.atom"
---
Socket’s Threat Research Team analyzed 11 malicious NuGet packages published as .NET command-line tools ( DotnetTool package type) that present themselves as game utilities, bots, and “panels”. Every package is a first-stage downloader that fetches and executes a second-stage Windows payload named pepesoft.exe from GitHub Releases and Hugging Face paths under the username pepegit666 , with dormant BitTorrent fallback code built in. The campaign splits cleanly into two stages: A .NET downloader stage shipped inside each NuGet package.
