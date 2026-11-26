# GBeurier.r-universe.dev

[R-universe](https://r-universe.dev) registry for public R packages in the
[nirs4all ecosystem](https://github.com/GBeurier).

`packages.json` selects the source repositories built and published at
**https://gbeurier.r-universe.dev**:

| Package | Description |
|---|---|
| **n4m** | Portable Methods engine over the libn4m C ABI |
| **pls4all** | PLS subset of the same Methods source |
| **nirs4allformats** | Rust-backed spectroscopy file readers for R |
| **nirs4allio** | Dataset assembly over the IO and Formats owners |
| **dagml** | R binding for the DAG-ML execution contracts |
| **dagmldata** | R surface for DAG-ML typed data contracts |
| **nirs4alldatasets** | Curated NIRS reference dataset catalog |
| **nirs4all** | End-user R pipeline package from `nirs4all-r` |

Each package uses the repository and subdirectory declared in `packages.json`.
Existing `.prepare` hooks stage native sources where the package needs them.
The versions below are declared by the selected source `DESCRIPTION` files;
they do not establish that every binary platform has finished building.

| R package | Selected source version | Registry reference |
|---|---|---|
| n4m | 1.5.1 | `25041f88bebb21a19748799c1681e138a3d55dfb` |
| pls4all | 1.5.1 | `25041f88bebb21a19748799c1681e138a3d55dfb` |
| nirs4allformats | 0.3.1 | `89f191396772c71379e7ad788f29f30472369498` |
| nirs4allio | 0.4.0 | `c1c3cdfa0e394ef696c56ac65bfabdef1b65a468` |
| dagml | 0.5.0 | `d3608565a5fe27875d4b64e54035eb8b4c05b204` |
| dagmldata | 0.2.17 | `8c86f13d3ff1c3fbdba94e18d73d4c2b367320c3` |
| nirs4alldatasets | 0.4.0 | `74bd2c6a21d344771efa0c23695216e667daba6b` |
| nirs4all | 0.8.0 | `d1d7517cb45813722e9c9d74b1a2181bc8f000a8` |

The weekday reader cohort selects Formats 0.3.1, IO 0.4.0 and Datasets
0.4.0. Each source revision matches the owner release tag. The owner R
workflows and the R-universe platform builds report their own results.

Both Methods packages use the same explicit commit. The other entries also use
explicit commits or release tags; none implicitly follows a default branch.
These references select R source packages and do not replace PyPI, npm or
crates.io artifacts or move the package repositories' Main branches.

Actual published versions, source commits and platform results are available on
the [build dashboard](https://gbeurier.r-universe.dev/builds) and each package's
API, for example [n4m](https://gbeurier.r-universe.dev/api/packages/n4m) and
[nirs4all](https://gbeurier.r-universe.dev/api/packages/nirs4all). Source
availability is distinct from successful Linux, macOS and Windows distribution.
Native HTTPS certificate checks remain enabled. WebR retains local cache
verification and preparation; host transport stages new network resources.

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
