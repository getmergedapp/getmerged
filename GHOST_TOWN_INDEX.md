# The Open Source Ghost Town Index (2026 Edition)
### We Analyzed 34,175 GitHub Repositories. Here Is Why 38% of Mega-Popular Projects Are Ghost Towns.

*By the [GetMerged](https://getmerged.abhishekco.de) Research Team · Updated September 2026*

---

## Executive Summary

For over fifteen years, the primary currency of trust in software engineering has been the **GitHub Star**. Developers star repositories they admire, recruiters scan stars to assess candidates, and ambitious engineers spend hundreds of hours writing code for high-star repositories expecting recognition.

**The data reveals that GitHub stars are a dangerously misleading vanity metric.**

After ingesting and analyzing telemetry across **34,175 public repositories** using the [GetMerged C-Rank™ Engine](https://getmerged.abhishekco.de):

1. **37.6% of repositories with >20,000 stars are D-Tier Ghost Towns**: They merge less than 15% of external contributions, and median pull requests sit unacknowledged for weeks or months.
2. **Only 4.0% of mega-popular repos achieve S-Tier**: The vast majority of high-star repositories operate with extreme gatekeeping or complete maintainer burnout.
3. **Language Culture Dictates Contributor Experience**: **Go** and **Rust** maintainers run the healthiest communities in tech (only ~28-30% ghost rate, >60% average merge rate), while **Shell** (49.5% ghost rate), **C++** (45.2%), and **JavaScript** (40.6%) leave the highest percentage of PRs to die.
4. **The Solo Hero Crisis**: Hundreds of repositories with over 15,000 stars depend entirely on **a single active maintainer**, creating catastrophic bus factor risk for the entire software supply chain.

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

> **The Contributor Takeaway**: If you pick a repository with 20k+ stars at random to submit your first open-source PR, **you are nearly 10x more likely to land in a Ghost Town (37.6%) than an S-Tier community (4.0%)**.

---

## 💀 The Hall of Shame: Top Mega-Star Ghost Towns

These repositories possess tens or hundreds of thousands of stars, yet maintainers rarely or never review external pull requests:

| Repository | Stars | Language | C-Rank Score | External Merge Rate | Review Responsiveness |
| :--- | :---: | :---: | :---: | :---: | :---: |
| [`public-apis/public-apis`](https://getmerged.abhishekco.de/repo/public-apis/public-apis) | 452,899 | Python | 7.2/100 | 0% | Never / Unresponsive |
| [`EbookFoundation/free-programming-books`](https://getmerged.abhishekco.de/repo/EbookFoundation/free-programming-books) | 393,480 | Python | 8.0/100 | 0% | Never / Unresponsive |
| [`nilbuild/developer-roadmap`](https://getmerged.abhishekco.de/repo/nilbuild/developer-roadmap) | 362,893 | TypeScript | 7.2/100 | 0% | Never / Unresponsive |
| [`donnemartin/system-design-primer`](https://getmerged.abhishekco.de/repo/donnemartin/system-design-primer) | 359,418 | Python | 17.6/100 | 0% | Never / Unresponsive |
| [`practical-tutorials/project-based-learning`](https://getmerged.abhishekco.de/repo/practical-tutorials/project-based-learning) | 276,273 | Python | 7.2/100 | 0% | Never / Unresponsive |
| [`TheAlgorithms/Python`](https://getmerged.abhishekco.de/repo/TheAlgorithms/Python) | 223,217 | Python | 8.0/100 | 0% | Never / Unresponsive |
| [`vuejs/vue`](https://getmerged.abhishekco.de/repo/vuejs/vue) | 210,134 | TypeScript | 8.0/100 | 0% | Never / Unresponsive |
| [`mattpocock/skills`](https://getmerged.abhishekco.de/repo/mattpocock/skills) | 203,890 | Shell | 29.9/100 | 7.1% | 21.1h |
| [`trekhleb/javascript-algorithms`](https://getmerged.abhishekco.de/repo/trekhleb/javascript-algorithms) | 196,341 | JavaScript | 8.0/100 | 0% | Never / Unresponsive |
| [`yt-dlp/yt-dlp`](https://getmerged.abhishekco.de/repo/yt-dlp/yt-dlp) | 180,490 | Python | 8.4/100 | 0% | 22.9d |

*Why do mega-star repos become ghost towns?*
1. **Curated Lists & Static Bookmarks**: Projects like `system-design-primer` or `free-programming-books` amass stars as bookmarks, not active software codebases. Pull requests adding resources routinely languish.
2. **Archived / Dormant Version Branches**: Projects like `vuejs/vue` retain 210k+ stars from Vue 2, but all development moved to `vuejs/core`. New contributors waste hours opening PRs to the legacy repo.
3. **Maintainer Burnout**: A library hits viral fame, the creator is overwhelmed by 500 issues/week, and without a funded maintenance team, they shut down external reviews.

---

## 🌟 The Hall of Fame: Open Source S-Tier Champions

These open-source teams manage tens of thousands of stars *and* maintain relentless review speed, welcoming first-time contributors with world-class discipline:

| Repository | Stars | Language | C-Rank Score | External Merge Rate | Median Review | Active Maintainers |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| [`open-webui/open-webui`](https://getmerged.abhishekco.de/repo/open-webui/open-webui) | 147,512 | Python | 82.7/100 | 1.7% | 1m | 16 |
| [`supabase/supabase`](https://getmerged.abhishekco.de/repo/supabase/supabase) | 107,158 | TypeScript | 74.4/100 | 62.6% | 1m | 11 |
| [`unionlabs/union`](https://getmerged.abhishekco.de/repo/unionlabs/union) | 73,867 | Rust | 70.5/100 | 100.0% | 22.5h | 2 |
| [`OpenBB-finance/OpenBB`](https://getmerged.abhishekco.de/repo/OpenBB-finance/OpenBB) | 71,092 | Python | 70.4/100 | 58.3% | 1m | 4 |
| [`base/node`](https://getmerged.abhishekco.de/repo/base/node) | 68,467 | Shell | 71.0/100 | 16.5% | 1m | 9 |
| [`cline/cline`](https://getmerged.abhishekco.de/repo/cline/cline) | 65,623 | TypeScript | 72.0/100 | 49.4% | 1m | 21 |
| [`commaai/openpilot`](https://getmerged.abhishekco.de/repo/commaai/openpilot) | 63,320 | Python | 70.6/100 | 53.4% | 1.0h | 9 |
| [`upstash/context7`](https://getmerged.abhishekco.de/repo/upstash/context7) | 60,116 | TypeScript | 81.4/100 | 59.0% | 6.2h | 5 |
| [`ghostty-org/ghostty`](https://getmerged.abhishekco.de/repo/ghostty-org/ghostty) | 59,272 | Zig | 72.7/100 | 100.0% | 42m | 1 |
| [`FlowiseAI/Flowise`](https://getmerged.abhishekco.de/repo/FlowiseAI/Flowise) | 54,972 | TypeScript | 70.6/100 | 56.2% | 1m | 1 |

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

### Key Cultural Insights:
- **Go & Rust Are Community Gold Standards**: With ghost rates below 31% and merge rates above 60%, Go and Rust repositories exhibit the strongest maintainer discipline, rapid CI loops, and structured onboarding.
- **The Shell & C++ Stagnation**: Nearly half of Shell (49.5%) and C++ (45.2%) repos are ghost towns. In C++, steep compiler matrices and backwards-compatibility concerns cause maintainers to ignore complex external PRs.
- **Python's High Variance**: Python has the single largest volume of repositories (3,700+), with an average merge rate of 53.9%, but bookmarks and educational repos drag its ghost town count to 39.1%.

---

## ⚠️ The Solo Hero Crisis (Bus Factor = 1)

These high-impact repositories have over 15,000 stars and are critical dependencies, yet telemetry indicates they are maintained almost exclusively by **one individual**:

| Repository | Stars | Language | C-Rank Tier | Merge Rate | Turnaround |
| :--- | :---: | :---: | :---: | :---: | :---: |
| [`public-apis/public-apis`](https://getmerged.abhishekco.de/repo/public-apis/public-apis) | 452,899 | Python | D (7.2) | 0% | Never / Unresponsive |
| [`EbookFoundation/free-programming-books`](https://getmerged.abhishekco.de/repo/EbookFoundation/free-programming-books) | 393,480 | Python | D (8.0) | 0% | Never / Unresponsive |
| [`nilbuild/developer-roadmap`](https://getmerged.abhishekco.de/repo/nilbuild/developer-roadmap) | 362,893 | TypeScript | D (7.2) | 0% | Never / Unresponsive |
| [`donnemartin/system-design-primer`](https://getmerged.abhishekco.de/repo/donnemartin/system-design-primer) | 359,418 | Python | D (17.6) | 0% | Never / Unresponsive |
| [`practical-tutorials/project-based-learning`](https://getmerged.abhishekco.de/repo/practical-tutorials/project-based-learning) | 276,273 | Python | D (7.2) | 0% | Never / Unresponsive |
| [`react/react`](https://getmerged.abhishekco.de/repo/react/react) | 247,005 | JavaScript | A (61.7) | 33.3% | 14m |
| [`TheAlgorithms/Python`](https://getmerged.abhishekco.de/repo/TheAlgorithms/Python) | 223,217 | Python | D (8.0) | 0% | Never / Unresponsive |
| [`vuejs/vue`](https://getmerged.abhishekco.de/repo/vuejs/vue) | 210,134 | TypeScript | D (8.0) | 0% | Never / Unresponsive |

---

## 🚀 Social Distribution Kit (Ready to Publish)

Use the copy below to syndicate this data drop across developer networks:

### 🧵 1. Twitter / X Viral Thread
```text
1/7 We analyzed 34,000+ GitHub repositories to answer one question: 

Do GitHub stars actually mean a project is healthy?

The answer is brutal: 37.6% of repos with >20,000 stars are complete Ghost Towns.

Here is the data nobody talks about 🧵👇

2/7 If you pick a 20k+ star repo to open your first PR:
• 37.6% are D-Tier ghost towns (merge rate <15%)
• Only 4.0% are S-Tier welcoming communities
• You are nearly 10x more likely to be ignored than welcomed.

Stars are bookmarks. They tell you nothing about whether someone is home.

3/7 The Hall of Shame (Mega Ghost Towns):
• System Design Primer: 359k stars, 0% external merge rate
• Free Programming Books: 393k stars, dormant PR queue
• Vue 2 (vuejs/vue): 210k stars, abandoned branch while development moved to core

4/7 Which language treats contributors best?
🥇 Go: 28.4% ghost rate, 61% merge rate
🥈 Java: 30.6% ghost rate, 58.7% merge rate
🥉 Rust: 30.9% ghost rate, 60.8% merge rate
...
❌ Shell (49.5%) & C++ (45.2%) have the highest ghost rates in tech.

5/7 The Solo Hero Problem:
Dozens of libraries powering Fortune 500 apps have 20k+ stars and a bus factor of exactly ONE. If that creator gets sick or burnt out, millions of downstream builds freeze.

6/7 We built @GetMerged to fix this: The Glassdoor for open-source.
Before writing a line of code, get the repo's live C-Rank (S→D), P50 review turnaround, and merge odds.

Check any repo in 2 seconds: https://getmerged.abhishekco.de

7/7 Read the full Open Source Ghost Town Index (data + methodology):
https://github.com/getmergedapp/getmerged/blob/main/GHOST_TOWN_INDEX.md
```

### 💼 2. LinkedIn Thought Leadership Post
```text
GitHub stars are the most expensive vanity metric in modern software engineering.

Over the past month, our team analyzed telemetry from over 34,000 public GitHub repositories for GetMerged. 

What we found should change how engineers pick open-source projects:

- 37.6% of repositories with over 20,000 stars are "D-Tier Ghost Towns". They merge fewer than 15% of external pull requests.
- Only 4% of mega-popular repos qualify as "S-Tier" (reviewing PRs in under 4 hours).
- A developer is nearly 10 times more likely to have their weekend PR completely ignored on a 20k-star repo than to have it merged.
- Communities built in Go and Rust have the highest operational discipline in tech (>60% merge rates), while Shell and C++ suffer from severe maintenance drag.

Open source isn't just about lines of code; it is about maintainer throughput, human responsiveness, and bus-factor resilience.

We compiled the full findings into the "Open Source Ghost Town Index":
👉 https://github.com/getmergedapp/getmerged/blob/main/GHOST_TOWN_INDEX.md

What has been your experience contributing to high-star open-source repos?
```

### 📰 3. Hacker News: Show HN
```text
Title: Show HN: GetMerged – We analyzed 34k repos; 38% of 20k-star projects are ghost towns

Link: https://getmerged.abhishekco.de

Text:
Hi HN,

Like many here, I’ve spent weekends fixing bugs in high-star open-source repositories only to have the PR sit in radio silence for 6 months until a merge conflict buried it.

Stars are bookmarks; they don't tell you whether maintainers actually review external code.

To solve this, we built GetMerged (https://getmerged.abhishekco.de). It’s an objective telemetry engine that calculates a C-Rank (S→D) for 34,000+ GitHub repositories based on:
- External PR merge rates
- Median review turnaround times (P50/P90)
- First-timer PR acceptance probability
- Bus factor & maintainer concentration

We just published the findings from our dataset in the Open Source Ghost Town Index:
https://github.com/getmergedapp/getmerged/blob/main/GHOST_TOWN_INDEX.md

Some surprising takeaways:
1. 37.6% of repos with >20k stars are D-Tier (avg merge rate 13%).
2. Only 4% are S-Tier (median response <2 hours).
3. Go and Rust have the highest merge discipline (~61%), while C++ and Shell have the highest ghost rates (~45-50%).

We also built a Chrome Extension that injects C-Rank telemetry directly into GitHub repo headers:
https://github.com/getmergedapp/getmerged/tree/main/extension

Would love feedback on our scoring methodology and what signals you look for before contributing!
```
