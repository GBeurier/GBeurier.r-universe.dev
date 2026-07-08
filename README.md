# GBeurier.r-universe.dev

[R-universe](https://r-universe.dev) registry for public R packages in the
[nirs4all ecosystem](https://github.com/GBeurier).

`packages.json` lists the R packages built and published at
**https://gbeurier.r-universe.dev**:

| Package | Description |
|---|---|
| **n4m** | Portable PLS / NIRS engine (full surface) over the libn4m C ABI |
| **pls4all** | Slim PLS-only subset |
| **nirs4allformats** | Rust-backed spectroscopy file readers for R |
| **nirs4allformats.lite** | Lean no-Parquet `nirs4allformats` build variant |
| **nirs4allio** | Dataset assembly bridge for nirs4all formats and datasets |
| **dagmldata** | R surface for DAG-ML typed data contracts |
| **nirs4alldatasets** | Curated NIRS reference dataset catalog |
| **nirs4all** | V1 RC portable aggregate from `nirs4all-core` |

Each package is built from the source repository and subdirectory declared in
`packages.json`. Some packages include repository-specific `.prepare` hooks to
stage native code or generated binding assets before the R-universe build.

## Install

```r
install.packages("n4m",
  repos = c("https://gbeurier.r-universe.dev", "https://cloud.r-project.org"))

install.packages("pls4all",
  repos = c("https://gbeurier.r-universe.dev", "https://cloud.r-project.org"))

install.packages("nirs4allformats",
  repos = c("https://gbeurier.r-universe.dev", "https://cloud.r-project.org"))

install.packages("nirs4all",
  repos = c("https://gbeurier.r-universe.dev", "https://cloud.r-project.org"))
```
