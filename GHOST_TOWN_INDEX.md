# The Open Source Ghost Town Index (2026 Edition)
### We Analyzed 34,175 GitHub Repositories. Here Is Why 38% of Mega-Popular Codebases Are Ghost Towns.

*By the [GetMerged](https://getmerged.abhishekco.de) Research Team · Updated September 2026*

---

## Executive Summary

For over fifteen years, the primary currency of trust in software engineering has been the **GitHub Star**. Developers star repositories they admire, recruiters scan stars to assess candidates, and ambitious engineers spend hundreds of hours writing code for high-star repositories expecting recognition.

**The data reveals that GitHub stars are a dangerously misleading vanity metric.**

We explicitly filtered out curated bookmark lists (such as `awesome-*`, `free-programming-books`, and `system-design-primer`) to focus **strictly on real software codebases, compilers, frameworks, developer tools, and applications**.

After analyzing telemetry across **34,175 public repositories** using the [GetMerged C-Rank™ Engine](https://getmerged.abhishekco.de):

1. **37.6% of real codebases with >20,000 stars are D-Tier Ghost Towns**: They merge less than 15% of external pull requests, and median contributions sit unacknowledged for months.
2. **Only 4.0% of mega-popular repos achieve S-Tier**: Maintaining world-class community turnaround while operating at massive scale is an extreme rarity achieved by fewer than 1 in 25 high-star projects.
3. **The 5 Archetypes of Software Ghost Towns**: Why genuine engineering projects rot on GitHub (detailed below: Gerrit mirrors, sunset codebases, unmaintained viral CLIs, overwhelmed AI repos, and read-only model drops).
4. **Go & Rust Run Tech's Healthiest Ecosystems**: With ghost rates below 31% and merge rates above 60%, Go and Rust repositories exhibit the strongest review discipline, while Shell (49.5%) and C++ (45.2%) suffer from acute maintenance paralysis.

---

## 📊 The 20k+ Star Illusion: Stars vs. Contributor Reality

When an open-source project crosses 20,000 stars, conventional wisdom assumes it is thriving. Here is what actually happens across all 1,232 repositories in that bracket:

| C-Rank™ Tier | Classification | % of 20k+ Star Repos | Avg PR Merge Rate | Median Review Turnaround |
| :---: | :--- | :---: | :---: | :---: |
| **S-Tier** | 🌟 World-Class Community | **4.0%** | 87.4% | ~1.3 hours |
| **A-Tier** | 🤝 Highly Responsive | **31.5%** | 82.9% | ~1.8 hours |
| **B-Tier** | ⏳ Moderate Turnaround | **21.5%** | 68.8% | ~3.6 hours |
| **C-Tier** | ⚠️ High Friction | **5.4%** | 67.1% | ~4.7 hours |
| **D-Tier** | 💀 Ghost Town / Dormant | **37.6%** | **13.1%** | **Weeks / Unresponsive** |

```
Distribution of GitHub Repos with >20,000 Stars:
  [█████████████████████████████████████        ] D-Tier (Ghost Towns): 37.6%
  [█████████████████████████████                ] A-Tier (Responsive): 31.5%
  [█████████████████████                        ] B-Tier (Moderate):   21.5%
  [█████                                        ] C-Tier (Friction):    5.4%
  [████                                         ] S-Tier (Champions):   4.0%
```

> **The Contributor Reality**: If you pick a software repository with 20k+ stars at random to submit your first pull request, **you are nearly 10x more likely to land in a Ghost Town (37.6%) than an S-Tier community (4.0%)**.

---

## 💀 The Hall of Shame: Mega-Star Software Ghost Towns

*(Filtered to include strictly real programming software projects, libraries, and frameworks)*

| Repository | Stars | Language | C-Rank Score | External Merge Rate | Review Status | Primary Failure Mode |
| :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| [`vuejs/vue`](https://getmerged.abhishekco.de/repo/vuejs/vue) | 210,134 | TypeScript | 8.0/100 | 0% | Unresponsive / No Comments | Sunset Flagship (development moved to vuejs/core) |
| [`mattpocock/skills`](https://getmerged.abhishekco.de/repo/mattpocock/skills) | 203,890 | Shell | 29.9/100 | 7.1% | 21.1h | Dormant / Unresponsive Maintainers |
| [`yt-dlp/yt-dlp`](https://getmerged.abhishekco.de/repo/yt-dlp/yt-dlp) | 180,490 | Python | 8.4/100 | 0% | 22.9d | Maintainer Overwhelm (550h review turnaround) |
| [`ollama/ollama`](https://getmerged.abhishekco.de/repo/ollama/ollama) | 177,729 | Go | 20.0/100 | 0% | Unresponsive / No Comments | Dormant / Unresponsive Maintainers |
| [`anthropics/skills`](https://getmerged.abhishekco.de/repo/anthropics/skills) | 164,588 | Python | 17.6/100 | 0% | Unresponsive / No Comments | Dormant / Unresponsive Maintainers |
| [`AUTOMATIC1111/stable-diffusion-webui`](https://getmerged.abhishekco.de/repo/AUTOMATIC1111/stable-diffusion-webui) | 164,294 | Python | 8.0/100 | 0% | Unresponsive / No Comments | Hyper-Growth Bottleneck (massive PR backlog) |
| [`airbnb/javascript`](https://getmerged.abhishekco.de/repo/airbnb/javascript) | 148,087 | JavaScript | 17.6/100 | 0% | 1m | Dormant / Unresponsive Maintainers |
| [`ytdl-org/youtube-dl`](https://getmerged.abhishekco.de/repo/ytdl-org/youtube-dl) | 140,807 | Python | 8.0/100 | 0% | Unresponsive / No Comments | Abandoned Viral CLI (unmaintained codebase) |
| [`anthropics/claude-code`](https://getmerged.abhishekco.de/repo/anthropics/claude-code) | 139,325 | Python | 8.0/100 | 0% | Unresponsive / No Comments | Dormant / Unresponsive Maintainers |
| [`golang/go`](https://getmerged.abhishekco.de/repo/golang/go) | 135,583 | Go | 19.6/100 | 0% | 1m | Gerrit Mirror Trap (GitHub PRs auto-rejected) |

---

### 🔍 Anatomy of a Software Ghost Town: The 5 Traps

Why do real, battle-tested software projects with tens of thousands of stars stop merging pull requests?

1. **The External Code-Review Mirror Trap (e.g., `golang/go`)**:
   Projects like the Go compiler mirror their code to GitHub for maximum visibility, but conduct **all code reviews on Gerrit** (`go-review.googlesource.com`). Any external contributor who spends hours writing tests and opening a pull request on GitHub receives an immediate automated rejection or gets closed unmerged.
2. **The Deprecated / Sunset Flagship (e.g., `react/create-react-app`, `vuejs/vue`)**:
   Projects like Create React App or Vue 2 retain their massive star counts forever, keeping them at the top of beginner search results. But the maintainers have moved on to Vite or Vue 3. Pull requests rot indefinitely.
3. **The Abandoned Viral CLI (e.g., `ytdl-org/youtube-dl`, `nvbn/thefuck`)**:
   A solo developer builds an ingenious CLI tool that reaches 100k+ stars. But when real life, legal notices, or career changes intervene, the creator steps away. The codebase remains frozen in time with hundreds of open PRs.
4. **The Hyper-Growth Maintainer Bottleneck (e.g., `AUTOMATIC1111/stable-diffusion-webui`)**:
   Viral explosion in AI tooling creates an influx of 500+ PRs a week. Without a formal engineering organization or paid triage team, maintainers retreat into triage paralysis.
5. **The "Read-Only" Open-Weights Dump (e.g., `openai/whisper`)**:
   AI frontier labs release inference code to accompany paper publications, but have zero mandate to act as community stewards. External contributions are not part of their workflow.

---

## 🌟 The Hall of Fame: S-Tier Community Champions

*(Filtered for verified multi-maintainer teams with sustainable 35%–90% merge rates)*

| Repository | Stars | Language | C-Rank Score | External Merge Rate | Median Turnaround | Active Maintainers |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| [`supabase/supabase`](https://getmerged.abhishekco.de/repo/supabase/supabase) | 107,158 | TypeScript | 74.4/100 | 62.6% | 1m | 11 |
| [`OpenBB-finance/OpenBB`](https://getmerged.abhishekco.de/repo/OpenBB-finance/OpenBB) | 71,092 | Python | 70.4/100 | 58.3% | 1m | 4 |
| [`cline/cline`](https://getmerged.abhishekco.de/repo/cline/cline) | 65,623 | TypeScript | 72.0/100 | 49.4% | 1m | 21 |
| [`commaai/openpilot`](https://getmerged.abhishekco.de/repo/commaai/openpilot) | 63,320 | Python | 70.6/100 | 53.4% | 1.0h | 9 |
| [`upstash/context7`](https://getmerged.abhishekco.de/repo/upstash/context7) | 60,116 | TypeScript | 81.4/100 | 59.0% | 6.2h | 5 |
| [`x64dbg/x64dbg`](https://getmerged.abhishekco.de/repo/x64dbg/x64dbg) | 49,042 | C++ | 79.7/100 | 63.2% | 7.7h | 5 |
| [`babel/babel`](https://getmerged.abhishekco.de/repo/babel/babel) | 43,958 | TypeScript | 73.3/100 | 55.0% | 2m | 6 |
| [`stablyai/orca`](https://getmerged.abhishekco.de/repo/stablyai/orca) | 37,284 | TypeScript | 70.7/100 | 88.4% | 5m | 72 |
| [`MetaCubeX/mihomo`](https://getmerged.abhishekco.de/repo/MetaCubeX/mihomo) | 32,942 | Python | 73.0/100 | 35.3% | 1.4h | 2 |
| [`langfuse/langfuse`](https://getmerged.abhishekco.de/repo/langfuse/langfuse) | 32,500 | TypeScript | 71.2/100 | 76.9% | 1.1h | 8 |

---

### 💡 The "100% Merge Rate Paradox" & Small-Sample Anomalies

You may occasionally encounter early-stage or viral repositories that display a **100% PR Merge Rate** (such as `ghostty-org/ghostty` or private beta projects). 

**Why does this happen?**
* **Tiny Sample Sizes (Small N)**: If an indexer scans a window where only 2 or 3 external PRs were opened and all 3 were merged, the raw mathematical formula evaluates to `3 / 3 = 100%`.
* **Gated Private Betas**: Before Ghostty went public, contributions were coordinated privately via Discord. Only pre-vetted, author-approved PRs were allowed through.
* **Why Real S-Tier Repos Sit Between 50% and 80%**: In genuine, mature software engineering communities (like `supabase/supabase` at 62.6% or `cline/cline` at 49.4%), a 100% merge rate is practically impossible. Natural noise, failing test suites, duplicate fixes, and out-of-scope RFCs mean that **a healthy, welcoming project accepts between 50% and 80% of external code**. Anything claiming 100% is either tightly gated or mathematically distorted by sample size.

---

## 🌐 The Ecosystem Health Matrix: Language Rankings

Which programming language community treats outside contributors best? We ranked ecosystems with at least 500 indexed repositories by their **Ghost Town Rate** (lowest is best):

| Rank | Language | Total Repos | Ghost Town Rate (D-Tier %) | Avg Merge Rate | Median Turnaround |
| :---: | :--- | :---: | :---: | :---: | :---: |
| 1 | **Go** | 2,953 | **28.4%** | 61.0% | 2.3d |
| 2 | **Java** | 2,291 | **30.6%** | 58.7% | 2.2d |
| 3 | **Rust** | 2,419 | **30.9%** | 60.8% | 2.1d |
| 4 | **PHP** | 1,564 | **36.2%** | 55.1% | 2.3d |
| 5 | **TypeScript** | 2,973 | **36.8%** | 57.2% | 40.2h |
| 6 | **C#** | 1,625 | **39.0%** | 54.6% | 2.3d |
| 7 | **Python** | 3,769 | **39.1%** | 53.9% | 47.7h |
| 8 | **Kotlin** | 1,527 | **39.6%** | 51.9% | 2.3d |
| 9 | **JavaScript** | 2,572 | **40.6%** | 48.6% | 2.9d |
| 10 | **Swift** | 1,307 | **44.8%** | 48.1% | 2.6d |
| 11 | **C++** | 2,343 | **45.2%** | 51.2% | 39.4h |
| 12 | **Shell** | 1,751 | **49.5%** | 44.4% | 39.5h |
| 13 | **Dart** | 1,119 | **52.6%** | 40.7% | 2.0d |
| 14 | **Lua** | 1,095 | **52.7%** | 42.9% | 42.2h |
| 15 | **Julia** | 926 | **60.8%** | 36.7% | 29.4h |
| 16 | **Scala** | 1,016 | **64.0%** | 28.5% | 5.0d |
| 17 | **Elixir** | 1,025 | **70.0%** | 27.1% | 29.1h |
| 18 | **Haskell** | 1,014 | **81.2%** | 18.3% | 15.2h |

### Key Cultural Takeaways:
- **Go & Rust Are the Community Gold Standards**: With ghost rates below 31% and merge rates above 60%, Go and Rust repositories exhibit the strongest maintainer discipline, rapid CI loops, and structured onboarding.
- **The Shell & C++ Stagnation**: Nearly half of Shell (49.5%) and C++ (45.2%) repos are ghost towns. In C++, steep compiler matrices and backwards-compatibility concerns cause maintainers to ignore complex external PRs.
- **Python's High Variance**: Python has the single largest volume of repositories (3,700+), with an average merge rate of 53.9%, but thousands of dormant scripts and unmaintained ML experiments drag its ghost town count to 39.1%.

---

## ⚠️ The Solo Hero Crisis (Bus Factor = 1)

These high-impact software repositories have over 15,000 stars and are critical dependencies, yet telemetry indicates they are maintained almost exclusively by **one individual**:

| Repository | Stars | Language | C-Rank Tier | Merge Rate | Turnaround |
| :--- | :---: | :---: | :---: | :---: | :---: |
| [`react/react`](https://getmerged.abhishekco.de/repo/react/react) | 247,005 | JavaScript | A (61.7) | 33.3% | 14m |
| [`vuejs/vue`](https://getmerged.abhishekco.de/repo/vuejs/vue) | 210,134 | TypeScript | D (8.0) | 0% | Unresponsive / No Comments |
| [`tensorflow/tensorflow`](https://getmerged.abhishekco.de/repo/tensorflow/tensorflow) | 196,890 | C++ | A (66.7) | 80.0% | < 1 min (Instant) |
| [`yt-dlp/yt-dlp`](https://getmerged.abhishekco.de/repo/yt-dlp/yt-dlp) | 180,490 | Python | D (8.4) | 0% | 22.9d |
| [`ollama/ollama`](https://getmerged.abhishekco.de/repo/ollama/ollama) | 177,729 | Go | D (20.0) | 0% | Unresponsive / No Comments |
| [`anthropics/skills`](https://getmerged.abhishekco.de/repo/anthropics/skills) | 164,588 | Python | D (17.6) | 0% | Unresponsive / No Comments |
| [`AUTOMATIC1111/stable-diffusion-webui`](https://getmerged.abhishekco.de/repo/AUTOMATIC1111/stable-diffusion-webui) | 164,294 | Python | D (8.0) | 0% | Unresponsive / No Comments |
| [`firecrawl/firecrawl`](https://getmerged.abhishekco.de/repo/firecrawl/firecrawl) | 160,841 | TypeScript | C (39.4) | 50.0% | 5m |

---

## 🚀 Social Distribution Kit (Ready to Publish)

Use the copy below to syndicate this data drop across developer networks:

### 🧵 1. Twitter / X Viral Thread
```text
1/7 We analyzed 34,000+ GitHub repositories to answer one question: 

Do GitHub stars actually mean a codebase is healthy?

The answer is brutal: 37.6% of real software repos with >20,000 stars are complete Ghost Towns.

Here is the data nobody talks about 🧵👇

2/7 We filtered out curated bookmark lists (awesome-*, free-books, primers) to focus strictly on REAL software projects.

If you pick a 20k+ star repo to open your first PR:
• 37.6% are D-Tier ghost towns (merge rate <15%)
• Only 4.0% are S-Tier welcoming communities
• You are nearly 10x more likely to be ignored than welcomed.

3/7 The 5 Software Ghost Town Traps:
1. The Gerrit Mirror: @golang (135k stars) mirrors to GitHub, but rejects all GitHub PRs.
2. The Sunset Flagship: @vuejs v2 (210k stars) and Create React App (103k stars) are officially abandoned, yet top search results.
3. The Dormant CLI: @ytdl (140k stars) & @thefuck (97k stars) frozen in time.
4. The AI Influx: AUTOMATIC1111 (164k stars) paralyzed by maintainer bottlenecks.
5. The Read-Only Dump: OpenAI Whisper (105k stars) has zero community triage.

4/7 What about 100% merge rates?
If a repo claims a "100% PR merge rate", it’s almost always a small-sample artifact (e.g. 2 out of 2 PRs merged in beta).
In real, healthy communities like @supabase (62.6%) or @cline (49.4%), natural noise means realistic S-Tier acceptance is 50%–80%.

5/7 Which language treats contributors best?
🥇 Go: 28.4% ghost rate, 61% merge rate
🥈 Java: 30.6% ghost rate, 58.7% merge rate
🥉 Rust: 30.9% ghost rate, 60.8% merge rate
...
❌ Shell (49.5%) & C++ (45.2%) have the highest ghost rates in tech.

6/7 We built @GetMerged to fix this: The Glassdoor for open-source.
Before writing a single line of code, get the repo's live C-Rank (S→D), median review turnaround, and merge odds.

Check any repo in 2 seconds: https://getmerged.abhishekco.de

7/7 Read the full Open Source Ghost Town Index (data + methodology):
https://github.com/getmergedapp/getmerged/blob/main/GHOST_TOWN_INDEX.md
```

### 💼 2. LinkedIn Thought Leadership Post
```text
GitHub stars are the most expensive vanity metric in modern software engineering.

Over the past month, our team analyzed telemetry from over 34,000 public GitHub repositories for GetMerged. 

We filtered out reading lists and bookmark repos to focus strictly on real software codebases—compilers, frameworks, developer tools, and libraries.

What we found should change how engineers choose where to contribute:

- 37.6% of real software repos with over 20,000 stars are "D-Tier Ghost Towns". They merge fewer than 15% of external pull requests.
- Only 4% of mega-popular repos qualify as "S-Tier" (reviewing PRs in under 4 hours).
- The "Gerrit Mirror Trap": Flagship projects like Go (golang/go, 135k stars) mirror to GitHub for visibility, but reject all GitHub PRs because review happens on Gerrit. Junior engineers waste thousands of hours opening PRs that are dead on arrival.
- Sunset Flagships: Repos like Create React App (103k stars) and Vue 2 (210k stars) stay at the top of search despite being officially sunset.
- Communities built in Go and Rust have the highest operational discipline in tech (>60% merge rates), while Shell and C++ suffer from severe maintenance drag.

Open source isn't just about stars on a screen; it is about maintainer throughput, human responsiveness, and bus-factor resilience.

We compiled the full findings into the "Open Source Ghost Town Index":
👉 https://github.com/getmergedapp/getmerged/blob/main/GHOST_TOWN_INDEX.md

What has been your experience contributing to high-star open-source repos?
```

### 📰 3. Hacker News: Show HN
```text
Title: Show HN: GetMerged – We analyzed 34k repos; 38% of 20k-star software projects are ghost towns

Link: https://getmerged.abhishekco.de

Text:
Hi HN,

Like many here, I’ve spent weekends fixing bugs in high-star open-source repositories only to have the PR sit in radio silence for 6 months until a merge conflict buried it.

Stars are bookmarks; they don't tell you whether maintainers actually review external code.

To solve this, we built GetMerged (https://getmerged.abhishekco.de). It’s an objective telemetry engine that calculates a C-Rank (S→D) for 34,000+ GitHub repositories based on external PR merge rates, median response times (P50/P90), and bus-factor concentration.

We filtered out curated reading lists (awesome-*, bookmarks, primers) to focus strictly on actual software projects:
https://github.com/getmergedapp/getmerged/blob/main/GHOST_TOWN_INDEX.md

Key findings:
1. 37.6% of real software repos with >20k stars are D-Tier (avg merge rate 13%).
2. Only 4% are S-Tier (median response <2 hours).
3. The 5 Ghost Town Archetypes: Gerrit mirrors (golang/go auto-closing PRs), sunset flagships (create-react-app, vue 2), abandoned viral CLIs (youtube-dl, thefuck), overwhelmed AI hubs (AUTOMATIC1111), and read-only model dumps (whisper).
4. The 100% merge rate paradox: High-star repos with 100% merge rates (like Ghostty in private beta) are almost always small-sample artifacts. Healthy mature communities (Supabase, Cline) sit realistically between 50% and 80%.

We also built a Chrome Extension that injects C-Rank telemetry directly into GitHub repo headers:
https://github.com/getmergedapp/getmerged/tree/main/extension

Would love feedback on our scoring methodology and what signals you look for before contributing!
```
