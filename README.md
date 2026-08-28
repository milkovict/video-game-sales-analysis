# Video Game Sales and Ratings Analysis

Statistical analysis of 16,719 video games examining the 
relationship between critic scores, user scores, and global sales.
Written in R and Quarto.

**[View the rendered report](https://https://milkovict.github.io/video-game-sales-analysis/)** | [PDF](Seminar.pdf)

## Questions

- Do critics and players agree on the same games?
- Do genres differ in quality?
- Do better-rated games actually sell more?

## Key findings

- Critics rate games on average 1.57 points lower than players.
  Statistically significant (n = 7,017), but small in practice:
  individual disagreements reach over 60 points.
- Sports games score about 6 points higher than Action games (Welch t-test).
- 32% of highly rated games (score >= 75) sell over a million copies,
  versus 9% of the rest.
- Critic score correlates positively with log sales (r = 0.36) but
  explains only 13% of variance. Quality relates to commercial success
  without guaranteeing it.

## Methods

One-sample and Welch t-tests, paired t-test, two-proportion test,
Pearson correlation, linear regression with residual diagnostics.
Sales were log-transformed because the raw distribution
is heavily right-skewed.

## Data

[Video Game Sales with Ratings](https://www.kaggle.com/datasets/rush4ratio/video-game-sales-with-ratings)
(Kaggle, snapshot from 22 December 2016). Download `sales.csv` into
the project root to reproduce.

## Running

`quarto render seminar.qmd`

Requires R with `dplyr`, `viridisLite`, `knitr`.

## Note

AI tools were used for editing and phrasing throughout, and for
drafting the written interpretation in the correlation and
regression sections (3.6.2 and 3.6.3). All code, statistical
choices, and the remaining analysis are my own.
