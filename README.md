<div align="center">

# GetMerged

### Don't guess which door is open. Know before you code.

**The Glassdoor™ for open-source repositories.** Stop burning weekends on PRs that rot in ghost-town repos. GetMerged scores 1,200+ public GitHub repositories on a proprietary **C-Rank™ (S→D)** built from *objective* telemetry — merge rates, maintainer response times, and first-timer success — so your next pull request lands somewhere it will actually be **reviewed, welcomed, and merged**.

[![Live](https://img.shields.io/badge/🌐_Live-getmerged.abhishekco.de-10b981?style=for-the-badge&labelColor=09090b)](https://getmerged.abhishekco.de?utm_campaign=hero_live&utm_source=github&utm_medium=readme)
[![C-Rank Telemetry Engine](https://img.shields.io/badge/C--Rank™_Telemetry-S→D_Engine-f59e0b?style=for-the-badge&labelColor=09090b)](#-the-c-rank™-system)
[![License: MIT](https://img.shields.io/badge/License-MIT-8b5cf6?style=for-the-badge&labelColor=09090b)](https://github.com/GetMergedApp/getmerged/blob/main/LICENSE)
[![Go](https://img.shields.io/badge/Backend-Go_1.22+-00ADD8?style=for-the-badge&logo=go&logoColor=white&labelColor=09090b)](https://go.dev)
[![Next.js](https://img.shields.io/badge/Frontend-Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white&labelColor=09090b)](https://nextjs.org)

**[🚀 Launch the App](https://getmerged.abhishekco.de?utm_campaign=cta_top&utm_source=github&utm_medium=readme)** · **[📊 Browse the Directory](https://getmerged.abhishekco.de?utm_campaign=cta_directory&utm_source=github&utm_medium=readme)** · **[⭐ Star the Repo](https://github.com/GetMergedApp/getmerged/stargazers)** · **[🐞 Report a Bug](https://github.com/GetMergedApp/getmerged/issues/new?template=bug_report.md)**

</div>

---

## 💔 The Problem Every Contributor Knows

You find the perfect repo. The issue says `good first issue`. You read CONTRIBUTING.md, you write the tests, you open the PR…

…then you wait. **11 days. 40 days. Forever.**

> **73% of first-time PRs to unvetted repos never get merged.** Not because the code was bad — because nobody was home.

GetMerged flips the script: instead of guessing which maintainers care, you consult the data.

---

## ⚡ Why GetMerged

| | The old way | The GetMerged way |
|---|---|---|
| 🎲 Choosing a repo | Vibes & star counts | **C-Rank™ S→D**, backed by merge telemetry |
| ⏱️ Review wait | Unknown | **P50 response time** per repo, measured |
| 🤝 First-timer odds | A coin flip | **First-timer success rate**, tracked |
| 🪑 Maintainer health | Invisible | **Bus-factor gate** flags single-maintainer risk |
| 🔁 Repo freshness | Stale READMEs lie | **Adaptive nightly rescans** + staleness decay |

---

## 📊 The C-Rank™ System

Every repository gets a live score (0–100) computed from normalised signals pulled via the **GitHub GraphQL API**:

```
External PR merge rate · P50 response time · Issue triage velocity
Maintainer breadth · First-timer success rate · Good-first-issue depth
Onboarding quality (CONTRIBUTING, templates, CI) · Recency
```

| Tier | Score band | Meaning |
|:---:|:---:|---|
| 🟢 **S** | ≥ 70 | Elite. Fast reviews, high external merge rate, healthy maintainer bench. Ship here. |
| 🔵 **A** | 55–70 | Excellent. Responsive maintainers, welcoming to newcomers. |
| 🟡 **B** | 40–55 | Solid. Merges happen, but pace varies. |
| 🟠 **C** | 25–40 | Lukewarm. Expect slow or inconsistent review cycles. |
| 🔴 **D** | < 25 | Ghost town. Your PR may never be seen. Enter at your own risk. |

**Anti-gaming, engineered in:**
- 🧊 **Hysteresis (±2.0)** — tiers can't flicker across a boundary on noise; promotions must *earn* the jump, demotions need a real slide.
- 🚌 **Bus-Factor Gate** — a repo with ≤ 1 active maintainer is hard-capped at tier **B**. No matter how fast that one hero merges.
- 🌫️ **Small-Sample Damping** — 2 lucky PRs can't fake an S-tier.
- 🗓️ **Staleness Decay** — dormant repos are forced to **D** until they prove life again.
- 🔁 **Adaptive Rescans** — S/A repos refresh nightly; struggling repos re-check less often, stagnant ones accelerate their own decay clock.

<div align="center">
<br>
<a href="https://getmerged.abhishekco.de?utm_campaign=crank_cta&utm_source=github&utm_medium=readme"><strong>See today's C-Rank leaderboard →</strong></a>
</div>

---

## 🗂️ Interactive Directory

Browse 1,200+ scored repositories, filtered server-side for instant results:

<div align="center">

| By Language | By Popularity | By Tier |
|:---|:---|:---|
| [🐹 Go](https://getmerged.abhishekco.de/?language=go&utm_campaign=dir_go&utm_source=github&utm_medium=readme) | [⭐ 500–1k](https://getmerged.abhishekco.de/?stars=500-1k&utm_campaign=dir_stars1&utm_source=github&utm_medium=readme) | [🟢 S-Tier only](https://getmerged.abhishekco.de/?tier=S&utm_campaign=dir_s&utm_source=github&utm_medium=readme) |
| [🔷 TypeScript](https://getmerged.abhishekco.de/?language=typescript&utm_campaign=dir_ts&utm_source=github&utm_medium=readme) | [⭐ 1k–5k](https://getmerged.abhishekco.de/?stars=1k-5k&utm_campaign=dir_stars2&utm_source=github&utm_medium=readme) | [🔵 S + A](https://getmerged.abhishekco.de/?tier=SA&utm_campaign=dir_sa&utm_source=github&utm_medium=readme) |
| [🐍 Python](https://getmerged.abhishekco.de/?language=python&utm_campaign=dir_py&utm_source=github&utm_medium=readme) | [⭐ 5k–50k](https://getmerged.abhishekco.de/?stars=5k-50k&utm_campaign=dir_stars3&utm_source=github&utm_medium=readme) | [🔴 Avoid D](https://getmerged.abhishekco.de/?exclude=D&utm_campaign=dir_nod&utm_source=github&utm_medium=readme) |
| [🦀 Rust](https://getmerged.abhishekco.de/?language=rust&utm_campaign=dir_rs&utm_source=github&utm_medium=readme) | [⭐ 50k–500k+](https://getmerged.abhishekco.de/?stars=50k-500k&utm_campaign=dir_stars4&utm_source=github&utm_medium=readme) | [📈 All repos](https://getmerged.abhishekco.de?utm_campaign=dir_all&utm_source=github&utm_medium=readme) |

</div>

---

## ✨ Feature Highlights

- ⚡ **C-Rank™ Scoring Engine** — objective, math-backed tiers with hysteresis, bus-factor caps, and staleness decay.
- 🎯 **Server-side filtering & pagination** — slice by language and star bucket; sub-millisecond responses via Valkey + Cloudflare edge caching.
- 🤖 **AI Maintainer Vibe Check** — LLM-generated review-style summaries and a PR submission checklist per repo, so you walk in prepared.
- 📊 **Macro telemetry visualizations** — live distribution charts of winning languages and tier breakdowns.
- 🔐 **GitHub OAuth + watchlists** — sign in once (7-day signed JWT), track the repos you're eyeing.
- 🌌 **Spacetime particle grid** — an interactive relativity-lens background, because scoring engines deserve aesthetics too.

---

## 🛠️ Architecture

```
┌─────────────────────┐      ┌──────────────────────────┐
│   Next.js + Tailwind │ HTTP │  Go 1.22 + gin-gonic     │
│   shadcn/ui frontend │◄────►│  Native SQL (no ORMs)    │
│   /frontend          │ JSON │  /backend                │
└─────────────────────┘      └────────┬─────────┬────────┘
                                      │         │
                          ┌───────────▼──┐   ┌──▼──────────────────┐
                          │ Turso/LibSQL │   │ GitHub GraphQL API  │
                          │ Valkey cache │   │ OpenCode AI insights│
                          └──────────────┘   └─────────────────────┘
```

| Layer | Tech |
|---|---|
| Backend | Go 1.22+, gin-gonic, native SQL queries (zero ORM dogma) |
| Frontend | Next.js, Tailwind CSS, shadcn/ui |
| Data | Turso (LibSQL) in prod · SQLite in dev |
| Cache | Valkey in-memory + Cloudflare edge (`Cache-Control` headers) |
| External | GitHub GraphQL API · OpenCode AI |

```bash
git clone https://github.com/GetMergedApp/getmerged.git && cd getmerged
cp .env.example .env   # config-driven; no defaults, no hacks
make dev               # backend :8080 · frontend :3000
```

---

## 🤝 Contributing

We eat our own cooking — this repo maintains its own C-Rank™, and it shows. `good first issue`s get triaged within days, not months.

1. Browse the [open issues](https://github.com/GetMergedApp/getmerged/issues) — look for [`good first issue`](https://github.com/GetMergedApp/getmerged/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22).
2. Fork → branch → TDD (red → green → refactor) for backend changes.
3. `golangci-lint` / `eslint` green before you push.
4. Open your PR — and enjoy being reviewed by someone who's actually home.

---

## 🔗 Backlinks & Community

If GetMerged saved you from a ghost-town repo, pay it forward:

<div align="center">

<a href="https://getmerged.abhishekco.de?utm_campaign=backlink_footer&utm_source=github&utm_medium=readme"><img src="https://img.shields.io/badge/Find_your_next_repo-GetMerged-10b981?style=flat-square" alt="GetMerged" title="GetMerged — Glassdoor for open-source repos"/></a>
&nbsp;
<a href="https://github.com/GetMergedApp"><img src="https://img.shields.io/badge/GitHub-@GetMergedApp-181717?style=flat-square&logo=github" alt="GetMergedApp org" title="GetMergedApp on GitHub"/></a>
&nbsp;
<a href="https://github.com/GetMergedApp/getmerged"><img src="https://img.shields.io/badge/Source-getmerged/fork-8b5cf6?style=flat-square&logo=git" alt="getmerged repo" title="Fork the getmerged repo"/></a>

**⭐ Star us** — [github.com/GetMergedApp/getmerged](https://github.com/GetMergedApp/getmerged/stargazers) ·
**🐦 Share it** — tell one contributor whose PR died silently.
**🔗 Link to us** — `https://getmerged.abhishekco.de` in your CONTRIBUTING.md so contributors arrive informed.

</div>

---

<div align="center">

<sub><strong>C-Rank™</strong> is a trademark of the GetMerged project. Data sourced from public GitHub activity via the GraphQL API.</sub><br/>
<sub>Made with ☕ and an unreasonable hatred of unanswered PRs.</sub><br/><br/>

<a href="https://getmerged.abhishekco.de?utm_campaign=final_cta&utm_source=github&utm_medium=readme" title="Open the GetMerged directory now"><strong>🚪 Don't guess which door is open. GetMerged shows you. →</strong></a>

</div>

<!-- markdownlint-disable MD033 -->
