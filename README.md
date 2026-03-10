![](./.logo.png)

🌐 A continuously updated list of high-quality DNS resolvers, validated daily.

## 📖 Overview

This repository maintains a curated list of public DNS resolvers that have been verified to be stable, responsive, and returning validated results. The resolver list is updated every 24 hours through an automated pipeline.

## 🔬 Methodology

Our validation process combines multiple techniques to ensure only reliable resolvers make it into the list:

- 🔗 **Aggregation** — Resolvers are pulled from over 100 different public sources and merged into a single deduplicated list.
- 📡 **Port Scanning** — We continuously scan for open port 53 (DNS) across the IPv4 space 24/7 to discover new resolvers as they come online.
- ⏱️ **Stability Testing** — Each discovered resolver is tested repeatedly over time. Only resolvers that demonstrate consistent uptime and response times are included.
- ✅ **Response Validation** — Resolvers must return correct, non-poisoned responses for a set of known domains. Any resolver returning invalid or manipulated results is removed.
- 🔄 **Daily Refresh** — The entire list is regenerated daily, dropping any resolvers that have gone offline or started misbehaving.

## 🚀 Usage

Fetch the latest resolver list directly:

```bash
curl -sL https://raw.githubusercontent.com/acidvegas/liveresolvers/main/resolvers.txt
```

Or clone the repository:

```bash
git clone https://github.com/acidvegas/liveresolvers.git
```

## 🔒 Privacy-Focused Resolvers

For users who prefer well-known, privacy-respecting DNS providers, we also maintain a separate [`privacy-resolvers.txt`](privacy-resolvers.txt) file. This includes providers like Cloudflare, Quad9, Mullvad, AdGuard, NextDNS, and others that have strong no-logging policies and support encrypted DNS protocols (DoH/DoT).

## 📄 Format

The `resolvers.txt` file contains one IPv4 address per line — no ports, no comments, no extra formatting. Ready to use with tools like `massdns`, `dnsx`, `puredns`, `shuffledns`, etc.
