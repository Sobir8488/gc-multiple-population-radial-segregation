# Data dictionary

## `data/final_results/final_cluster_results.csv`

- `cluster_id`: NGC identifier.
- `D_diff`: mean differential radial-slope summary over the frozen claim interval.
- `D_diff_p16`, `D_diff_p84`: 68% latent-membership bootstrap interval.
- `S_diff`: RMS differential-slope summary.
- `permutation_p`: global radius–population permutation p-value.
- `BH_q`: Benjamini–Hochberg FDR-adjusted q-value across the six clusters.
- `final_science_class`: frozen machine-readable interpretation class.
- `final_interpretation`: reader-facing interpretation after spatial/quality validation.

## `data/population_probabilities/<cluster>/..._population_probabilities.csv.gz`

Derived Stage1C3 probabilistic 1P/2P classifications. The primary science analysis uses the continuous 2P probability rather than hard population labels.

## `data/support_and_smoothing/`

Contains the frozen radial supports, cross-validation folds, spline knots, master-star hygiene information, and exact penalty-nullspace smoothness closure.

## `data/final_results/stage1g_synthetic_curvature_power_summary.csv`

Post-freeze positive-control/sensitivity calibration. It cannot change observed-cluster classifications.

## `data/literature_crosscheck/leitinger2023_crosscheck.csv`

Quantitative comparison with Leitinger et al. (2023). `D_diff` and `A+` are complementary but non-equivalent estimands.
