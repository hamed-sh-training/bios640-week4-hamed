# BIOS 640 Week 4 Exercise - Hamed

This repository contains the Hamed (A-series) solution for the BIOS 640 Week 4 exercise. It builds on the cleaned NHANES data and the Week 3 R Markdown report to demonstrate GitHub version control, interactive R Markdown output, a `flexdashboard`, and formatted statistical tables.

## Repository structure

- `code/week3/`: original Week 3 A-series R Markdown source.
- `code/week4/`: the interactive HTML report, dashboard, and complex-table report sources.
- `data/`: cleaned NHANES data and the diet example data used by the Week 3 report.
- `figures/`: figures saved during Week 3 and Week 4.
- `outputs/week3-original/`: the original Week 3 PDF report.
- `outputs/week3-html/`: the updated interactive HTML report.
- `outputs/dashboard/`: the rendered NHANES dashboard.
- `outputs/tables/`: the rendered PDF table report.
- `references/`: BibTeX citation used by the PDF report.

## Exercise 1

The project is organized in a public GitHub repository with data, code, figures, references, and rendered reports stored in separate folders. The commit history records the original Week 3 materials, the branch-based HTML conversion, and the remaining Week 4 outputs.

## Exercise 2

`code/week4/NHANES_week3_interactive.Rmd` converts the Week 3 report to HTML. It uses a theme and syntax highlighting, a floating table of contents, tabbed sections in Exercise 1, and a `DT` table at the start of Exercise 2. The rendered file is `outputs/week3-html/NHANES_week3_interactive.html`.

## Exercise 3

`code/week4/NHANES_dashboard.Rmd` creates a row-oriented dashboard. The top row displays a saved Week 3 figure. The bottom row reports the percentage of participants aged 21 years or older and the percentage with average systolic blood pressure above 120 mm Hg. The rendered dashboard is `outputs/dashboard/NHANES_dashboard.html`.

## Exercise 4

`code/week4/NHANES_tables_Hamed.Rmd` creates a short PDF report with formatted tables for wave sample sizes, male counts and percentages, ethnicity counts and percentages, and average systolic blood-pressure summaries. Its bibliography is stored in `references/references.bib`. The rendered report is `outputs/tables/NHANES_tables_Hamed.pdf`.

## Reproducing the outputs

1. Clone this repository and open `BIOS640-Week4-Hamed.Rproj` in RStudio.
2. Keep the repository structure unchanged so that `here()` resolves the data and figure paths.
3. Open any `.Rmd` file in `code/week4/` and click **Knit**. The setup chunks use `pacman::p_load()` to load or install the required packages.
4. To reproduce the supplied folder layout exactly, render from the project root with:

```r
rmarkdown::render(
  "code/week4/NHANES_week3_interactive.Rmd",
  output_dir = "outputs/week3-html"
)

rmarkdown::render(
  "code/week4/NHANES_dashboard.Rmd",
  output_dir = "outputs/dashboard"
)

rmarkdown::render(
  "code/week4/NHANES_tables_Hamed.Rmd",
  output_dir = "outputs/tables"
)
```

The rendered outputs are committed with their source files so the work can be reviewed without rerunning the analyses.
