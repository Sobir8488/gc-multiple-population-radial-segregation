DOI: [![DOI](https://zenodo.org/badge/1327546214.svg)](https://doi.org/10.5281/zenodo.21848593)
# Beyond global concentration — reproducibility release v1.0.0

**Zenodo DOI:** `10.5281/zenodo.21848593`

This archive is the data/code/figure reproducibility release for:

**Beyond global concentration: differential radial segregation of multiple populations in six Galactic globular clusters**

Authors:
1. Sirojiddin Turaev
2. Sobir Turaev (corresponding author)
3. Davron Ismoilov

Corresponding author: `sobr8488@mail.ru`

## What is included

This release contains the scientific products needed to document and reproduce the main analysis:

- probabilistic 1P/2P classifications for the six science clusters;
- frozen radial support, knots, cross-validation folds and smoothness-boundary products;
- the final six-cluster numerical result table;
- the final cluster-by-cluster interpretation/claim boundary;
- synthetic curvature positive-control summaries;
- the quantitative Leitinger et al. (2023) cross-check;
- manuscript-grade science figures;
- the executable analysis code, protocols and Windows runners for the primary HST analysis;
- validation/provenance records;
- file-level SHA-256 checksums.

## What is deliberately NOT included

The manuscript is intentionally excluded. This archive contains **no manuscript PDF, no `main.tex`, and no manuscript bibliography**.

Raw third-party HUGS/HST source catalogues are also not redistributed. The derived classification products are included, while the public source data should be obtained from the original MAST HUGS archive:

https://archive.stsci.edu/prepds/hugs/

The failed ground-transfer pathway is not part of the primary release because it was not validated for outer-field science.

## Scientific target

The released conditional quantity is

`Delta_gamma(R) = - d logit[p_2P(R)] / d ln R`

under the assumption that both populations share the same selection function inside the frozen RGB sample.

The analysis does **not** claim absolute population-specific surface-density slopes without artificial-star/effective-area closure.

## Final six-cluster interpretation

- **NGC 5272:** clean conditional radial differential structure.
- **NGC 5024:** robust HST-footprint radial average with persistent non-axisymmetry.
- **NGC 6205:** robust HST-footprint radial average with persistent non-axisymmetry.
- **NGC 2808:** quality-sensitive; excluded from the primary radial claim.
- **NGC 3201:** no resolved differential radial trend.
- **NGC 5904:** no resolved differential radial trend.

The synthetic calibration shows that the frozen selector is conservative for localized curvature. The observed profiles should therefore be interpreted as broad/low-order radial constraints rather than detailed reconstructions of non-monotonic structure.

## Directory structure

- `data/final_results/` — final numerical science summaries and curvature calibration.
- `data/population_probabilities/` — six-cluster q2P products and classifier summaries.
- `data/support_and_smoothing/` — support, knots, folds, hygiene and boundary-closure products.
- `data/literature_crosscheck/` — Leitinger et al. (2023) comparison inputs/results.
- `tables/` — publication-facing machine-readable tables.
- `figures/` — final science figures (PDF).
- `code/` — analysis scripts, stage configs, decision documentation and runners.
- `protocols/` — convenient copies of the principal frozen protocol files.
- `provenance/` — preflight/decision/replay records and release-scope notes.
- `licenses/` — code/data licensing and third-party-data notice.
- `manifest/` — SHA-256 manifest and file inventory.

## Reproduction order

The primary HST pathway is:

`Stage1C2 -> Stage1C2B -> Stage1C3 -> Stage1C3B -> Stage1D1A -> Stage1D1B -> Stage1D1B2 -> Stage1D2 -> Stage1D3(v0.1.1 hotfix) -> Stage1D3B -> Stage1D3C -> Stage1D4 -> Stage1E -> Stage1G -> Stage1G2`

Stage1G is a post-freeze sensitivity calibration and does not alter any real-cluster class.

## DOI insertion before Zenodo publication

After Zenodo assigns/reserves the exact-version DOI:

1. replace `<INSERT_ZENODO_EXACT_VERSION_DOI_HERE>` in this `README.md`;
2. add the DOI in `CITATION.cff` at the marked placeholder;
3. optionally add the DOI to your GitHub release page and manuscript Data/Code Availability statement;
4. do **not** change any scientific output after the final checksum freeze unless you increment the release version.

## Citation

Until the DOI is inserted, cite the release as:

Turaev, S., Turaev, S., & Ismoilov, D. (2026). *Beyond global concentration: differential radial segregation of multiple populations in six Galactic globular clusters: reproducibility release* (v1.0.0). Zenodo. DOI: <INSERT_ZENODO_EXACT_VERSION_DOI_HERE>

## License

- Analysis code: MIT.
- Derived data, figures, tables and documentation: CC BY 4.0.
- Third-party source catalogues: original provider/archive terms; not redistributed here.

See `licenses/`.
