# DRSI: Decision-Robust Selection Index

Analysis code accompanying the paper **"Beyond the Pareto front: a decision-robust index for selecting groundwater management strategies from explainable post-optimality analysis"** (Mishra et al., submitted to *Journal of Hydrology*).

## Overview

This repository contains the Jupyter notebook used to:

- generate and analyze synthetic multi-objective groundwater management benchmarks (MODFLOW 6 + NSGA-II/MOEA-D/SMS-EMOA via `pymoo`),
- fit surrogate models and compute explainability attributions (SHAP, LIME, GAM, PCA) against a Sobol sensitivity ground truth (`SALib`),
- compute the Decision-Robust Selection Index (DRSI) and compare it against TOPSIS and other post-optimality selection rules across all Pareto fronts, including the real-world Ain basin (France) case study.

## Contents

- `dv_paper_analysis_FINAL (1).ipynb` — the main analysis notebook, run top-to-bottom.

## Requirements

- Python 3.x with: `numpy`, `pandas`, `scipy`, `scikit-learn`, `shap`, `pymoo`, `SALib`, `flopy`, `geopandas`, `contextily`, `matplotlib`, `seaborn`, `nbformat`/`nbclient`.
- [MODFLOW 6](https://github.com/MODFLOW-USGS/modflow6) executable available on `PATH` (used via FloPy for the groundwater flow simulations).
- The Ain basin case study additionally requires the external optimization output (`PyGWMO`) and basin shapefiles, which are not included in this repository.

## Running

Run the notebook cells in order. It caches intermediate results (MODFLOW runs, surrogate fits) under `cache/` so repeat runs after the first are fast.

## Citation

If you use this code, please cite the associated paper (details to be added upon publication).

## Contact

Shreyansh Mishra — BRGM — s.mishra@brgm.fr

## License

MIT — see [LICENSE](LICENSE).
