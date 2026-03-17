# Netflix Engagement Analysis

**Tools:** R · ggplot2 · tidyverse · R Markdown · Tableau
**Data source:** [TidyTuesday — Netflix Engagement Report (July 2025)](https://github.com/rfordatascience/tidytuesday/tree/main/data/2025/2025-07-29)

---

## Overview

This end-to-end case study analyzes Netflix's official first-half 2025 engagement
report to uncover what drives viewership across movies and TV shows. The analysis
follows the Google Data Analytics framework — Ask, Prepare, Process, Analyze,
Share, and Act — and produces both a polished PDF report and Tableau-ready CSV
exports for interactive dashboarding.

---

## Business Questions

1. Which titles drove the most engagement by hours viewed?
2. How do Movies and TV Shows compare in total hours viewed and view counts?
3. Does global availability significantly impact engagement?
4. How does release month relate to viewership volume?
5. Is there a relationship between runtime and hours viewed — and does it differ between movies and TV shows?

---

## Key Findings

- **TV shows accumulate more total hours** than movies despite movies making up
  a larger share of titles — serialized content compounds engagement across
  episodes and seasons.
- **Global availability is a measurable advantage.** Globally available titles
  substantially outperform non-global titles in both hours viewed and view counts,
  with the gap especially pronounced for TV shows.
- **Q1 is the highest-viewership window.** January releases in particular stand
  out, consistent with Netflix front-loading tent-pole content after the holidays.
- **Runtime predicts engagement differently by type.** For movies, runtime and
  hours viewed are uncorrelated. For TV shows, longer cumulative runtimes
  (more episodes/seasons) correlate positively with total hours viewed.

---

## Visualizations

| Chart | Description |
|---|---|
| Top 10 Titles by Hours Viewed | Horizontal bar chart ranked by hours viewed, colored by content type |
| Movies vs. TV Shows | Side-by-side bars comparing total hours viewed and total views |
| Global vs. Non-Global | Faceted bar chart showing the engagement gap by availability |
| Viewership by Release Month | Monthly breakdown of total hours by content type |
| Runtime vs. Engagement | Faceted scatter plots (one per content type) with linear trend lines |

---

## Repository Structure

```
netflix-engagement-analysis/
├── notebooks/
│   ├── analysis.Rmd       # Full annotated R Markdown report
│   └── analysis.pdf       # Rendered PDF output
└── data/
    └── tableau/           # CSV exports for Tableau dashboards
        ├── all_content.csv
        ├── monthly_summary.csv
        ├── global_summary.csv
        ├── top_50_titles.csv
        └── type_summary.csv
```

---

## How to Run

1. Clone the repository.
2. Open `notebooks/analysis.Rmd` in RStudio.
3. Install dependencies if needed:
   ```r
   install.packages(c("tidyverse", "knitr", "scales"))
   ```
4. Click **Knit** to render the PDF report. The Tableau CSVs will be exported
   to `data/tableau/` automatically.

---
