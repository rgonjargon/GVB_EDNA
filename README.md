# 241206_Justine

Project for R analyses and manuscript figures rendered with Quarto.

## Folder structure

```text
analysis/                # Data and generated pipeline outputs
  data/                  # Raw spreadsheets (git-ignored)
  output/
    models/              # Cached brms model fits (git-ignored)

outputs/
  plots/                 # Rendered figure images (git-ignored)

scripts/
  1_analysis.qmd         # Main Quarto analysis document (source + render target)

.gitignore
241206_Justine.Rproj
```

## Quick start

```bash
quarto render scripts/1_analysis.qmd
open scripts/1_analysis.html
```

Raw data under `analysis/data/` should be placed locally before rendering.

