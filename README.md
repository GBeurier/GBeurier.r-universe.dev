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
| nirs4allformats | 0.2.19 | `5499372e0b32a35f6cc5a9aeec657ab2a1a1d1f7` |
| nirs4allio | 0.3.8 | `ce82e0ac074b322d04a276c57cd9bf2b5f8adc91` |
| dagml | 0.5.0 | `d3608565a5fe27875d4b64e54035eb8b4c05b204` |
| dagmldata | 0.2.17 | `8c86f13d3ff1c3fbdba94e18d73d4c2b367320c3` |
| nirs4alldatasets | 0.3.22 | `6011ab023a3975e69b78b4f2e453f314cec1d974` |
| nirs4all | 0.8.0 | `d1d7517cb45813722e9c9d74b1a2181bc8f000a8` |

Datasets selects the reviewed `0.3.22` source. This source selection
does not assert completion of the hosted R publisher or the R-universe rebuild.
The updated cohort still requires distributed build and platform results.

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
