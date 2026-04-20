
```markdown
# Soybean_Gwas_Project

## Overview

This repository contains a **Soybean Genome‑Wide Association Study (GWAS)** workflow implemented in **R** and documented using **Quarto**. Phenotype and genotype data are analyzed across multiple sections, and results are published as a static HTML website via **GitHub Pages**.

The project is designed to be:
- **Reproducible** across machines
- **Self‑contained** (project‑relative file paths only)
- **Documented** through a rendered Quarto website

---

## Repository Structure

```

Soybean\_Gwas\_Project/
├── README.md                # Project overview and usage instructions
├── \_quarto.yml              # Quarto project configuration
├── quarto/                  # Quarto source files (.qmd)
│   └── entire project combined sections.qmd
├── raw\_data/                # Phenotype and genotype input data
├── R\_codes/                 # Helper R scripts and functions
├── outputs/                 # Intermediate or auxiliary outputs (if applicable)
├── docs/                    # Rendered HTML site (GitHub Pages source)

````

All input data files are expected to reside in `raw_data/`.

---

## Software Requirements

To run the analysis locally, you will need:

- **R**
- **Quarto**
- Required R packages, including (but not limited to):
  - `tidyverse`
  - `here`
  - `readr`
  - GWAS‑related packages (e.g. `GAPIT`)

---

## Reproducibility and File Paths

The analysis is written to be portable across computers:

- All data and files are accessed using **project‑relative paths**, for example:
  ```r
  here("raw_data", "<filename>")
````

*   Absolute paths such as `C:/Users/...` are avoided.
*   After cloning the repository, the analysis should run correctly provided required data files are present in `raw_data/`.

***

## Rendering the Analysis

The main analysis document is:

    quarto/entire project combined sections.qmd

It can be rendered using:

*   The **Render** button in RStudio, or
*   The Quarto command‑line interface.

***

## Execution Control

Quarto execution settings (e.g. `freeze`) are used to manage computational cost and avoid unnecessary recomputation during repeated renders.

***

## Viewing Results (GitHub Pages)

Rendered results are published as a static website:

*   The **`docs/`** directory contains the HTML output.
*   GitHub Pages serves the site directly from this folder.

Viewing the website requires only a web browser; no R environment or data files are needed.

```

