# Bayesian Analysis of Donner Party Survival

This project examines how age and gender were associated with survival among members of the Donner Party. It was completed as a final project for STAT 3303.

## Overview

The analysis fits three Bayesian binary regression models with different link functions:

- Probit
- Logistic
- Complementary log-log

Posterior inference is performed with a custom random-walk Metropolis sampler in R. Model assessment includes trace plots, acceptance rates, effective sample sizes, posterior summaries, and posterior predictive checks.

Across all three specifications, the posterior estimates suggest that survival probability decreased with age and was lower for males after adjusting for age. These results describe associations in a small historical dataset and should not be interpreted causally.

## Repository contents

- `Stat_3303_Project.qmd` - Quarto source, analysis, and R code
- `Stat_3303_Project_polish.pdf` - rendered final report

## Requirements

To render the report, install [Quarto](https://quarto.org/) and the following R packages:

```r
install.packages(c(
  "LearnBayes",
  "MCMCpack",
  "rstanarm",
  "dplyr",
  "tidyr",
  "knitr",
  "ggplot2"
))
```

Then run:

```bash
quarto render Stat_3303_Project.qmd
```

## Data and references

The analysis uses the `donner` dataset distributed with the `LearnBayes` R package. Background literature and course materials used during development are not redistributed in this repository.

## Author

Jayking Wu
