# GBV Detection Analysis

Bayesian GLMM analyses and manuscript figures in R, rendered with Quarto (see `scripts/1_analysis.qmd`).

## Folder structure

```text
analysis/
  data/                  # Raw spreadsheets (local only; not committed)

outputs/
  models/                # Cached brms model fits (.rds) from 1_analysis.qmd
  plots/                 # Manuscript figure PNGs (600 dpi), committed

scripts/
  1_analysis.qmd         # Main Quarto analysis document (source + render target)

.gitignore
project.Rproj
```

## Quick start

- Open `scripts/1_analysis.qmd` and **Render** (Quarto) from the IDE (RStudio / VS Code / Cursor).
- Place raw data files under `analysis/data/` (not committed) before rendering.

## Outputs

- **Models**: `scripts/1_analysis.qmd` saves cached fits under `outputs/models/` (`.rds` files).
- **Figures**: effect and qPCR plots are written to `outputs/plots/` at **600 dpi** (same dimensions as in the rendered Quarto HTML). This folder is part of the repo so manuscript figures are available without re-running the models.

## Dependencies

- The setup chunk in `scripts/1_analysis.qmd` installs any missing R packages required to run the analysis.
- Bayesian models are fit with `brms` using the `cmdstanr` backend; ensure CmdStan is available and the path in the setup chunk is correct for your machine.

