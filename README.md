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
| n4m | 1.3.15 | `81755e6aa484efb02359867b08901f40bd414ff9` |
| pls4all | 1.3.15 | `81755e6aa484efb02359867b08901f40bd414ff9` |
| nirs4allformats | 0.2.16 | `819f5764a2138d755155e5018d7bbcb178924861` |
| nirs4allio | 0.3.1 | `28e47c9d6491b83a31dd36a25f2b0a35eeab9860` |
| dagml | 0.4.0 | `beaba0b62f9a65bca86c2f521fc482bd80092ba3` |
| dagmldata | 0.2.16 | `bbddf63671a689a2afd51e97cb631b09db96af77` |
| nirs4alldatasets | 0.3.19 | `57ccd12fddbfb767b3ff5941433af5980f175c96` |
| nirs4all | 0.7.5 | `6e8412ac4fcd2f353e552da972c54f4ebcf7b6bd` |

Datasets selects the public `v0.3.19` release source. This source selection
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
