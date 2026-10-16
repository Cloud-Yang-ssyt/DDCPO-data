# DDCPO manuscript data

Data accompanying **DDCPO: A Dimension-Decoupled Crested Porcupine Optimizer
for Mobile Robot Path Planning**, by Dingzhe Yang, Shuping Xu, Yiyu Chen and
Lu Dai.

## Contents

| Folder | Contents and coverage |
| --- | --- |
| `maps/` | Five binary input grids (20x20 to 60x60), endpoints and coordinate/orientation notes for the path-planning figures. |
| `cec2017/` | CEC2017 results reported in the manuscript's tables, with their printed precision and source limitations documented in the folder README. |
| `ablation_figure8/` | Only the final Figure 8 data: the four plotted groups, 150 matched map-seed trials / 600 group-run records, and the saved mean ranks and 97.5% confidence intervals. |

Read each folder's README.txt for field definitions and provenance.

## Coverage of the CEC2017 files

The CEC CSVs are **reported summary values**, rather than individual-run
samples or convergence histories. The available source archive does not
provide the full numerical trajectories and individual samples behind
Figures 3 and 4. These summary files therefore do not reconstruct those
curves or boxplots. No values were estimated from image pixels.

The third-party CEC2017 benchmark implementation and official benchmark
input files are outside this release; see the benchmark reference cited
in the manuscript.

## Data preparation

This is a data-only release. It contains existing numerical records and
value-preserving exports, together with documentation. It does not include
algorithm source code. No optimization experiments, ranks, bootstrap
intervals or new scientific statistics were generated when preparing it.
It is a supporting-data collection, rather than an executable reproduction
package for the complete study.

`checksums.sha256` records a SHA-256 digest for each data/documentation file.
