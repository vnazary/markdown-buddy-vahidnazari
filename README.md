# Technical Analysis of a Synthetic Stock in R

An R project that calculates moving averages and the Relative Strength Index (RSI) on one year of simulated daily stock prices, flags crossover signals, and charts the results.

> [!NOTE]
> For learning purposes only. The data is synthetic and nothing here is investment advice.

## Table of Contents

- [Overview](#overview)
- [Data](#data)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Example Code](#example-code)
- [Outputs](#outputs)
- [License](#license)
- [Author](#author)

## Overview

The project computes three common technical indicators:

- **20-day SMA**: short-term trend
- **50-day SMA**: longer-term trend
- **14-day RSI**: momentum (above 70 often read as overbought, below 30 as oversold)

A **buy signal** is flagged when the 20-day SMA crosses above the 50-day SMA, and a **sell signal** when it crosses below.

## Data

Synthetic closing prices for a fictional ticker, `DEMO`, over 250 trading days, generated with a random walk. `set.seed()` makes the results reproducible.

| Column  | Type   | Description                   |
|---------|--------|-------------------------------|
| `date`  | Date   | Trading day                   |
| `close` | number | Simulated closing price (USD) |

## Project Structure

```
markdown-buddy-vahidnazari/
├── README.md                 # Project documentation
├── technical_analysis.R      # Generates data, calculates indicators, plots charts
├── technical_analysis.Rmd    # R Markdown report documenting the script
├── Reflection.md             # Reflection questions
└── Appendix.md               # AI prompts and key responses
```

## Installation

1. Install R 4.0 or later, and optionally RStudio or Posit Cloud.
2. Clone the repository:

   ```bash
   git clone https://github.com/<your-username>/markdown-buddy-vahidnazari.git
   ```

3. Install the required packages in R:

   ```r
   install.packages(c("TTR", "dplyr", "ggplot2", "rmarkdown", "knitr"))
   ```

## Example Code

Run the analysis from the project folder:

```r
source("technical_analysis.R")
```

Knit the documentation report to HTML:

```r
rmarkdown::render("technical_analysis.Rmd")
```

## Outputs

- Price chart with the 20-day and 50-day SMAs and crossover signals
- RSI chart with reference lines at 30 and 70
- Summary table of buy and sell signals

## License

Released under the [MIT License](LICENSE).

## Author

**Vahid Nazari**  
BDA400 Data Science Tools and Techniques
