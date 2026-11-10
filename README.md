# Agentná AI v praxi sociálnej vedy

Materiály k workshopu o práci s Claude Code v kvantitatívnej sociálnej vede.
Prezentácia: [`claude_code_workshop.pdf`](claude_code_workshop.pdf).

## Čo budete potrebovať

1. **R** — <https://cran.r-project.org>
2. **Vývojové prostredie (IDE)** — [Positron](https://positron.posit.co),
   [RStudio](https://posit.co/download/rstudio-desktop/) alebo
   [VS Code](https://code.visualstudio.com)
3. **Predplatné Claude Code alebo porovnateľnej služby** (agent, ktorý pracuje v termináli
   vo vašom priečinku) — inštalácia Claude Code:
   <https://code.claude.com/docs/en/setup>
4. **R balíky `tidyverse`, `gssr` a `gssrdoc`** — dáta General Social Survey a ich codebook

## Inštalácia balíkov

Balíky `gssr` a `gssrdoc` nie sú na CRAN-e; inštalujú sa z R-universe:

```r
install.packages(
  c("gssr", "gssrdoc"),
  repos = c("https://kjhealy.r-universe.dev", "https://cloud.r-project.org")
)
```

Overenie, že všetko funguje:

```r
library(gssr)
library(gssrdoc)

data(gss_all)   # kumulatívny súbor GSS
data(gss_doc)   # codebook
```

V ukážkach používame aj `tidyverse`:

```r
install.packages("tidyverse")
```

## Článok na replikáciu

Článok Mondak a Sanders (2003) nie je voľne dostupný, preto nie je súčasťou repozitára.
Postup nájdete v [`replication_paper/README.md`](replication_paper/README.md).

## Spustenie agenta

Otvorte tento priečinok vo svojom IDE, otvorte terminál a napíšte:

```bash
claude
```
