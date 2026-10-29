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
| **nirs4allio** | Dataset assembly bridge for nirs4all formats and datasets |
| **dagml** | R binding for the DAG-ML execution contracts |
| **dagmldata** | R surface for DAG-ML typed data contracts |
| **nirs4alldatasets** | Curated NIRS reference dataset catalog |
| **nirs4all** | End-user R pipeline package from `nirs4all-r` tag `v0.7.3` |

Each package is built from the source repository and subdirectory declared in
`packages.json`. Some packages include repository-specific `.prepare` hooks to
stage native code or generated binding assets before the R-universe build.
The current release cohort is Formats 0.2.13, IO 0.2.11, DAG-ML 0.3.43,
DAG-ML-Data 0.2.14, Datasets 0.3.16 and the R pipeline 0.7.3. DAG-ML, Datasets and
the R pipeline track immutable release tags. Formats, IO and DAG-ML-Data are pinned by full commit for their R packaging
revisions. These references include the 29 October 2026 platform/documentation
corrections without replacing existing release tags or native registry artifacts:

| R package | Revision | Correction |
|---|---|---|
| nirs4allformats | `46eb653c6463c3515b26ee6691579e27a2301b63` | Honor the declared Windows ARM64 target and native Cargo build directory |
| nirs4allio | `cbd467f4f7fd59d5a1ce0909a33fb9394b8bedb8` | Use the declared ARM64 target, private Cargo paths and LLVM unwind runtime |
| dagmldata | `03199ecb7dd27f275edbdbddb13bff3bc5ec6fe9` | Include documentation for the exported in-memory provider |
| nirs4alldatasets | `v0.3.16` | Retain the ARM64/WebR packaging corrections; use catalog-declared numeric/categorical types in curated views and invalidate converter caches with the new version |

These references describe the R source packages, not replacement PyPI, npm or
crates.io releases. Native HTTPS certificate checks remain enabled. WebR retains
local cache verification/preparation; host transport is required to stage new
network resources.

The `n4m` and `pls4all` entries track the default branches of their source
repositories. Published binaries can lag those branches while R-universe
rebuilds; check the package page or API for the actual version and source SHA.
Source availability also does not imply every binary platform succeeded. For
example, a macOS builder preparation failure before source checkout must be
distinguished from a package compilation/check failure.

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
