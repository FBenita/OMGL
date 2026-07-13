# Optimization over Mutable Geographic Layers (OMGL)

This repository contains the implementation accompanying the manuscript

> **Optimization over Mutable Geographic Layers: A General Framework for Predictive Spatial Optimization**

## Overview

OMGL is a spatial optimization framework that combines

- predictive surrogate modeling,
- graph diffusion,
- and accelerated lazy greedy optimization

to optimize infrastructure allocation over large metropolitan pedestrian networks.

The repository contains the complete computational workflow used in the manuscript, including optimization, benchmarking, and post-optimization statistical analyses.

---

## Repository structure

```
OMGL/
│
├── notebooks/
│   ├── 01_run_omgl_optimization.ipynb
│   ├── 02_lazy_greedy_benchmarking.ipynb
│   └── 03_post_optimization_analysis.ipynb
│
├── data/
├── figures/
└── results/
```

---

## Notebook descriptions

### 01_run_omgl_optimization.ipynb

Main computational pipeline.

This notebook performs

- loading and preprocessing spatial datasets,
- construction of the spatial graph,
- predictive surrogate training,
- execution of the OMGL optimization,
- export of optimized intervention layers (GeoPackage).

Outputs include optimized intervention maps and GIS layers used throughout the manuscript.

---

### 02_lazy_greedy_benchmarking.ipynb

Computational benchmarking.

This notebook reproduces the scalability experiments presented in the paper, including

- neighborhood statistics,
- influence-radius experiments,
- stale-bound analysis,
- computational runtime benchmarks.

Outputs correspond to the computational performance tables.

---

### 03_post_optimization_analysis.ipynb

Post-processing of optimization outputs.

This notebook computes

- intervention-order statistics,
- nearest-neighbor distances,
- influence-region overlap,
- OLS regressions,
- Spearman/Pearson correlations,

and generates the figures used to characterize the spatial behavior of the optimization algorithm.

---

## Data

The repository does not include the full GIS datasets because of their size.

The analysis relies on

- OpenStreetMap
- WorldPop Population Counts

Processed intermediate datasets generated during the workflow can be stored inside the `data/` directory.

---

## Requirements

Install the required Python packages using

```bash
pip install -r requirements.txt
```

---

## Reproducibility

To reproduce the manuscript:

1. Execute

```
01_run_omgl_optimization.ipynb
```

2. Execute

```
02_lazy_greedy_benchmarking.ipynb
```

3. Execute

```
03_post_optimization_analysis.ipynb
```

The generated figures and tables correspond to those reported in the manuscript.

---

## Citation

If you use this repository, please cite both the accompanying paper and the Zenodo DOI associated with this release.
