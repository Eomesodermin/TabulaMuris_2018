# Tabula Muris 2018 — mouse multi-organ atlas (immune subset re-analysis)

Re-analysis of the publicly available single-cell dataset from:

> **The Tabula Muris Consortium. Single-cell transcriptomics of 20 mouse organs creates a Tabula Muris.**  
> *Nature* 2018. https://doi.org/10.1038/s41586-018-0590-4  
> Data: figshare / GEO: GSE109774

## Dataset at a glance
- **System:** Mouse multi-organ reference atlas — immune-cell compartment
- **Assay:** 10x Genomics + Smart-seq2 scRNA-seq
- **Accession / source:** figshare / GEO: GSE109774

## What this repository does
Preprocesses the immune-cell compartment of the mouse multi-organ atlas into a Seurat object for cross-tissue immune comparisons. See `scripts/01_Tabula_Muris_immune_cell_dataset_preprocessing.Rmd`.

## Repository structure
- `scripts/` — analysis pipeline (numbered `.Rmd` scripts run in order)
- `Setup.R` / `Load_packages.R` — environment setup and package loading
- Large data objects are **not** tracked in Git — download from the source above.

---
Part of my NK / T-cell single-cell research programme — see my [GitHub profile](https://github.com/Eomesodermin) and [dilloncorvino.com](https://dilloncorvino.com).  
Author: **Dillon Corvino**

## Environment

Built in **R** with a Seurat-based single-cell stack — key packages: `Seurat`, `SeuratDisk`, `scCustomize`, `dplyr`, `ggplot2`, plus my helper package [`r-utility-functions`](https://github.com/Eomesodermin/r-utility-functions).

A pinned `renv.lock` is **not** committed for this repository. To capture an exact, reproducible
environment, run in the project root:

```r
install.packages("renv")
renv::init()        # discovers dependencies from the scripts
renv::snapshot()    # writes renv.lock pinning every package version
```
