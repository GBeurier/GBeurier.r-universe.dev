# GBeurier.r-universe.dev

[R-universe](https://r-universe.dev) registry for
[nirs4all-methods](https://github.com/GBeurier/nirs4all-methods).

`packages.json` lists the R packages built and published at
**https://gbeurier.r-universe.dev**:

| Package | Description |
|---|---|
| **n4m** | Portable PLS / NIRS engine (full surface) over the libn4m C ABI |
| **pls4all** | Slim PLS-only subset |

Both are built from subdirectories of the monorepo; a `.prepare` pre-build hook
vendors the libn4m C/C++/Fortran core into a self-contained source tarball, so
R-universe builds them with no external libn4m.

## Install

```r
install.packages("n4m",
  repos = c("https://gbeurier.r-universe.dev", "https://cloud.r-project.org"))

install.packages("pls4all",
  repos = c("https://gbeurier.r-universe.dev", "https://cloud.r-project.org"))
```
