# Premier League Index

**A descriptive ranking model for Premier League players.**

## → [Open the site](https://raffaeleciccone-analyst.github.io/premier-league-index/)

---

The TPI ranks qualified Premier League players by attacking impact: xG and xA adjusted for
opponent difficulty, seven dimensions, one ranking. It is **descriptive** — it ranks,
it does not predict — and the checks say where it loses too.

### Same engine, second league

This site is not a second project. It is the same engine as the
[Serie A Scout Index](https://raffaeleciccone-analyst.github.io/serie-a-index/), pointed at a
different competition: the league is a parameter, like the season. No fork, no second copy to
keep in step — one correction stays one correction.

That matters for reading the two indices side by side. The seven weights are a declared choice,
not a fit to Italian data, so they are applied identically here; what changes is the data, the
site's starting language, and the checks that cannot be run outside Italy.

Those checks are **declared, not omitted**. Two of the fifteen lean on Italian-only sources — a
fantasy-football rating and a hand-written reference list — and the validation page says so in
place, rather than quietly publishing thirteen and calling it fifteen.

| Page | What it is |
|---|---|
| [Homepage](https://raffaeleciccone-analyst.github.io/premier-league-index/) | What the index is, who is on top right now |
| [Ranking](https://raffaeleciccone-analyst.github.io/premier-league-index/dashboard_premier_league.html) | Every qualified player, five contexts, head-to-head |
| [Validation](https://raffaeleciccone-analyst.github.io/premier-league-index/validazione.html) | What holds up and what does not, with confidence intervals |
| [Method](https://raffaeleciccone-analyst.github.io/premier-league-index/guida_completa.html) | Every formula the engine actually runs |
| [Data (CSV)](https://raffaeleciccone-analyst.github.io/premier-league-index/premier_league_tpi_2025-26.csv) | Every qualified player, every column the engine writes, refreshed on every run |

**Seven dimensions** — output, buildup, centrality, team boost, consistency, finishing,
recent form. **Five contexts** — overall, home, away, vs top six, vs the tightest defences.

The ranking page publishes the top 100 by default and loads every qualified player on request.
The top-100 cut is not a neutral filter: the index rewards players who produce in teams that
produce, so the list leans towards the sides at the top of the table. Players beyond the hundred
come without the per-matchday series, and the page says so.

Every season the engine has measured stays on file, in the selector above the ranking, plus a
combined view across all of them. The combined view is not a season: it is the same measure over
more minutes, so the estimates are steadier and the ranking belongs to no single year. The page
says that too — and when a season is still being played, it says how many matchdays it has.

Counts and season names are deliberately absent from this file. They live on the pages, which
are generated from the data, so nothing here can go stale behind them. The one exception is the
CSV link above, which has to name a file.

---

### The engine

The model, the validation suite and the data-quality machinery live in
**[serie-a-index-engine](https://github.com/raffaeleciccone-analyst/serie-a-index-engine)**.
This repository holds the published site only: HTML, the payloads the pages read, and the CSV.

Everything on these pages is generated. No number is typed by hand, which is the only way the
site and the data cannot drift apart.

---

*Raffaele Ciccone — data analyst.
[Portfolio](https://raffaeleciccone-analyst.github.io/) ·
[LinkedIn](https://www.linkedin.com/in/raffaele-ciccone-9528603a9)*
