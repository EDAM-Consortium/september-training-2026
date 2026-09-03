# EDAM Training

Materials for the EDAM September 2026 training.

## What to download

Clone or download this whole repository, then open the `.Rmd` file for the session you're working on **inside that session's own folder**:

- `session_1/session_1_EXERCISES.Rmd`: work through this one yourself. Needs `session_1/data/*`.
- `session_1/session_1_SOLUTIONS.Rmd`: the worked answer key for session 1, sharing the same `session_1/data/`. This is published on the course site (see below).
- `session_2/xgboost_shap_workflow_tutorial.Rmd`: the session 2 tutorial published on the course site (see below). 

You can also read the rendered session 1 (solutions) and session 2 walkthrough online (no R required) via the published [course site](https://edam-consortium.github.io/september-training-2026/).

## Setup
This repo uses [renv](https://rstudio.github.io/renv/) to pin package versions. If you're familiar with it, after cloning, open the project in your desired IDE and run:

```r
renv::restore()
```

> [!NOTE]
> `renv` needs to be installed. If it's not, please install it using:
> `install.packages('renv')`

> [!WARNING]
> Installing packages without an active `renv` environment installs them into your base R library, which can upgrade or downgrade packages you already have and affect other projects on your machine. We recommend creating a project-specific `renv` using `renv::activate()` if you haven't already, and activating the environment before running `renv::restore()` above, so installs stay isolated to this project instead.

If you're not familiar with `renv`, you can instead install the required packages directly. Open RStudio and run the code below in the Console:

```r
install.packages(c(
  "tidyverse",   # includes dplyr, ggplot2, readr, tidyr, stringr, forcats, lubridate
  "sf",          # spatial data handling (Session 1)
  "patchwork",   # combining ggplot figures (Session 1)
  "scales",      # axis and legend formatting (Session 1)
  "anthro",      # WHO child growth standards (Session 1)
  "tidymodels",  # modelling workflow (Session 2)
  "xgboost",     # gradient-boosted tree models (Session 2)
  "shapviz"      # SHAP value visualisation (Session 2)
))
```

To check that all the packages installed correctly, run:

```r
packages <- c(
  "tidyverse", "sf", "patchwork", "scales",
  "anthro", "tidymodels", "xgboost", "shapviz"
)
installed <- unname(sapply(packages, requireNamespace, quietly = TRUE))
data.frame(package = packages, installed = installed)
```