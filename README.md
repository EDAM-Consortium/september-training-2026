# EDAM Training

Training materials for the EDAM course.

## What to download

Clone or download this whole repository, then open the `.Rmd` file for the session you're
working on **inside that session's own folder**:

- `session_1/session_1_EXERCISES.Rmd` — work through this one yourself. Needs `session_1/data/`
  alongside it (relative paths).
- `session_1/session_1_SOLUTIONS.Rmd` — the worked answer key for session 1, sharing the same
  `session_1/data/`. Also published on the course site (see below) — try the exercises first.
- `session_2/xgboost_shap_workflow_tutorial.Rmd` — needs the CSVs/PNG alongside it in
  `session_2/`.

You can also read the rendered session 1 (solutions) and session 2 walkthrough online (no R required) via
the published course site.

## `instructor/`

The `instructor/` folder is course-prep material (data generation scripts, old drafts/backups)
- not part of the training. Ignore it.

## Setup

This project uses [renv](https://rstudio.github.io/renv/) to pin package versions. After
cloning, open the project in your desired IDE and run:

```r
renv::restore()
```

> [!NOTE]
> `renv` needs to be installed. If it's not, please install it using:
> `install.packages('renv')`