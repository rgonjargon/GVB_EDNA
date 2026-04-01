# GBV Detection Analysis

Bayesian GLMM analyses and manuscript figures in R, rendered with Quarto (see `scripts/1_analysis.qmd`).

## Folder structure

```text
analysis/                # Input data (local)
  data/                  # Raw spreadsheets (git-ignored)

outputs/
  models/                # Cached brms model fits (git-ignored)
  plots/                 # Rendered figure images (git-ignored)

scripts/
  1_analysis.qmd         # Main Quarto analysis document (source + render target)

.gitignore
project.Rproj
```

## Quick start

- Open `scripts/1_analysis.qmd` and **Render** (Quarto) from the IDE (RStudio / VS Code / Cursor).
- Place raw data files under `analysis/data/` (not committed) before rendering.

## Outputs

- **Models**: `scripts/1_analysis.qmd` writes cached model objects under `outputs/models/`.
- **Figures**: effect plots are saved under `outputs/plots/` at **600 dpi** with the same dimensions as rendered in the Quarto HTML.

## Dependencies

- The setup chunk in `scripts/1_analysis.qmd` installs any missing R packages required to run the analysis.
- Bayesian models are fit with `brms` using the `cmdstanr` backend; ensure CmdStan is available and the path in the setup chunk is correct for your machine.

