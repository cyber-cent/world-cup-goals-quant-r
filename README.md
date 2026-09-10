# FIFA World Cup Over 1.5 Goals — Quantitative Research in R

**Author:** Busari Aliu Oluwaseyi

## Research question
Does the Over 1.5 Goals outcome demonstrate a historically persistent high-frequency pattern in FIFA World Cup matches?

## Dataset
The analysis uses match-level World Cup data covering 1930–2022. The working dataset should be placed at `data/matches_1930_2022.csv`.

> Data provenance: the supplied match CSV is treated as the analysis dataset. Tournament-level historical figures were cross-checked against World Cup History. This repository does not claim the supplied CSV is an official FIFA dataset without separate verification.

## Main result
Across **964 matches**, **704** recorded at least two goals, giving an observed Over 1.5 rate of **73.03%**. A simple 95% Wald confidence interval is approximately **70.23%–75.83%**.

This is a historical frequency estimate, not a guaranteed future probability or proof of betting profitability.

## Project structure
```text
world-cup-goals-quant-r/
├── data/
│   └── matches_1930_2022.csv
├── R/
│   ├── 01_clean_data.R
│   ├── 02_descriptive_analysis.R
│   ├── 03_visualizations.R
│   └── 04_statistical_analysis.R
├── figures/
├── results/
└── report/
    └── world_cup_over15_report.qmd
```

## Run
Install the packages once:

```r
install.packages(c("tidyverse", "scales"))
```

Then run the scripts from the repository root in order:

```r
source("R/01_clean_data.R")
source("R/02_descriptive_analysis.R")
source("R/03_visualizations.R")
source("R/04_statistical_analysis.R")
```

## Quant-finance interpretation
The research is intentionally framed as an empirical signal study. Historical frequency alone does not establish an exploitable market edge. A next-stage model should incorporate bookmaker odds, implied probabilities, margin, match-specific features, and strict time-based out-of-sample validation.

For decimal odds `O` and a properly estimated match-specific probability `p`, expected value is:

`EV = p * O - 1`

## License
MIT
